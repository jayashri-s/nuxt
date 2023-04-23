<template>
  <div
    class="flex flex-col flex-grow pt-2 overflow-y-auto bg-white border-r border-gray-200"
  >
    <div class="flex items-center ml-4 flex-shrink-0">
      <svg
        class="svg-icon"
        style="
          width: 50px;
          height: 50px;
          vertical-align: middle;
          fill: currentColor;
          overflow: hidden;
        "
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M507.904 264.192c73.728 0 133.12 59.392 133.12 133.12v33.792c-44.032-5.12-89.088-7.168-133.12-7.168-44.032 0-89.088 2.048-133.12 7.168v-33.792c0-72.704 59.392-133.12 133.12-133.12z m241.664 389.12l13.312-116.736c29.696 5.12 52.224 29.696 52.224 57.344 0 32.768-29.696 59.392-65.536 59.392z m-484.352 0c-35.84 0-65.536-26.624-65.536-59.392 0-28.672 22.528-52.224 52.224-57.344l13.312 116.736z m438.272-193.536c-67.584-7.168-132.096-10.24-194.56-10.24s-128 3.072-194.56 10.24c-22.528 2.048-38.912 22.528-35.84 44.032l20.48 198.656c2.048 18.432 16.384 33.792 35.84 35.84 57.344 7.168 115.712 10.24 175.104 10.24s117.76-3.072 175.104-10.24c18.432-2.048 33.792-17.408 35.84-35.84l20.48-198.656c0-22.528-15.36-41.984-37.888-44.032zM395.264 640c-16.384 0-28.672-16.384-28.672-37.888s13.312-37.888 28.672-37.888 28.672 16.384 28.672 37.888-12.288 37.888-28.672 37.888z m171.008 41.984c0 2.048-1.024 4.096-2.048 5.12-1.024 1.024-3.072 2.048-5.12 2.048h-101.376c-2.048 0-4.096-1.024-5.12-2.048-1.024-1.024-2.048-3.072-2.048-5.12v-18.432c0-4.096 3.072-7.168 7.168-7.168h2.048c4.096 0 7.168 3.072 7.168 7.168v9.216h82.944v-9.216c0-4.096 3.072-7.168 7.168-7.168h2.048c4.096 0 7.168 3.072 7.168 7.168v18.432z m54.272-41.984c-16.384 0-28.672-16.384-28.672-37.888s13.312-37.888 28.672-37.888 28.672 16.384 28.672 37.888-12.288 37.888-28.672 37.888z"
        />
      </svg>
      <span class="font-bold text-lg font-mono">Lead Bot</span>
    </div>
    <div class="mt-1">
      <div to="/index" @click="navigate('dashboard')">
        <div
          class="flex ml-2 mr-2 rounded-md cursor-pointer"
          :class="{
            'font-inter text-sm  font-medium bg-blue-100   text-blue-700 w-fill align-self active':
              status == 'index',
            'text-gray-600 font-inter font-medium text-sm border-transparent':
              status != 'index',
          }"
        >
          <svg
            version="1.1"
            id="Layer_1"
            xmlns="http://www.w3.org/2000/svg"
            xmlns:xlink="http://www.w3.org/1999/xlink"
            x="0px"
            y="0px"
            width="122.88px"
            height="122.88px"
            viewBox="0 0 122.88 122.88"
            enable-background="new 0 0 122.88 122.88"
            xml:space="preserve"
          >
            <g>
              <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'index',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'index',
              }"
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M61.439,0c33.928,0,61.44,27.513,61.44,61.439c0,33.929-27.513,61.44-61.44,61.44 C27.512,122.88,0,95.368,0,61.439C0,27.513,27.512,0,61.439,0L61.439,0z M45.917,40.282l19.997,36.447 c1.326,1.263,2.336,2.896,2.846,4.796c1.475,5.502-1.791,11.159-7.293,12.634c-5.501,1.474-11.159-1.794-12.634-7.293 c-0.388-1.451-0.446-2.914-0.222-4.309L45.917,40.282L45.917,40.282z M112.652,64.89c0,4.503-3.653,8.156-8.154,8.156 c-4.504,0-8.158-3.653-8.158-8.156c0-4.502,3.654-8.155,8.158-8.155C108.999,56.734,112.652,60.388,112.652,64.89L112.652,64.89z M10.229,64.89c0,4.503,3.651,8.156,8.155,8.156c4.504,0,8.155-3.653,8.155-8.156c0-4.502-3.651-8.155-8.155-8.155 C13.881,56.734,10.229,60.388,10.229,64.89L10.229,64.89z M25.124,28.49c-3.184,3.184-3.184,8.35,0,11.534 c3.184,3.184,8.35,3.184,11.534,0c3.184-3.184,3.184-8.35,0-11.534C33.474,25.306,28.308,25.306,25.124,28.49L25.124,28.49z M61.485,13.285c4.504,0,8.154,3.651,8.154,8.155c0,4.501-3.65,8.155-8.154,8.155s-8.155-3.653-8.155-8.155 C53.331,16.936,56.981,13.282,61.485,13.285L61.485,13.285z M97.755,28.49c3.187,3.184,3.187,8.35,0.003,11.534 c-3.184,3.184-8.35,3.184-11.534,0c-3.186-3.184-3.186-8.35,0-11.534C89.408,25.306,94.574,25.306,97.755,28.49L97.755,28.49z"
              />
            </g>
          </svg>
          

          <div class="m-2 mt-3">Dashboard</div>
        </div>
      </div>

      <div @click="navigate('broadCast')">
        <div
          class="flex ml-2 mr-2 rounded-md cursor-pointer"
          :class="{
            'font-inter text-sm  font-medium bg-blue-100   text-blue-700 w-fill align-self active':
              status == 'broadCast',
            'text-gray-600 font-inter font-medium text-sm border-transparent':
              status != 'broadCast',
          }"
        >
          <svg
            class="mt-3.5 ml-3.5"
            width="20"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'broadCast',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'broadCast',
              }"
              d="M18.0505 8.69999L17.2338 12.1833C16.5338 15.1917 15.1505 16.4083 12.5505 16.1583C12.1338 16.125 11.6838 16.05 11.2005 15.9333L9.80048 15.6C6.32548 14.775 5.25048 13.0583 6.06714 9.57499L6.88381 6.08332C7.05048 5.37499 7.25048 4.75832 7.50048 4.24999C8.47548 2.23332 10.1338 1.69165 12.9171 2.34999L14.3088 2.67499C17.8005 3.49165 18.8671 5.21665 18.0505 8.69999Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'broadCast',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'broadCast',
              }"
              d="M12.5503 16.1583C12.0336 16.5083 11.3836 16.8 10.592 17.0583L9.27528 17.4917C5.96695 18.5583 4.22528 17.6667 3.15028 14.3583L2.08362 11.0667C1.01695 7.75833 1.90028 6.00833 5.20862 4.94167L6.52528 4.50833C6.86695 4.4 7.19195 4.30833 7.50028 4.25C7.25028 4.75833 7.05028 5.375 6.88362 6.08333L6.06695 9.575C5.25028 13.0583 6.32528 14.775 9.80028 15.6L11.2003 15.9333C11.6836 16.05 12.1336 16.125 12.5503 16.1583Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'broadCast',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'broadCast',
              }"
              d="M10.5332 7.10834L14.5749 8.13334"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'broadCast',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'broadCast',
              }"
              d="M9.7168 10.3333L12.1335 10.95"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>

          <div class="m-2 mt-3">broadCast</div>
        </div>
      </div>

      <div @click="navigate('teamChat')">
        <div
          class="flex ml-2 mr-2 rounded-md cursor-pointer"
          :class="{
            'font-inter stroke-blue-900 text-sm   font-medium  bg-blue-100 text-blue-700 w-fill align-self active':
              status == 'teamChat',
            'text-gray-600 font-inter font-medium text-sm border-transparent':
              status != 'teamChat',
          }"
        >
          <svg
            width="20"
            :class="{
              ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                status == 'teamChat',
              'text-gray-600 font-inter font-medium text-sm border-transparent':
                status != 'teamChat',
            }"
            class="mt-3.5 ml-3.5"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'teamChat',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'teamChat',
              }"
              d="M15 5.96669C14.95 5.95836 14.8917 5.95836 14.8417 5.96669C13.6917 5.92502 12.775 4.98336 12.775 3.81669C12.775 2.62502 13.7334 1.66669 14.925 1.66669C16.1167 1.66669 17.075 2.63336 17.075 3.81669C17.0667 4.98336 16.15 5.92502 15 5.96669Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'teamChat',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'teamChat',
              }"
              d="M14.1417 12.0334C15.2834 12.225 16.5417 12.025 17.425 11.4334C18.6 10.65 18.6 9.3667 17.425 8.58337C16.5334 7.9917 15.2584 7.79169 14.1167 7.99169"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'teamChat',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'teamChat',
              }"
              d="M4.9749 5.96669C5.0249 5.95836 5.08324 5.95836 5.13324 5.96669C6.28324 5.92502 7.1999 4.98336 7.1999 3.81669C7.1999 2.62502 6.24157 1.66669 5.0499 1.66669C3.85824 1.66669 2.8999 2.63336 2.8999 3.81669C2.90824 4.98336 3.8249 5.92502 4.9749 5.96669Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'teamChat',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'teamChat',
              }"
              d="M5.83328 12.0334C4.69162 12.225 3.43328 12.025 2.54995 11.4334C1.37495 10.65 1.37495 9.3667 2.54995 8.58337C3.44162 7.9917 4.71662 7.79169 5.85828 7.99169"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'teamChat',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'teamChat',
              }"
              d="M10 12.1917C9.95002 12.1833 9.89169 12.1833 9.84169 12.1917C8.69169 12.15 7.77502 11.2083 7.77502 10.0417C7.77502 8.85 8.73336 7.89166 9.92502 7.89166C11.1167 7.89166 12.075 8.85833 12.075 10.0417C12.0667 11.2083 11.15 12.1583 10 12.1917Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'teamChat',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'teamChat',
              }"
              d="M7.57498 14.8167C6.39998 15.6 6.39998 16.8833 7.57498 17.6667C8.90831 18.5583 11.0916 18.5583 12.425 17.6667C13.6 16.8833 13.6 15.6 12.425 14.8167C11.1 13.9333 8.90831 13.9333 7.57498 14.8167Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>

          <div class="m-2 mt-3">Team Chat</div>
        </div>
      </div>

      <div to="/dummy" @click="navigate('analytics')">
        <div
          class="flex ml-2 mr-2 rounded-md cursor-pointer"
          :class="{
            'font-inter text-sm  font-medium bg-blue-100   text-blue-700 w-fill align-self active':
              status == 'analytics',
            'text-gray-600 font-inter font-medium text-sm border-transparent':
              status != 'analytics',
          }"
        >
          <svg
            class="mt-3 ml-3.5"
            width="20"
            height="20"
            viewBox="0 0 20 20"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'analytics',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'analytics',
              }"
              d="M2.5 18.3333H17.5"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'analytics',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'analytics',
              }"
              d="M4.66665 6.98334H3.33333C2.875 6.98334 2.5 7.35834 2.5 7.81667V15C2.5 15.4583 2.875 15.8333 3.33333 15.8333H4.66665C5.12498 15.8333 5.49998 15.4583 5.49998 15V7.81667C5.49998 7.35834 5.12498 6.98334 4.66665 6.98334Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'analytics',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'analytics',
              }"
              d="M10.6666 4.32501H9.33333C8.875 4.32501 8.5 4.70001 8.5 5.15835V15C8.5 15.4583 8.875 15.8333 9.33333 15.8333H10.6666C11.125 15.8333 11.5 15.4583 11.5 15V5.15835C11.5 4.70001 11.125 4.32501 10.6666 4.32501Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
            <path
              :class="{
                ' bg-blue-100  stroke-blue-700 w-fill align-self active':
                  status == 'analytics',
                'text-gray-600 font-inter font-medium text-sm border-transparent':
                  status != 'analytics',
              }"
              d="M16.6666 1.66669H15.3333C14.875 1.66669 14.5 2.04169 14.5 2.50002V15C14.5 15.4584 14.875 15.8334 15.3333 15.8334H16.6666C17.125 15.8334 17.5 15.4584 17.5 15V2.50002C17.5 2.04169 17.125 1.66669 16.6666 1.66669Z"
              stroke="#4B5563"
              stroke-width="1.5"
              stroke-linecap="round"
              stroke-linejoin="round"
            />
          </svg>

          <div class="m-2 mt-3">Analytics</div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      status: this.$route.name,

      isLoading: true,
    };
  },

  mounted() {
    console.log(this.$route.name);
  },
  methods: {
    navigate(status) {
      this.status = status;
      this.isLoading = false;
      if (this.status == "dashboard") {
        navigateTo("/");
      }
      if (this.status == "broadCast") {
        navigateTo("/broadCast");
      }
      if (this.status == "teamChat") {
        navigateTo("/teamChat");
      }
      if (this.status == "analytics") {
        navigateTo("/analytics");
      }
    },
  },
};
</script>
