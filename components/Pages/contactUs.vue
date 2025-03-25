<!-- <template>
    <div class="py-1 w-[95%] h-[90%] relative ">

        <div class="bg-white rounded-3xl w-full">
            <div class="flex flex-col  gap-10 md:flex-row m-[3%]  items-center">
                <div class="w-full md:w-[60%]">
                 <div class="mb-2 text-left">
                        <h2 class="text-3xl md:text-5xl lg:text-6xl  font-serif mb-3">Let's Partner Together</h2>
                        <p class="text-lg md:text-xl font-normal  leading-relaxed">
                            If you’d like to partner together, please fill in your contact details below and one of our
                            team
                            will reach out.
                        </p>
                    </div>

          
                    <div class="mb-1">
                        <h3 class="text-2xl lg:text-4xl font-bold mb-4">Company Details</h3>
                        <table class="w-full text-left border-collapse  border border-gray-300 ">
                            <tbody class="w-full">
                                <tr class="border-b">
                                    <td class="py-2 pr-4 font-medium border-r border-gray-300  p-2">Email</td>
                                    <td class="py-2 p-2">
                                        <a href="mailto:info@apxzone.com"
                                            class="text-blue-500 hover:underline">info@apxzone.com</a>
                                    </td>
                                </tr>
                                <tr class="border-b ">
                                    <td class="py-2 pr-4 border-r border-gray-300 font-medium p-2">Phone</td>
                                    <td class="py-2 p-2">
                                        <a href="tel:+61862452320" class="text-blue-500 hover:underline">+61 8 6245
                                            2320</a>
                                    </td>
                                </tr>
                                <tr class="border-b">
                                    <td class="py-2 pr-4 font-medium border-r border-gray-300 p-2">Address</td>
                                    <td class="py-2 p-2">
                                        <div>
                                            <strong>Pakistan:</strong> Deans Trade Cetre Peshawar, Office 762,
                                            Pakistan
                                            <br>
                                            <strong>UAE:</strong> Silicon Oasis, DDP, Building A1, Dubai, United Arab
                                            Emirates
                                        </div>
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>

                    <div>
                        <form class="space-y-3 ">
                            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                                <input class="p-4 bg-white border rounded-3xl outline-none" placeholder="Name"
                                    type="text">
                                <input class="p-4  border  outline-none rounded-3xl" placeholder="Email" type="email">
                            </div>
                            <textarea class="p-3 rounded-3xl outline-none border w-full"
                                placeholder="Your Message"></textarea>
                            <button type="submit"
                                class="bg-blue-500 text-white py-3 px-6 w-[80%] rounded-2xl hover:bg-blue-600">Send
                                Message</button>
                        </form>
                    </div>
                </div>

                <div class="w-full mt-5 md:w-[40%] shadow-2xl rounded-2xl ">
                    <swiper :slides-per-view="1" :space-between="30" :loop="true" :pagination="{ clickable: true }"
                        :navigation="false" :modules="modules" :grab-cursor="true" class="mySwiper">
                        <swiper-slide v-for="(item, index) in items" :key="index">
                            <div class="bg-white p-6 rounded-lg  flex flex-col">
                                <div class="flex gap-4">
                                    <img :src="item.img" alt="Profile Image" class="w-24 h-24 rounded-full mb-4" />
                                    <div class="">
                                        <h1 class="text-xl md:text-2xl lg:text-4xl font-semibold mb-1">{{ item.name }}
                                        </h1>
                                        <h2 class="text-lg md:text-xl  text-gray-500">{{ item.role }}</h2>
                                    </div>
                                </div>
                                <p class="text-gray-700 mt-4">{{ item.description }}</p>
                            </div>
                        </swiper-slide>
                    </swiper>
                </div>

            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/navigation';
import { Pagination, Navigation } from 'swiper/modules';

const items = ref([
    { img: 'https://i.pinimg.com/564x/b6/be/ff/b6beff8f5ebe84c8e0d8511b669e6316.jpg', role: "Team Lead", name: 'Waqar Khan', description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi ullam ad delectus neque quod vitae amet exercitationem consequatur, provident suscipit, facere, similique optio.ctus neque quod vitae amet exercitationem consequatur, provident suscipit, facere, similique optio' },
    { img: 'https://i.pinimg.com/564x/b6/be/ff/b6beff8f5ebe84c8e0d8511b669e6316.jpg', role: "Prodect manager", name: 'John Doe', description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi ullam ad delectus neque quod vitae amet exercitationem consequatur, provident suscipit, facere, similique optio.ctus neque quod vitae amet exercitationem consequatur, provident suscipit, facere, similique optio' },
    { img: 'https://i.pinimg.com/564x/b6/be/ff/b6beff8f5ebe84c8e0d8511b669e6316.jpg', role: "Ui Developer", name: 'Jane Smith', description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quasi ullam ad delectus neque quod vitae amet exercitationem consequatur, provident suscipit, facere, similique optio.ctus neque quod vitae amet exercitationem consequatur, provident suscipit, facere, similique optio' }
]);


</script>

<style scoped>
.mySwiper {
    width: 100%;
    height: 100%;
}
</style> -->

<!-- <template>
    <div class="relative w-full min-h-screen p-8 bg-gray-100 overflow-hidden flex items-center justify-center">
      <span class="absolute w-[500px] h-[500px] rounded-full bg-gradient-to-b from-[#1cd4af] to-[#159b80] bottom-[50%] right-[40%] transform translate-x-[-40%] translate-y-[38%]"></span>
      <img class="absolute h-[400px] top-1/2 left-1/2 transform translate-x-[181%] translate-y-[11%] opacity-20" alt="" />
      <div class="relative w-full max-w-[920px] bg-white rounded-xl shadow-lg grid grid-cols-2 overflow-hidden z-50">
        <div class="relative p-9 bg-[#196BA2]">
          <span class="absolute w-[130px] h-[130px] rounded-full bg-gradient-to-tr from-transparent to-[#196BA2] top-[130px] right-[-40px]"></span>
          <span class="absolute w-[80px] h-[80px] rounded-full bg-gradient-to-tr from-transparent to-[#196BA2] top-[10px] right-[30px]"></span>
          <span class="absolute w-6 h-6 bg-[#1abc9c] transform rotate-45 top-[50px] left-[-13px]"></span>
          <h3 class="text-white font-medium text-2xl leading-[2] mb-3">Let's get in touch</h3>
          <p class="text-gray-300 mb-6">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Saepe dolorum
            adipisci recusandae praesentium dicta!
          </p>
  
          <div class="space-y-3">
            <div class="flex items-center space-x-3 text-gray-300 text-sm">
              <i class="fas fa-map-marker-alt text-[#1ABC9C]"></i>
              <p>92 Cherry Drive Uniondale, NY 11553</p>
            </div>
            <div class="flex items-center space-x-3 text-gray-300 text-sm">
              <i class="fas fa-envelope text-[#1ABC9C]"></i>
              <p>lorem@ipsum.com</p>
            </div>
            <div class="flex items-center space-x-3 text-gray-300 text-sm">
              <i class="fas fa-phone text-[#1ABC9C]"></i>
              <p>123-456-789</p>
            </div>
          </div>
  
          <div class="mt-8">
            <p class="text-gray-300">Connect with us :</p>
            <div class="flex space-x-2 mt-2">
              <a href="#" class="w-9 h-9 rounded-lg bg-gradient-to-tr from-[#1abc9c] to-[#149279] text-white flex items-center justify-center transform transition-transform hover:scale-105"><i class="fab fa-facebook-f"></i></a>
              <a href="#" class="w-9 h-9 rounded-lg bg-gradient-to-tr from-[#1abc9c] to-[#149279] text-white flex items-center justify-center transform transition-transform hover:scale-105"><i class="fab fa-twitter"></i></a>
              <a href="#" class="w-9 h-9 rounded-lg bg-gradient-to-tr from-[#1abc9c] to-[#149279] text-white flex items-center justify-center transform transition-transform hover:scale-105"><i class="fab fa-instagram"></i></a>
              <a href="#" class="w-9 h-9 rounded-lg bg-gradient-to-tr from-[#1abc9c] to-[#149279] text-white flex items-center justify-center transform transition-transform hover:scale-105"><i class="fab fa-linkedin-in"></i></a>
            </div>
          </div>
        </div>
  
        <div class="relative p-9 bg-[#196BA2]">
          <span class="absolute w-[130px] h-[130px] rounded-full bg-gradient-to-tr from-transparent to-[#196BA2] top-[130px] right-[-40px]"></span>
          <span class="absolute w-[80px] h-[80px] rounded-full bg-gradient-to-tr from-transparent to-[#196BA2] top-[10px] right-[30px]"></span>
          <span class="absolute w-6 h-6 bg-[#1abc9c] transform rotate-45 top-[50px] left-[-13px]"></span>
          
          <form @submit.prevent="handleSubmit" autocomplete="off" class="relative z-10 space-y-6">
            <h3 class="text-white font-medium text-2xl leading-[2] mb-3">Contact us</h3>
            <div v-for="input in inputs" :key="input.name" class="relative">
              <input
                :type="input.type"
                :name="input.name"
                class="w-full outline-none border-2 border-gray-100 bg-transparent py-2 px-4 text-white font-medium text-sm tracking-wider rounded-lg transition-all duration-300"
                v-model="formData[input.name]"
                @focus="focusFunc"
                @blur="blurFunc"
              />
              <label :for="input.name" class="absolute top-1/2 left-4 transform -translate-y-1/2 px-1 text-gray-100 text-sm transition-all duration-500">{{ input.label }}</label>
              <span class="absolute top-0 left-4 transform -translate-y-1/2 text-transparent text-sm px-1 pointer-events-none z-0">
                <span class="absolute w-1/2 h-1 bg-[#196BA2] opacity-0 transition-all duration-300"></span>
                <span class="absolute w-1/2 h-1 bg-[#196BA2] opacity-0 transition-all duration-300"></span>
              </span>
            </div>
            <input type="submit" value="Send" class="w-full py-2 bg-white border-2 border-gray-100 text-[#1abc9c] text-sm rounded-lg cursor-pointer transition-all duration-300 hover:bg-transparent hover:text-white" />
          </form>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref, onMounted } from 'vue';
  
  const formData = ref({
    name: '',
    email: '',
    phone: '',
    message: '',
  });
  
  const inputs = [
    { name: 'name', type: 'text', label: 'Username' },
    { name: 'email', type: 'email', label: 'Email' },
    { name: 'phone', type: 'tel', label: 'Phone' },
    { name: 'message', type: 'textarea', label: 'Message' },
  ];
  
  const focusFunc = (event) => {
    const parent = event.target.parentNode;
    parent.classList.add('focus');
  };
  
  const blurFunc = (event) => {
    const parent = event.target.parentNode;
    if (event.target.value === '') {
      parent.classList.remove('focus');
    }
  };
  
  onMounted(() => {
    const inputs = document.querySelectorAll('.input');
    inputs.forEach((input) => {
      input.addEventListener('focus', focusFunc);
      input.addEventListener('blur', blurFunc);
    });
  });
  
  const handleSubmit = () => {
    console.log('Form submitted:', formData.value);
  };
  </script>
  
  <style scoped>
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800&display=swap");
  
  body, input, textarea {
    font-family: "Poppins", sans-serif;
  }
  
  @media (max-width: 850px) {
    .form {
      grid-template-columns: 1fr;
    }
    .contact-info:before {
      bottom: initial;
      top: -75px;
      right: 65px;
      transform: scale(0.95);
    }
    .contact-form:before {
      top: -13px;
      left: initial;
      right: 70px;
    }
    .square {
      transform: translate(140%, 43%);
      height: 350px;
    }
    .big-circle {
      bottom: 75%;
      transform: scale(0.9) translate(-40%, 30%);
      right: 50%;
    }
    .text {
      margin: 1rem 0 1.5rem 0;
    }
    .social-media {
      padding: 1.5rem 0 0 0;
    }
  }
  
  @media (max-width: 480px) {
    .container {
      padding: 1.5rem;
    }
    .contact-info:before {
      display: none;
    }
    .square, .big-circle {
      display: none;
    }
    form, .contact-info {
      padding: 1.7rem 1.6rem;
    }
    .text, .information, .social-media p {
      font-size: 0.8rem;
    }
    .title {
      font-size: 1.15rem;
    }
    .social-icons a {
      width: 30px;
      height: 30px;
      line-height: 30px;
    }
    .icon {
      width: 23px;
    }
    .input {
      padding: 0.45rem 1.2rem;
      font-size: 0.8rem;
    }
  }
  </style>
   -->
   <template>
    <div class="container scale-y-[0.88] scale-x-95">
      <span class="big-circle"></span>
      <img  class="square" alt="" />
      <div class="form">
        <div class="contact-info">
          <h3 class="title">Let's get in touch</h3>
          <p class="text">
           Many are Called ,Few are Choosen
          </p>
          <div class="info">
            <div class="information">
              <i class="fas fa-map-marker-alt"></i> &nbsp
              <p>Deans Trade Centre</p>
            </div>
            <div class="information">
              <i class="fas fa-envelope"></i> &nbsp &nbsp
              <p>apxzone@org.com</p>
            </div>
            <div class="information">
              <i class="fas fa-phone"></i>&nbsp&nbsp
              <p>123-456-789</p>
            </div>
          </div>
          <div class="social-media">
            <p>Connect with us :</p>
            <div class="social-icons">
              <a href="#"><i class="fab fa-facebook-f"></i></a>
              <a href="#"><i class="fab fa-twitter"></i></a>
              <a href="#"><i class="fab fa-instagram"></i></a>
              <a href="#"><i class="fab fa-linkedin-in"></i></a>
            </div>
          </div>
        </div>
        <div class="contact-form ">
          <span class="circle one"></span>
          <span class="circle two"></span>
          <form @submit.prevent="handleSubmit" autocomplete="off">
            <h3 class="title">Contact us</h3>
            <div class="input-container" v-for="input in inputs" :key="input.name">
              <input
                :type="input.type"
                :name="input.name"
                class="input"
                v-model="formData[input.name]"
                @focus="focusFunc"
                @blur="blurFunc"
              />
              <label :for="input.name">{{ input.label }}</label>
              <span>{{ input.label }}</span>
            </div>
            <input type="submit" value="Send" class="btn" />
          </form>
        </div>
      </div>
    </div>
  </template>
  <script setup>
  import { ref, onMounted } from 'vue';
  const formData = ref({
    name: '',
    email: '',
    phone: '',
    message: '',
  });
  const inputs = [
    { name: 'name', type: 'text', label: 'Username' },
    { name: 'email', type: 'email', label: 'Email' },
    { name: 'phone', type: 'tel', label: 'Phone' },
    { name: 'message', type: 'textarea', label: 'Message' },
  ];
  const focusFunc = (event) => {
    const parent = event.target.parentNode;
    parent.classList.add('focus');
  };
  const blurFunc = (event) => {
    const parent = event.target.parentNode;
    if (event.target.value === '') {
      parent.classList.remove('focus');
    }
  };
  onMounted(() => {
    const inputs = document.querySelectorAll('.input');
    inputs.forEach((input) => {
      input.addEventListener('focus', focusFunc);
      input.addEventListener('blur', blurFunc);
    });
  });
  const handleSubmit = () => {
    console.log('Form submitted:', formData.value);
  };
  </script>
  <style scoped>
  /* Add your existing CSS styles here */
  @import url("https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body,
input,
textarea {
  font-family: "Poppins", sans-serif;
}
.container {
  position: relative;
  width: 100%;
  min-height: 100vh;
  padding: 2rem;
  background-color: #FAFAFA;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 30px;
}
.form {
  width: 100%;
  max-width: 920px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 20px 1px rgba(0, 0, 0, 0.1);
  z-index: 1000;
  overflow: hidden;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}
.contact-form {
  background-color: #1878B9;
  position: relative;
}
.circle {
  border-radius: 50%;
  background: linear-gradient(135deg, transparent 20%, #1878B9);
  position: absolute;
}
.circle.one {
  width: 130px;
  height: 130px;
  top: 130px;
  right: -40px;
}
.circle.two {
  width: 80px;
  height: 80px;
  top: 10px;
  right: 30px;
}
.contact-form:before {
  content: "";
  position: absolute;
  width: 26px;
  height: 26px;
  background-color: #1ABC9C;
  transform: rotate(45deg);
  top: 50px;
  left: -13px;
}
form {
  padding: 2.3rem 2.2rem;
  z-index: 10;
  overflow: hidden;
  position: relative;
}
.title {
  color: #fff;
  font-weight: 500;
  font-size: 1.5rem;
  line-height: 2;
  margin-bottom: 0.7rem;
}
.input-container {
  position: relative;
  margin: 1.5rem 0;
}
.input {
  width: 100%;
  outline: none;
  border: 2px solid #FAFAFA;
  background: none;
  padding: 0.6rem 1.2rem;
  color: #fff;
  font-weight: 500;
  font-size: 0.95rem;
  letter-spacing: 0.5px;
  border-radius: 5px;
  transition: 0.3s;
}
textarea.input {
  padding: 0.8rem 1.2rem;
  min-height: 150px;
  border-radius: 5px;
  resize: none;
  overflow-y: auto;
}
.input-container label {
  position: absolute;
  top: 50%;
  left: 15px;
  transform: translateY(-50%);
  padding: 0 0.4rem;
  color: #FAFAFA;
  font-size: 0.9rem;
  font-weight: 400;
  pointer-events: none;
  z-index: 1000;
  transition: 0.5s;
}
.input-container.textarea label {
  top: 1rem;
  transform: translateY(0);
}
.btn {
  padding: 0.6rem 1.3rem;
  background-color: #fff;
  border: 2px solid #FAFAFA;
  font-size: 0.95rem;
  color: #1878B9;
  line-height: 1;
  border-radius: 5px;
  outline: none;
  cursor: pointer;
  transition: 0.3s;
  margin: 0;
  width: 100%;
}
.btn:hover {
  background-color: transparent;
  color: #fff;
}
.input-container span {
  position: absolute;
  top: 0;
  left: 25px;
  transform: translateY(-50%);
  font-size: 0.8rem;
  padding: 0 0.4rem;
  color: transparent;
  pointer-events: none;
  z-index: 500;
}
.input-container span:before,
.input-container span:after {
  content: "";
  position: absolute;
  width: 10%;
  opacity: 0;
  transition: 0.3s;
  height: 5px;
  background-color: #196BA2;
  top: 50%;
  transform: translateY(-50%);
}
.input-container span:before {
  left: 50%;
}
.input-container span:after {
  right: 50%;
}
.input-container.focus label {
  top: 0;
  transform: translateY(-50%);
  left: 25px;
  font-size: 0.8rem;
}
.input-container.focus span:before,
.input-container.focus span:after {
  width: 50%;
  opacity: 1;
}
.contact-info {
  padding: 2.3rem 2.2rem;
  position: relative;
}
.contact-info .title {
  color: #1878B9;
}
.text {
  color: #333;
  margin: 1.5rem 0 2rem 0;
}
.information {
  display: flex;
  color: #555;
  margin: 0.7rem 0;
  align-items: center;
  font-size: 0.95rem;
}
.information i {
  color: #1ABC9C;
}
.icon {
  width: 28px;
  margin-right: 0.7rem;
}
.social-media {
  padding: 2rem 0 0 0;
}
.social-media p {
  color: #333;
}
.social-icons {
  display: flex;
  margin-top: 0.5rem;
}
.social-icons a {
  width: 35px;
  height: 35px;
  border-radius: 5px;
  background: linear-gradient(45deg, #1878B9, #149279);
  color: #fff;
  text-align: center;
  line-height: 35px;
  margin-right: 0.5rem;
  transition: 0.3s;
}
.social-icons a:hover {
  transform: scale(1.05);
}
.contact-info:before {
  content: "";
  position: absolute;
  width: 110px;
  height: 100px;
  border: 22px solid #1ABC9C;
  border-radius: 50%;
  bottom: -77px;
  right: 50px;
  opacity: 0.3;
}
.big-circle {
  position: absolute;
  width: 500px;
  height: 500px;
  border-radius: 50%;
  background: linear-gradient(to bottom, #1878B9, #159B80);
  bottom: 40%;
  right: 40%;
  transform: translate(-40%, 38%);
}
.big-circle:after {
  content: "";
  position: absolute;
  width: 360px;
  height: 360px;
  background-color: #FAFAFA;
  border-radius: 50%;
  top: calc(50% - 180px);
  left: calc(50% - 180px);
}
.square {
  position: absolute;
  height: 400px;
  top: 50%;
  left: 50%;
  transform: translate(181%, 11%);
  opacity: 0.2;
}
@media (max-width: 850px) {
  .form {
    grid-template-columns: 1fr;
  }
  .contact-info:before {
    bottom: initial;
    top: -75px;
    right: 65px;
    transform: scale(0.95);
  }
  .contact-form:before {
    top: -13px;
    left: initial;
    right: 70px;
  }
  .square {
    transform: translate(140%, 43%);
    height: 350px;
  }
  .big-circle {
    bottom: 75%;
    transform: scale(0.9) translate(-40%, 30%);
    right: 50%;
  }
  .text {
    margin: 1rem 0 1.5rem 0;
  }
  .social-media {
    padding: 1.5rem 0 0 0;
  }
}
@media (max-width: 480px) {
  .container {
    padding: 1.5rem;
  }
  .contact-info:before {
    display: none;
  }
  .square,
  .big-circle {
    display: none;
  }
  form,
  .contact-info {
    padding: 1.7rem 1.6rem;
  }
  .text,
  .information,
  .social-media p {
    font-size: 0.8rem;
  }
  .title {
    font-size: 1.15rem;
  }
  .social-icons a {
    width: 30px;
    height: 30px;
    line-height: 30px;
  }
  .icon {
    width: 23px;
  }
  .input {
    padding: 0.45rem 1.2rem;
  }
  .btn {
    padding: 0.45rem 1.2rem;
  }
}
  </style>