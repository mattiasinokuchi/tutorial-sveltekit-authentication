<script context="module">
  //  protecting page /admin
  export async function load({ page, session }) {
    if (page.path==='/admin' && session.user === "") {
      return { redirect: "/", status: 302 };
    }
    return { props: {} };

  }
</script>

<slot />
