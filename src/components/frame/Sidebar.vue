<template>
  <sidebar-menu :menu="menu" />
</template>
 
 <script>
 import AUTH from 'services/auth'
    export default {
        data() {
            return {
                auth: AUTH,
                menu: [
                    {
                        header: true,
                        title: 'Main Navigation',
                        hiddenOnCollapse: true,
                    
                    },
                    {
                        href: '/dashboard',
                        title: 'Dashboard',
                        icon: 'fa fa-user'
                    },
                    {
                        href: '/personalinformation',
                        title: 'Personal Information',
                        icon: 'fa fa-user',
                    },
                    {
                        href: '/courses',
                        title: 'Add Course & Subjects',
                        icon: 'fa fa-book',
                    },
                    {
                        href: '/confirmLogout',
                        title: 'Log Out',
                        icon: 'fa fa-user',
                    }
                ]
            }
        },
        methods:{
            // onToggleCollapse(collapsed) {},
            // onItemClick(event, item) {}
        }
    }
</script> 
   