<template>
  <div class="container-md d-flex flex-column align-items-center justify-content-center p-0" style="margin: 0 auto;">
    <HeaderComponent />
    <HeroComponent />
    <SecondSectionComponent />
    <DestinationsComponent />
    <VacationPlansContainer />
    <CommentsSectionComponent />
    <BlogsComponent />
    <FooterComponent />
  </div>
</template>

<script>
// @ is an alias to /src
import HeaderComponent from '@/components/HeaderComponent.vue';
import HeroComponent from '@/components/HeroComponent.vue'
import SecondSectionComponent from '@/components/SecondSectionComponent.vue'
import DestinationsComponent from '@/components/DestinationsComponent.vue'
import VacationPlansContainer from '@/components/VacationPlansContainer.vue';
import CommentsSectionComponent from '@/components/CommentsSectionComponent.vue';
import BlogsComponent from '@/components/BlogsComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue';

export default {
  name: 'HomeView',
  components: {
    HeaderComponent,
    HeroComponent,
    SecondSectionComponent,
    DestinationsComponent,
    VacationPlansContainer,
    CommentsSectionComponent,
    BlogsComponent,
    FooterComponent
  }
}
</script>
