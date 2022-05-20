<script>
  import { NavigationDrawer, List, ListItem, Button, Icon, MaterialApp, Avatar, Divider } from 'svelte-materialify';
  import { mdiViewDashboard, mdiAccountBox, mdiGavel } from '@mdi/js';
  let mini = true;
  function mouseenter() {
    mini = false;
  }
  function mouseleave() {
    mini = true;
  }
</script>

<MaterialApp>
  <div class="d-inline-block" on:mouseenter={mouseenter} on:mouseleave={mouseleave}>
    <NavigationDrawer absolute left {mini}>
    <ListItem>
      <span slot="prepend" class="ml-n2">
        <Avatar size={40}><img src="//picsum.photos/200" alt="profile" /></Avatar>
      </span>
      Mudit Somani
    </ListItem>
    <Divider />
    <List>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiViewDashboard} />
        </span>
        Dashboard
      </ListItem>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiAccountBox} />
        </span>
        Account
      </ListItem>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiGavel} />
        </span>
        Admin
      </ListItem>
    </List>
    <span slot="append" class="pa-2">
      <Button block>Logout</Button>
    </span>
  </NavigationDrawer>
</div>
</MaterialApp>
