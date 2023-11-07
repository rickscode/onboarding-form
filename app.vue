<script setup>

function handleSubmit(data) {
  console.log(data);
}

</script>

<template>
  <FormKit type="form" :actions="false" @submit="handleSubmit">
    <FormKit type="multi-step" tab-style="progress" :hide-progress-labels="true">
      <FormKit type="step" name="personalInfo">
        <FormKit 
          type="text"
          name="firstname"
          label="First Name"
          placeholder="first name"
          prefix-icon="avatarMan"
          validation="required|length:2" />
          
          <FormKit 
          type="text"
          name="lastname"
          label="Last Name"
          placeholder="last name"
          prefix-icon="avatarMan"
          validation="required|length:2" />
          
          <FormKit 
          type="email"
          name="useremail"
          label="Email Address"
          placeholder="example@mail.com"
          prefix-icon="email"
          validation="required|email" />
          
          <FormKit 
          type="tel"
          name="phone"
          label="Phone Number"
          placeholder="7424949049"
          prefix-icon="telephone"
          />
        <!-- <StepOne /> -->
      </FormKit>

      <FormKit type="step" name="BusinessDetails">
        <FormKit 
          type="text"
          name="businessname"
          label="Registered Business Name"
          placeholder="ABC LTD"
          prefix-icon=""
          validation="required|length:3" />

          <FormKit 
          type="text"
          name="region"
          label="Registered Region"
          placeholder="EU, UK, Other Specify"
          prefix-icon=""
          validation="required|length:2" />

          <FormKit 
          type="text"
          name="businesswebsite"
          label="Website Address"
          placeholder="www.example.com"
          prefix-icon=""
          validation="required|length:6" />

          <FormKit 
          type="text"
          name="companyemail"
          label="Company Email"
          placeholder="email@company.com"
          prefix-icon=""
          validation="required|email" />

          <FormKit 
          type="tel"
          name="companyphone"
          label="Company Phone Number"
          placeholder="77777777"
          prefix-icon="telephone"
          validation="required"
          />

          <FormKit 
          type="select"
          name="employeenumbers"
          label="Number Of Employees"
          :options="[
            '0-10',
            '11-50',
            '51-100',
            '101-200+',
            ]"
          validation="required"
          />

          <FormKit 
          type="text"
          name="businessmodel"
          label="Describe Your Business Model"
          placeholder="Accounting Consulting"
          prefix-icon=""
          validation="required" />

          <FormKit 
          type="text"
          name="businesscategory"
          label="Business Category"
          placeholder="Financial Services"
          prefix-icon=""
          validation="required" />

          <FormKit 
          type="text"
          name="cryptosubcategory"
          label="Sub-Category For Crypto"
          placeholder="Gaming"
          prefix-icon=""
          validation="required" />
          
        
      
        <!-- <StepTwo /> -->
      </FormKit>

      <FormKit type="step" name="BusinessDetailsContinued">
      
      <!-- <StepTwo /> -->
      </FormKit>

      <FormKit type="step" name="Directors">
        
        <!-- <StepTwo /> -->
      </FormKit>

      <FormKit type="step" name="Shareholders">
        
        <!-- <StepTwo /> -->
      </FormKit>

      <FormKit type="step" name="Final Business Details">
        <!-- component for example brevity. -->
        <!-- <StepThree /> -->

        <!-- using step slot for submit button-->
        <template #stepNext>
          <FormKit type="submit" />
        </template>
      </FormKit>
    </FormKit>
  </FormKit>
</template>
