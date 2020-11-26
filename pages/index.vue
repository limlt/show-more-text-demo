<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-card>
        <v-card-text>
          <show-more-text
            :text="txtString"
            :lines="4"
            additional-container-css="margin:14px;"
            additional-content-css="font-size:16px;"
            additional-content-expanded-css="font-size:16px;"
            additional-anchor-css="font-size: 16px;"
            @click="change"
          />
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import showMoreText from 'show-more-text'
export default {
  components: {
    showMoreText,
  },
  data() {
    return {
      txtString: `Note: This property was originally implemented in WebKit and has some issues. It got standardized for legacy support. The CSS Overflow Module Level 3 specification also defines a line-clamp property, which is meant to replace this property and avoid its issues.`,
    }
  },
  methods: {
    change(showAll) {
      console.log(showAll)
    },
  },
}
</script>
