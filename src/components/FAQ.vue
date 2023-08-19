<template>
    <div class="flex p-10 flex-col md:flex-row faq">
      
        <div class="md:w-6/12 w-full">
            <div  v-for="(q, index) in faqs" :key="index" @click="showRes(index)" class="hover:cursor-pointer">
                <div class="flex justify-between focus:text-white py-6">
                    <h1 class="text-xl">{{q.q}}</h1>
                    <img :src=" q.active ? '../../public/chevron-up.svg' : '../../public/chevron-down.svg' " class="w-6" alt="">
                </div>
                <hr>
                <h3 v-show="q.active">{{ q.r }}</h3>
            </div>
        </div>

        <div class="md:w-6/12 w-full">

          <div className="flex flex-col text-center w-full mb-6">
            <h1 className="sm:text-3xl text-2xl font-medium title-font mb-4 text-gray-900">
              Contact Us
            </h1>
            <p className="lg:w-2/3 mx-auto leading-relaxed text-base">
                Cant find an answer for your questions? Contact Us
            </p>
          </div>
          <div className="lg:w-1/2 md:w-2/3 mx-auto">
            <div className="flex flex-wrap -m-2">
              <div className="p-2 w-1/2">
                <div className="relative">
                  <label for="name" className="leading-7 text-sm text-gray-600">
                    Name
                  </label>
                  <input
                    type="text"
                    id="name"
                    name="name"
                    className="w-full bg-gray-100 rounded border border-gray-300 focus:border-indigo-500 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out"
                  />
                </div>
              </div>
              <div className="p-2 w-1/2">
                <div className="relative">
                  <label
                    for="email"
                    className="leading-7 text-sm text-gray-600"
                  >
                    Email
                  </label>
                  <input
                    type="email"
                    id="email"
                    name="email"
                    className="w-full bg-gray-100 rounded border border-gray-300 focus:border-indigo-500 text-base outline-none text-gray-700 py-1 px-3 leading-8 transition-colors duration-200 ease-in-out"
                  />
                </div>
              </div>
              <div className="p-2 w-full">
                <div className="relative">
                  <label
                    for="message"
                    className="leading-7 text-sm text-gray-600"
                  >
                    Message
                  </label>
                  <textarea
                    id="message"
                    name="message"
                    className="w-full bg-gray-100 rounded border border-gray-300 focus:border-indigo-500 h-32 text-base outline-none text-gray-700 py-1 px-3 resize-none leading-6 transition-colors duration-200 ease-in-out"
                  ></textarea>
                </div>
              </div>
              <div className="p-2 w-full">
                <button className="flex mx-auto text-white bg-cyan-500 border-0 py-2 px-8 focus:outline-none hover:bg-cyan-600 rounded text-lg">
                  Send
                </button>
              </div>
              
            </div>
          </div>




        </div>
    </div>

</template>

<script>
    export default {
        data() {
            return {
                faqs: [
                    {q: 'How Much is it',
                    r: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum ducimus perspiciatis aliquam magnam magni suscipit corrupti, itaque sunt voluptatibus officia similique voluptatum doloremque unde, numquam aperiam ex! Distinctio, possimus sapiente.',
                    active: false},
                    {q: 'How Much is it',
                    r: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum ducimus perspiciatis aliquam magnam magni suscipit corrupti, itaque sunt voluptatibus officia similique voluptatum doloremque unde, numquam aperiam ex! Distinctio, possimus sapiente.',
                    active: false},
                    {q: 'How Much is it',
                    r: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum ducimus perspiciatis aliquam magnam magni suscipit corrupti, itaque sunt voluptatibus officia similique voluptatum doloremque unde, numquam aperiam ex! Distinctio, possimus sapiente.',
                    active: false},
                    {q: 'How Much is it',
                    r: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum ducimus perspiciatis aliquam magnam magni suscipit corrupti, itaque sunt voluptatibus officia similique voluptatum doloremque unde, numquam aperiam ex! Distinctio, possimus sapiente.',
                    active: false},
            ]
            
        }
    },
    methods: {
        showRes(i) {
            this.faqs[i].active = !this.faqs[i].active
        }
    }
}
</script>

<style lang="scss" scoped>
  .faq {
    background-color: #F7F7F7;
  }
</style>