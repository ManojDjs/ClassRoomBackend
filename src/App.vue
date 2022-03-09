<template>
<div class="app">
  <Menubar :model="items">
    <template #start>
        <Avatar label="CB" class='p-avatar-lg' />
    </template>
    <template #end>
         <Avatar icon="pi pi-power-off"  class='p-avatar-lg' />
    </template>
</Menubar>

  <div id="nav">
  
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
  </div>
  <router-view/>
</div>  
</template>

<script>
export default{
name: 'App',
data() {
        return {
            items: [
                  {
                   label:'Home',
                   icon:'pi pi-fw pi-home',
                   },
                {
                   label:'News',
                   icon:'pi pi-fw pi-paperclip',
                  
                },
                {
                   label:'Module',
                   icon:'pi pi-fw pi-server',
                   },
                {
                   label:'Profile',
                   icon:'pi pi-fw pi-user',
                },
                
             ]
        }
    }

}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
