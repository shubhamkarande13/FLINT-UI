<template>
  <div>
    <div class="flex flex-wrap mt-4">
      <div
        class="
          relative
          bg-gradient-to-tl
          from-green-300
          via-blue-500
          to-purple-600
          md:pt-32
          pb-32
          pt-12
          w-full
          h-screen
        "
      >
        <div class="px-4 md:px-10 mx-auto w-full">
          <div class="bg-white p-6 rounded-lg shadow-lg">
            <h2 class="text-2xl font-bold mb-2 text-gray-800">
              GCBM simulation workflow
            </h2>
            <p class="text-gray-700">
              Follow the steps below to simulate GCBM runs.
            </p>
          </div>

          <div class="flex flex-col">
            <div class="mt-10">
              <div class="flex">
                <div class="w-1/3 text-center px-6">
                  <div
                    class="
                      bg-gray-300
                      rounded-lg
                      flex
                      items-center
                      justify-center
                      border border-gray-200
                    "
                  >
                    <div
                      class="
                        w-1/3
                        bg-transparent
                        h-20
                        flex
                        items-center
                        justify-center
                        icon-step
                      "
                    >
                      <i class="fas fa-plus fa-lg" />
                    </div>
                    <div
                      class="
                        w-2/3
                        bg-gray-200
                        h-24
                        flex flex-col
                        items-center
                        justify-center
                        px-1
                        rounded-r-lg
                        body-step
                      "
                    >
                      <h2 class="font-bold text-sm">Create a new simulation</h2>
                      <p class="text-xs text-gray-600">
                        Click the new button below
                      </p>
                    </div>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <i class="fas fa-arrow-right fa-2x" />
                </div>
                <div class="w-1/3 text-center px-6">
                  <div
                    class="
                      bg-gray-300
                      rounded-lg
                      flex
                      items-center
                      justify-center
                      border border-gray-200
                    "
                  >
                    <div
                      class="
                        w-1/3
                        bg-transparent
                        h-20
                        flex
                        items-center
                        justify-center
                        icon-step
                      "
                    >
                      <i class="far fa-file fa-lg" />
                    </div>
                    <div
                      class="
                        w-2/3
                        bg-gray-200
                        h-24
                        flex flex-col
                        items-center
                        justify-center
                        px-1
                        rounded-r-lg
                        body-step
                      "
                    >
                      <h2 class="font-bold text-sm">Upload file</h2>
                      <p class="text-xs text-gray-600">Dataset file for GCBM</p>
                    </div>
                  </div>
                </div>
                <div class="flex-1 flex items-center justify-center">
                  <i class="fas fa-arrow-right fa-2x" />
                </div>
                <div class="w-1/3 text-center px-6">
                  <div
                    class="
                      bg-gray-300
                      rounded-lg
                      flex
                      items-center
                      justify-center
                      border border-gray-200
                    "
                  >
                    <div
                      class="
                        w-1/3
                        bg-transparent
                        h-20
                        flex
                        items-center
                        justify-center
                        icon-step
                      "
                    >
                      <i class="fas fa-cogs fa-lg" />
                    </div>
                    <div
                      class="
                        w-2/3
                        bg-gray-200
                        h-24
                        flex flex-col
                        items-center
                        justify-center
                        px-1
                        rounded-r-lg
                        body-step
                      "
                    >
                      <h2 class="font-bold text-sm">Configure</h2>
                      <p class="text-xs text-gray-600">
                        Change configuration parameters
                      </p>
                    </div>
                  </div>
                </div>

                <div class="flex-1 flex items-center justify-center">
                  <i class="fas fa-arrow-right fa-2x" />
                </div>
                <div class="w-1/3 text-center px-6">
                  <div
                    class="
                      bg-gray-300
                      rounded-lg
                      flex
                      items-center
                      justify-center
                      border border-gray-200
                    "
                  >
                    <div
                      class="
                        w-1/3
                        bg-transparent
                        h-20
                        flex
                        items-center
                        justify-center
                        icon-step
                      "
                    >
                      <i class="fas fa-check fa-lg" />
                    </div>
                    <div
                      class="
                        w-2/3
                        bg-gray-200
                        h-24
                        flex flex-col
                        items-center
                        justify-center
                        px-1
                        rounded-r-lg
                        body-step
                      "
                    >
                      <h2 class="font-bold text-sm">Run</h2>
                      <p class="text-xs text-gray-600">
                        Run the simulation with new configs
                      </p>
                    </div>
                  </div>
                </div>
              </div>
            </div>

            <div class="flex flex-wrap mt-10">
              <div class="w-full lg:w-6/12 xl:w-4/12 px-4 content-center" />
              <div class="w-full lg:w-6/12 xl:w-4/12 px-4 content-center">
                <div
                  class="
                    relative
                    flex flex-col
                    min-w-0
                    break-words
                    bg-white
                    rounded
                    mb-6
                    xl:mb-0
                    shadow-lg
                  "
                >
                  <div class="flex-auto p-4">
                    <div class="relative w-full max-w-full flex-grow flex-1">
                      <span class="font-semibold text-xl text-blueGray-700">
                        Create a new Simulation
                      </span>

                      <input
                        v-model="simulation_title"
                        class="
                          w-full
                          mt-4
                          h-10
                          px-3
                          mb-2
                          text-base text-gray-700
                          placeholder-gray-600
                          border
                          rounded-lg
                          focus:shadow-outline
                        "
                        type="text"
                        placeholder="Enter title for simulation"
                      />

                      <button
                        class="
                          w-full
                          mt-4
                          block
                          align-middle
                          flex-initial
                          bg-white
                          hover:bg-black hover:text-white
                          text-gray-800
                          font-semibold
                          py-2
                          px-4
                          border border-gray-400
                          rounded
                          shadow
                        "
                        :disabled="isTitle()"
                        :class="{ 'opacity-25 cursor-not-allowed': isTitle() }"
                        @click="setNewTitle"
                      >
                        <i class="fas fa-plus" /> Set title
                      </button>

                      <button
                        class="
                          w-full
                          mt-4
                          block
                          align-middle
                          flex-initial
                          bg-white
                          hover:bg-black hover:text-white
                          text-gray-800
                          font-semibold
                          py-2
                          px-4
                          border border-gray-400
                          rounded
                          shadow
                        "
                        :disabled="isTitle()"
                        :class="{ 'opacity-25 cursor-not-allowed': isTitle() }"
                        @click="sendToAPI"
                      >
                        <i class="fas fa-plus" /> Create run
                      </button>
                    </div>
                    <p class="text-sm text-blueGray-400 mt-4">
                      <span class="whitespace-nowrap"
                        >Creates a new simulation run</span
                      >
                    </p>
                  </div>
                </div>
              </div>

              <div class="w-full lg:w-6/12 xl:w-4/12 px-4 content-center">
                <md-field>
                  <label>Multiple</label>
                  <md-file v-model="multiple" multiple />
                </md-field>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <StepperGCBM />
  </div>
</template>

<script>
import StepperGCBM from '@/components/Stepper/StepperGCBM.vue'

export default {
  name: 'DashboardPage',
  components: {
    StepperGCBM
  },

  data: () => ({
    multiple: null,
    simulation_title: ''
  }),

  methods: {
    checkforSimtitle() {
      if (this.simulation_title === '') return false
      else {
        console.log(this.simulation_title)
        return true
      }
    },
    isTitle() {
      if (this.checkforSimtitle()) {
        return false
      } else {
        return true
      }
    },
    setNewTitle() {
      //function for setting up a new title
      console.log(this.simulation_title, ' goto /gcbm/new')
      var simulation_title = this.simulation_title
      console.log('simulation_title')
      console.log(simulation_title)

      this.$store.dispatch('title_setter', simulation_title)
      console.log('from set new title')
      console.log(this.gcbm.state.Title)
    },
    sendToAPI() {
      //function to send the title to API
      this.$store.dispatch('send_new_gcbm_job_title')
    }
  }
}
</script>
