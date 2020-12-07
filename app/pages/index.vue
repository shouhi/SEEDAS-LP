<template>
  <div>
    <my-home />
    <my-header />
    <my-about />
    <my-StrongPoint />
    <my-numbers />
    <my-process />
    <my-services />
    <my-testimonials />
    <my-clients />
    <my-works />
    <my-contact />
    <my-footer />
  </div>
</template>

<script>
import myHome from '~/components/SHome'
import myHeader from '~/components/SHeader'
import myAbout from '~/components/SAbout'
import myStrongPoint from '~/components/SStrongPoint'
import myNumbers from '~/components/SNumbers'
import myWorks from '~/components/SWorks'
import myProcess from '~/components/SProcess'
import myServices from '~/components/SServices'
import myClients from '~/components/SClients'
import myTestimonials from '~/components/STestimonials'
import myContact from '~/components/SContact'
import myFooter from '~/components/SFooter'

export default {
  components: {
    myHeader,
    myHome,
    myAbout,
    myStrongPoint,
    myNumbers,
    myWorks,
    myProcess,
    myServices,
    myTestimonials,
    myClients,
    myContact,
    myFooter
  }
}
</script>
