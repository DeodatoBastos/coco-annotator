<script>
import button from "@/mixins/toolBar/button";

export default {
  name: "ValidationButton",
  mixins: [button],
  props: {
    verified: {
      type: Boolean,
      required: true,
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
      this.$parent.image.isverified = !this.verified;
      this.$parent.save()
    },
  },
};
</script>
