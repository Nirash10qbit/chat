<template>
  <div
    class="user-profile-sidebar"
    :class="{'show': shallShowActiveChatContactSidebar}"
  >
    <!-- Header -->
    <header
      v-if="contact"
      class="user-profile-header bg-light-info "
    >
      <span class="close-icon">
        <feather-icon
          class="text-dark"
          icon="XIcon"
          @click="$emit('update:shall-show-active-chat-contact-sidebar', false)"
        />
      </span>

      <div
        style="height:80px"
      />
    </header>

    <!-- User Details -->
    <validation-observer ref="refFormObserver">
      <!-- Form -->

      <b-card>

        <div class="row g-0">

          <!-- Contact Left Side Bar -->
          <div class="col-12 d-flex justify-content-center mt-n5 ">

            <div class="avatar box-shadow-1 avatar-xl avatar-border mb-1">
              <b-avatar
                size="80"
                :src="contact.avatar"
              />
              <span
                class="avatar-status-xl"
                :class="`avatar-status-${contact.status}`"
              />
            </div>

          </div>
        </div>

        <div class="col-12 d-flex justify-content-center ">
          <h4 class="chat-user-name ">
            {{ contact.fullName }}
          </h4>
        </div>
        <div class="col-12 d-flex justify-content-center">
          <b-alert
            variant="primary"
            show
          >
            <small class="text-dark font-weight-700 mx-1 ">
              <b-badge class="bg-light-info ">
                <div class="text-dark">
                  {{ contact.role }}
                </div>
              </b-badge>
            </small>
          </b-alert>
        </div>

        <div class="col-12 d-flex justify-content-start mt-1">
          <h6 class=" font-weight-700 ">
            Personal Info
          </h6>
        </div>

        <div class="col-12 d-flex justify-content-start">
          <div class="p-2 ml-n2">
            <div class="col-12 d-flex justify-content-start ">
              <feather-icon icon="PhoneIcon" />
              <div class="ml-1">
                078 4914 9377
              </div>
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              <feather-icon icon="MailIcon" />
              <div class="ml-1">
                courtney.henry@mp.co.uk
              </div>
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              <feather-icon icon="PocketIcon" />
              <div class="ml-1">
                AP234567B
              </div>
            </div>

          </div>
        </div>

        <div class="mt-n2">
          <hr>
        </div>

        <div class="col-12 d-flex justify-content-start mt-1">
          <h6 class=" font-weight-700 ">
            Professional Info
          </h6>
        </div>

        <div class="col-12 d-flex justify-content-start mt-n1">
          <div class="p-2 ml-n2">
            <div class="col-12 d-flex justify-content-start ">
              Qualification
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              Speciality
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              IT System
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              Smart Card Number
            </div>

          </div>
          <div class="p-2 ml-n2">
            <div class="col-12 d-flex justify-content-start ">
              <h5 class="mb-0 font-weight-700">
                MRCGP
              </h5>
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              <h5 class="mb-0 font-weight-700">
                Child Protection
              </h5>
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              <h5 class="mb-0 font-weight-700">
                EMIS WEB
              </h5>
            </div>
            <div class="col-12 d-flex justify-content-start mt-1">
              <h5 class="mb-0 font-weight-700">
                123456789
              </h5>
            </div>
          </div>

        </div>

        <div class="col-12 d-flex justify-content-start mt-n2">
          <div class="p-2 ml-n2">
            <div class="col-12 d-flex justify-content-start ">
              Skills
            </div>
          </div>
        </div>
        <div class="col-12 d-flex justify-content-start mt-n2">
          <div class="p-2 ml-n2">
            <div class="col-12 d-flex justify-content-start ">
              <b-row class="pl-0 ">
                <b-col
                  class="mt-1 font-weight-light"
                  cols="12"
                >
                  <b-badge
                    class="mr-1 mb-1"
                    variant="light-info"
                  >
                    <small>Dietology</small>
                  </b-badge>
                  <b-badge
                    class="mr-1 my-1 my-md-0"
                    variant="light-info"
                  >
                    <small>Food Processing</small>
                  </b-badge>
                  <b-badge
                    class="mr-1 mb-1"
                    variant="light-info"
                  >
                    <small>Nutrition</small>
                  </b-badge>
                  <b-badge
                    class="mr-1  mb-1 my-md-0"
                    variant="light-info"
                  >
                    <small>Biochemistry</small>
                  </b-badge>
                </b-col>

              </b-row>
            </div>
          </div>
        </div>
        <div class="mt-n3">
          <hr>
        </div>

        <div class="col-12 d-flex justify-content-start mt-1">
          <h6 class=" font-weight-700 ">
            Availability Today
          </h6>
        </div>

        <div class="col-12 d-flex justify-content-start mt-n1">
          <div class="p-2 ml-n2">
            <div class="col-12 d-flex justify-content-start mb-1">
              <div><b-avatar
                variant="success"
                rounded
                size="10"
              >
                <feather-icon
                  icon="CheckIcon"
                  size="1"
                />
              </b-avatar></div>
              <span class="ml-1"> 09:00 - 12:00</span>
            </div>
            <div class="col-12 d-flex justify-content-start ">
              <div><b-avatar
                variant="success"
                rounded
                size="10"
              >
                <feather-icon
                  icon="CheckIcon"
                  size="1"
                />
              </b-avatar></div>
              <span class="ml-1"> 14:00 - 18:00</span>
            </div>
          </div>
        </div>

        <div class="mt-n1">
          <hr>
        </div>

        <b-button
          v-ripple.400="'rgba(255, 255, 255, 0.15)'"
          variant="primary"
          block
          class=" mx-1 "
        >
          View Full Profile
        </b-button>
      </b-card>

    </validation-observer>
  </div>
</template>

<script>
import { BAvatar, BBadge, BButton } from 'bootstrap-vue'

export default {
  components: {
    // BSV
    BAvatar,
    BBadge,
    BButton,

    // 3rd Party
  },
  props: {
    shallShowActiveChatContactSidebar: {
      type: Boolean,
      required: true,
    },
    contact: {
      type: Object,
      required: true,
    },
  },
  setup() {
    const perfectScrollbarSettings = {
      maxScrollbarLength: 150,
    }

    return {
      perfectScrollbarSettings,
    }
  },
}
</script>

<style>

</style>
