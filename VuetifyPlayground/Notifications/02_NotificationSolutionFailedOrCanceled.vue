<script setup>
  const title = 'Solution creation'
  const descriptionFailed =
    "Failed to create GentilTo's Update Service solution."
  const descriptionCanceled =
    "GentilTo's Update Service solution creation was canceled."
  const buttonDescription = 'View error'
</script>

<template>
  <v-container class="d-flex justify-center">
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert"
    >
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="8" class="pl-2">
          <span class="text-body-3" style="font-weight: 600">{{ title }}</span>
        </v-col>
        <v-col cols="2" class="text-right">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col align="center" cols="2">
          <v-avatar>
            <v-icon size="50" class="error">mdi-microsoft-azure</v-icon>
          </v-avatar>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="9" class="pl-2">
          <div style="font-size: small">{{ descriptionFailed }}</div>
          <div style="font-size: small"></div>
          <div style="font-size: small"></div>
        </v-col>
        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="9" class="pl-2">
          <v-btn variant="outlined" size="x-small" rounded class="mr-1"
            >{{ buttonDescription }}</v-btn
          >
        </v-col>
        <!-- Timestamp -->
        <v-col cols="1" class="text-center">
          <small>1d</small>
        </v-col>
      </v-row>
    </v-alert>

    <span class="mr-2"></span>
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert"
    >
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="9" class="pl-2">
          <span class="text-body-3" style="font-weight: 600">{{ title }}</span>
        </v-col>
        <v-col cols="1" class="text-center">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col align="center" cols="2">
          <v-avatar>
            <v-icon size="50" class="error">mdi-docker</v-icon>
          </v-avatar>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="9" class="pl-2">
          <div style="font-size: small">{{ descriptionFailed }}</div>
          <div style="font-size: small"></div>
          <div style="font-size: small"></div>
        </v-col>
        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="9" class="pl-2">
          <v-btn variant="outlined" size="x-small" rounded class="mr-1"
            >{{ buttonDescription }}</v-btn
          >
        </v-col>
        <!-- Timestamp -->
        <v-col cols="1" class="text-center">
          <small>1d</small>
        </v-col>
      </v-row>
    </v-alert>
  </v-container>

  <v-container class="d-flex justify-center">
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert"
    >
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="8" class="pl-2">
          <span class="text-body-3" style="font-weight: 600">{{ title }}</span>
        </v-col>
        <v-col cols="2" class="text-right">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col align="center" cols="2">
          <v-avatar>
            <v-icon size="50" class="cancel">mdi-microsoft-azure</v-icon>
          </v-avatar>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="9" class="pl-2">
          <div style="font-size: small">{{ descriptionCanceled }}</div>
          <div style="font-size: small"></div>
          <div style="font-size: small"></div>
        </v-col>
        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="9" class="pl-2"> </v-col>
        <!-- Timestamp -->
        <v-col cols="1" class="text-center">
          <small>1d</small>
        </v-col>
      </v-row>
    </v-alert>

    <span class="mr-2"></span>
    <v-alert
      color="grey darken-1"
      variant="tonal"
      class="rounded-lg custom-alert"
    >
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <!-- Title and dismiss button -->
        <v-col cols="9" class="pl-2">
          <span class="text-body-3" style="font-weight: 600">{{ title }}</span>
        </v-col>
        <v-col cols="1" class="text-center">
          <v-btn icon size="x-small" variant="text" density="comfortable">
            <v-icon>mdi-close</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row align="center" no-gutters style="height: 50px">
        <!-- Azure icon -->
        <v-col align="center" cols="2">
          <v-avatar>
            <v-icon size="50" class="cancel">mdi-docker</v-icon>
          </v-avatar>
        </v-col>
        <!-- Description and buttons -->
        <v-col cols="9" class="pl-2">
          <div style="font-size: small">{{descriptionCanceled}}</div>
          <div style="font-size: small"></div>
          <div style="font-size: small"></div>
        </v-col>
        <v-col cols="1" />
      </v-row>
      <v-row align="center" no-gutters>
        <v-col cols="2" />
        <v-col cols="9" class="pl-2"> </v-col>
        <!-- Timestamp -->
        <v-col cols="1" class="text-center">
          <small>1d</small>
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
  .info {
    color: ;
  }
  * {
    font-family: 'Segoe UI';
  }
  .primary {
    color: #5c4582;
  }
</style>
