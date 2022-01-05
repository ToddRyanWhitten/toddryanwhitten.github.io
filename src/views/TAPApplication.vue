<template>
    <div>
        <form @submit.prevent="createApplication">

            <BaseInput
            label="KSU ID"
            v-model="application.ksuid"
            type="text"
            />

            <BaseInput
            label="Employee ID"
            v-model="application.employeeid"
            type="text"
            />

            <BaseInput
            label="First Name"
            v-model="application.firstName"
            type="text"
            />

            <BaseInput
            label="Middle Name"
            v-model="application.middleName"
            type="text"
            />

            <BaseInput
            label="Last Name"
            v-model="application.lastName"
            type="text"
            />

            <BaseInput
            label="EMail"
            v-model="application.emailAddress"
            type="text"
            />

            <BaseInput
            label="Phone"
            v-model="application.phone"
            type="text"
            />

            <label>Home Institution</label>
            <select v-model="application.homeInstitution">
                <option
                v-for="option in homeInstitutions"
                :value="option"
                :key="option"
                :selected="option === application.homeInstitution"
                >{{ option }}</option>
            </select>
            <div>
              <BaseButton
                type="submit"
                class="-fill-gradient"
                something="else">
                Submit
              </BaseButton>
            </div>
        </form>
    </div>
</template>
<script>
export default {
  data () {
    return {
      homeInstitutions: [
        'Kennesaw State University'
      ],
      application: {
        ksuid: '',
        employeeid: '',
        firstName: '',
        middleName: '',
        lastName: '',
        emailAddress: '',
        phone: '',
        homeInstitution: '',
        jobTitle: '',
        degreeSeeking: '',
        degreeProgram: '',
        areaOfDiscipline: '',
        academicTermYear: '',
        lastTermAttended: '',
        teachingInstitution1: '',
        teachingInstitution1Id: '',
        teachingInstitution2: '',
        teachingInstitution2Id: ''
      }
    }
  },
  methods: {
    createApplication () {
      // console.log('submit')
      alert(this.application.ksuid)
      console.log(this.application)
    }
  }
}
</script>
