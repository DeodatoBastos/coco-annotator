<script>
import button from "@/mixins/toolBar/button";

export default {
  name: "ValidationButton",
  mixins: [button],
  props: {
    verified: {
      type: Boolean,
      required: false,
    },
  },
  data() {
    return {
      name: "Validate Annotation",
      icon: "fa-check-square-o",
    };
  },
  methods: {
    execute() {
      this.$parent.verified = !this.verified;
      // this.$parent.verify();
    },
  },
};
</script>
