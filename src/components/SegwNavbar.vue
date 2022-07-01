<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">
        <img src="../assets/logo.svg" alt="" width="30" height="24">
        Solos::Tec
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
        aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav me-auto">
          <li class="nav-item">
            <router-link class="nav-link" to="/">{{ $t("nav-home") }}</router-link>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
              {{ $t('nav-config') }}
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfDevices' }">{{ $t("nav-devices")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfGateways' }">{{ $t("nav-gateways")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfMeter' }">{{ $t("nav-meter") }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfwMBus' }">{{ $t("nav-config-wmbus") }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfIEC' }">{{ $t("nav-iec") }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfLoRa' }">{{ $t("nav-LoRa") }}
                </router-link>
              </li>
              <li>
                <hr class="dropdown-divider">
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfUpload' }">{{ $t("nav-upload") }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfDownload' }">{{ $t("nav-download")
                }}
                </router-link>
              </li>
              <li>
                <hr class="dropdown-divider">
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfSystem' }">{{ $t("nav-system") }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'ConfWeb' }">{{ $t("nav-web") }}
                </router-link>
              </li>
            </ul>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
              {{ $t("Navbar-Collectors") }}
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li>
                <router-link class="dropdown-item" :to="{ name: 'LoRaUplink' }">{{ $t("Navbar-Collectors-LoRaUplink")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'MBusRadio' }">{{ $t("Navbar-Collectors-MBusRadio")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'CollectorsIEC' }">{{
                    $t("Navbar-Collectors-CollectorsIEC")
                }}
                </router-link>
              </li>
            </ul>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
              {{ $t("Navbar-Status") }}
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li>
                <router-link class="dropdown-item" :to="{ name: 'StatusSessions' }">{{ $t("Navbar-Status-Sessions")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'StatusTargets' }">{{ $t("Navbar-Status-Targets")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'StatusConnections' }">{{
                    $t("Navbar-Status-Connections")
                }}
                </router-link>
              </li>
            </ul>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
              {{ $t("Navbar-Monitoring") }}
            </a>
            <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
              <li>
                <router-link class="dropdown-item" :to="{ name: 'MonitoringSystem' }">{{ $t("Navbar-Monitoring-System")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'MonitoringMessages' }">{{
                    $t("Navbar-Monitoring-Messages")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'MonitoringIECGateways' }">{{
                    $t("Navbar-Monitoring-IECGateways")
                }}
                </router-link>
              </li>
              <li>
                <router-link class="dropdown-item" :to="{ name: 'MonitoringwMBusGateways' }">{{
                    $t("Navbar-Monitoring-wMBusGateways")
                }}
                </router-link>
              </li>
            </ul>
          </li>
        </ul>
        <ul class="navbar-nav mr-auto">
          <li class="nav-item">
            <a class="nav-link">{{ $t("Navbar-User") }}</a>
          </li>
          <li class="nav-item">
            <LocaleSwitcher />
          </li>
          <li class="nav-item">
            <a class="nav-link">{{ $t("Navbar-Status") }}</a>
          </li>
        </ul>
      </div>

    </div>
  </nav>
</template>

<script>
import LocaleSwitcher from "../components/LocaleSwitcher.vue";

export default {
  name: "BootstrapNavbar",
  components: { LocaleSwitcher }
};

</script>