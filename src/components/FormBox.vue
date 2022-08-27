<template>

   <form class="contact-form row">
      <div class="message">
      <span v-if="error" class="text-danger">{{ msg }}</span>
      <span v-else class="text-success">{{ msg }}</span></div>
      <div class="form-field col-lg-6">
         <input id="name" class="input-text js-input" type="text" placeholder="Name" required>
         
      </div>
      <div class="form-field col-lg-6 ">
         <input id="email" class="input-text js-input" type="email" @blur="checkEmail" placeholder="Email" required>
      </div>
      <div class="form-field col-lg-6 ">
         <input id="phone" class="input-text js-input" type="text" placeholder="Phone" @blur="checkPhone">
         
      </div>
      <div class="form-field col-lg-6 ">
         <input id="subject" class="input-text js-input" type="text" placeholder="Subject" required>
         
      </div>
      <div class="form-field col-lg-12">
         <input id="message" class="input-text js-input" placeholder="Message" type="text">
      </div>
      <div class="form-field col-lg-12">
         <input class="submit-btn" type="submit" value="Submit">
      </div>
   </form>
</template>

<script>
export default {
   name: 'FormBox',
   props: {
      txt: String
   },
   data: function() {
      return {
         error: true,
         msg: ''
      }
   },
   methods: {
      checkEmail: function (value) {
         if (/^[a-zA-Z0-9.! #$%&'*+/=? ^_`{|}~-]+@[a-zA-Z0-9-]+(?:\. [a-zA-Z0-9-]+)*$/.test(value)) {
            this.error = false;
            this.msg = "Email address OK"
         } else {
            this.error = true;
            this.msg = 'Please enter a valid email address';
         }
      },
      checkPhone: function(value) {
         if (value ==="hi" || /^(\+\d{1,2}\s?)?1?-?\.?\s?\(?\d{3}\)?[\s.-]?\d{3}[\s.-]?\d{4}$/.test(value)) {
            this.error = false;
            this.msg = "Phone No. OK"
         } else {
            this.error = true;
            this.msg = 'Please enter a valid Phone No.';
         }
      }
      
   }
}

</script>

<style scoped>
.contact-form .form-field {
   position: relative;
   margin: 32px 0;
}

.contact-form .input-text {
   display: block;
   width: 100%;
   height: 36px;
   border-width: 0 0 2px 0;
   border-color: #01CB63;
   font-size: 18px;
   line-height: 26px;
   font-weight: 400;
}





.contact-form .label {
   position: absolute;
   left: 20px;
   bottom: 11px;
   font-size: 18px;
   line-height: 26px;
   font-weight: 400;
   color: var(--bs-secondary);
   cursor: text;
   
}

.contact-form .submit-btn {
   display: inline-block;
   background-color: #000;
   background-image: #01CB63;
   color: #fff;
   text-transform: uppercase;
   letter-spacing: 2px;
   font-size: 16px;
   padding: 8px 16px;
   border: none;
   width: 200px;
   cursor: pointer;
}
</style>