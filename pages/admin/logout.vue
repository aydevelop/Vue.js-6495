<template>
    <div>
        logout .....
    </div>
</template>

<script>
export default {
    layout: 'admin',
    middleware: ['admin-auth'],
    beforeCreate(){
        this.$store.dispatch('auth/logout');
        this.$router.push('/admin/login?msg=logout');
    }
}
</script>