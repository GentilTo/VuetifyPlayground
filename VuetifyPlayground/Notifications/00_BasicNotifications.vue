<script setup>
  const title = 'Cleun storage files'
  const description = 'Cleared 3 files from database.'
  const icon = 'mdi-recycle'
  const icon_size = 40
  const time = '14:00'
</script>

<template>
  <v-container class="d-flex justify-center">
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert"
    >
      <v-row align="end" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="8">
          <span class="text-body-1">{{ title }}</span>
        </v-col>
        <v-col cols="2" class="text-right">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>

      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col cols="2">
          <v-icon :size="icon_size" class="success">{{ icon }}</v-icon>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="8">
          <small>{{ description }}</small>
        </v-col>
        <v-col cols="2" />
      </v-row>

      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="8"> </v-col>
        <!-- Timestamp -->
        <v-col cols="2" class="text-right">
          <small>{{ time }}</small>
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
        <v-col cols="8">
          <span class="text-body-1">{{ title }}</span>
        </v-col>
        <v-col cols="2" class="text-right">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col cols="2">
          <v-icon :size="icon_size" class="error">{{ icon }}</v-icon>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="8">
          <small>Failed.</small>
        </v-col>
        <v-col cols="2" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="8">
          <div>
            <v-btn variant="outlined" size="x-small" rounded class="mr-1"
              >View error</v-btn
            >
          </div>
        </v-col>
        <!-- Timestamp -->
        <v-col cols="2" class="text-right">
          <small>{{ time }}</small>
        </v-col>
      </v-row>
    </v-alert>
  </v-container>
  <!-- Dark theme ---------------------------------------------------------------- -->
  <v-container class="d-flex justify-center">
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert dark-theme"
    >
      <v-row align="end" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="8">
          <span class="text-body-1 dark-theme">{{ title }}</span>
        </v-col>
        <v-col cols="2" class="text-right">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon class="dark-theme">mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>

      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col cols="2">
          <v-icon :size="icon_size" class="success">{{ icon }}</v-icon>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="8">
          <small class="dark-theme">{{ description }}</small>
        </v-col>
        <v-col cols="2" />
      </v-row>

      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="8"> </v-col>
        <!-- Timestamp -->
        <v-col cols="2" class="text-right dark-theme">
          <small>{{ time }}</small>
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
        <v-col cols="8">
          <span class="text-body-1 dark-theme">{{ title }}</span>
        </v-col>
        <v-col cols="2" class="text-right">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon class="dark-theme">mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col cols="2">
          <v-icon :size="icon_size" class="error">{{ icon }}</v-icon>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="8">
          <small class="dark-theme">Failed.</small>
        </v-col>
        <v-col cols="2" />
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
              >View error</v-btn
            >
          </div>
        </v-col>
        <!-- Timestamp -->
        <v-col cols="2" class="text-right">
          <small class="dark-theme">{{ time }}</small>
        </v-col>
      </v-row>
    </v-alert>
  </v-container>
</template>

<style scoped>
  .custom-alert {
    max-width: 380px;
    max-height: 140px;
  }
  .light-theme {
    background-color: #424242;
  }
  .dark-theme {
    background-color: #505050;
    color: white;
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
  * {
    font-family: 'Segoe UI';
  }

  .primary {
    color: #5c4582;
  }
</style>
