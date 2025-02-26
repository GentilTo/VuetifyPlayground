<script setup>
  import { ref, onMounted, onUnmounted, computed } from 'vue'

  const items = ref([
    { title: 'Step 1', activity: '', icon: 'mdi-check', class: 'success' },
    {
      title: 'Step 2',
      activity: '(Process: 1)',
      icon: 'mdi-progress',
      class: 'primary',
    },
    { title: 'Step 3', activity: '', icon: 'mdi-timer', class: 'cancel' },
    { title: 'Step 4', activity: '', icon: 'mdi-timer', class: 'cancel' },
    { title: 'Step 5', activity: '', icon: 'mdi-timer', class: 'cancel' },
  ])

  const runningText = ref('Running')
  const isExpanded = ref(false)
  const toggleSize = () => (isExpanded.value = !isExpanded.value)
  const centerHeight = computed(() => (isExpanded.value ? '120px' : '50px'))

  let interval

  onMounted(() => {
    let dots = 0
    let process = 1
    interval = setInterval(() => {
      dots = (dots + 1) % 4
      process = dots == 3 ? (process % 2) + 1 : process
      runningText.value =
        '1st step (Process: ' + process + ') is running' + '.'.repeat(dots)
    }, 500)
  })

  onUnmounted(() => {
    clearInterval(interval)
  })
</script>

<template>
  <v-container class="d-flex justify-center">
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert component-transation"
      :style="{ height: isExpanded ? '210px' : '140px', width: '380px'}"
    >
      <v-row align="end" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="9">
          <span class="text-body-1">Dummy to Azure</span>
        </v-col>
        <v-col cols="1" class="text-center">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>

      <v-row
        align="start"
        no-gutters
        class="component-transation"
        :style="{ height: centerHeight, minHeight: 'auto', maxHeight: '210px' }"
      >
        <!-- Azure icon -->
        <v-col cols="2">
          <VProgressCircular
            v-if="!isExpanded"
            indeterminate
            class="primary-light-theme"
          />
        </v-col>

        <!-- Description and items -->
        <v-col cols="9">
          <small v-if="!isExpanded">{{ runningText }}</small>

          <!-- Looping through items -->
          <v-row
            v-if="isExpanded"
            v-for="(item, i) in items"
            :key="i"
            class="activity-row"
            align="center"
            no-gutters
            style="height: auto; min-height: auto"
          >
            <v-col cols="1" style="height: auto; min-height: auto">
              <v-icon
                v-if="item.icon != 'mdi-progress'"
                v
                :class="item.class"
                size="15px"
                >{{ item.icon }}</v-icon
              >
              <v-icon size="15px" v-if="item.icon == 'mdi-progress'">
                <VProgressCircular indeterminate class="primary-light-theme"
              /></v-icon>
            </v-col>
            <v-col cols="10" style="height: auto; min-height: auto">
              <small>{{ item.title + ' ' + item.activity }}</small>
            </v-col>
          </v-row>
        </v-col>

        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="8">
          <div>
            <v-btn variant="outlined" size="x-small" rounded class="mr-1"
              >Cancel</v-btn
            >
            <v-btn
              variant="outlined"
              size="x-small"
              rounded
              class="mr-1"
              @click="toggleSize"
              >{{ isExpanded ? 'View less' : 'View more' }}</v-btn
            >
          </div>
        </v-col>
        <!-- Timestamp -->
        <v-col cols="2" class="text-center">
          <small>14:25</small>
        </v-col>
      </v-row>
    </v-alert>
    <span class="mr-2"></span>
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert"
    >
      <v-row align="end" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="9">
          <span class="text-body-1">Dummy to Azure</span>
        </v-col>
        <v-col cols="1" class="text-center">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters>
        <!-- Azure icon -->
        <v-col cols="2">
          <v-icon size="50" class="cancel">mdi-microsoft-azure</v-icon>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="9">
          <small>Canceled by user.</small>
        </v-col>
        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="9">
          <div v-if="false">
            <v-btn variant="outlined" size="x-small" rounded class="mr-1"
              >View error</v-btn
            >
          </div>
        </v-col>
        <!-- Timestamp -->
        <v-col cols="1" class="text-center">
          <small>1d</small>
        </v-col>
      </v-row>
    </v-alert>
  </v-container>
  <!-- --------------------------------------------------------------------------------- -->
  <v-container class="d-flex justify-center">
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert dark-theme"
    >
      <v-row align="end" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="9">
          <span class="text-body-1 dark-theme">Dummy to Azure</span>
        </v-col>
        <v-col cols="1" class="text-center">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon class="dark-theme">mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>

      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col cols="2">
          <VProgressCircular indeterminate class="primary-dark-theme" />
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="10">
          <small class="dark-theme">{{ runningText }}</small>
        </v-col>
      </v-row>

      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="8">
          <div>
            <v-btn
              variant="outlined"
              size="x-small"
              rounded
              class="mr-1 dark-theme"
              >Cancel</v-btn
            >
            <v-btn
              variant="outlined"
              size="x-small"
              rounded
              class="mr-1 dark-theme"
              >View more</v-btn
            >
          </div>
        </v-col>
        <!-- Timestamp -->
        <v-col cols="2" class="text-center dark-theme">
          <small>14:20</small>
        </v-col>
      </v-row>
    </v-alert>
    <span class="mr-2"></span>
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert dark-theme"
    >
      <v-row align="end" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="9">
          <span class="text-body-1 dark-theme">Dummy to Azure</span>
        </v-col>
        <v-col cols="1" class="text-center">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon class="dark-theme">mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters>
        <!-- Azure icon -->
        <v-col cols="2">
          <v-icon size="50" class="cancel">mdi-microsoft-azure</v-icon>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="9">
          <small class="dark-theme">Canceled by user.</small>
        </v-col>
        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="9">
          <div v-if="false">
            <v-btn
              variant="outlined"
              size="x-small"
              rounded
              class="mr-1 dark-theme"
              >View error</v-btn
            >
          </div>
        </v-col>
        <!-- Timestamp -->
        <v-col cols="1" class="text-center">
          <small class="dark-theme">1d</small>
        </v-col>
      </v-row>
    </v-alert>
  </v-container>
</template>

<style scoped>
  .component-transation {
    transition: height 0.3s ease-in-out;
  }
  .custom-alert {
    max-height: 210px;
    max-width: 380px;
  }

  .light-theme {
    background-color: #eeeeee;
  }

  .dark-theme {
    background-color: #505050;
    color: white;
  }
  .primary-light-theme {
    color: #361d5c;
  }
  .primary-dark-theme {
    color: #5c4582;
  }

  .success {
    color: #02a481;
  }
  .cancel {
    color: grey;
  }
  .error {
    color: #c43633;
  }

  :deep(*) {
    font-family: 'Segoe UI';
  }
</style>
