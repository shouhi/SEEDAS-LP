<template>
  <div>
    <my-home />
    <my-header />
    <my-about />
    <my-StrongPoint />
    <my-numbers />
    <to-owners />
    <my-services />
    <my-clients />
    <my-works />
    <my-visions />
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
import toOwners from '~/components/SToOwners'
import myServices from '~/components/SServices'
import myClients from '~/components/SClients'
import myVisions from '~/components/SVisions'
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
    toOwners,
    myServices,
    myVisions,
    myClients,
    myContact,
    myFooter
  }
}
</script>
