<template>
      <b-col md="3" align-v="center">
        <b-card 
        :title="job.name"
        img-src="https://picsum.photos/600/300"
        img-alt="Job-Info"
        img-top
        tag="article"
        style="max-width: 20rem"
        class="mb-2"
        footer="Card footer">

          <b-card-text>
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium quibusdam eaque, laudantium amet impedit non officiis doloremque ipsam esse, cupiditate id aliquid rerum quia quas consectetur iusto dolore a soluta.
          </b-card-text>

          <b-button 
            v-b-tooltip.hover 
            title="Tooltip content" 
            v-b-modal="modalId" 
            variant="primary">
              Apply
          </b-button>

          <b-modal :id="modalId" title="BootstrapVue">
            <p class="my-4">Hello from {{job.name}}!</p>
          </b-modal>
        </b-card>
      </b-col>
</template>

<script>
export default {
  props: ['job'],
  computed: {
    modalId() {
      return `modal-${this.job.id}`;
    }
  }
}
</script>

<style>

</style>