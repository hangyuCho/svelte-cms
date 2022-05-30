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
      마호샵 관리자화면
    </ListItem>
    <Divider />
    <List>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiViewDashboard} />
        </span>
        내 쇼핑몰 정보
      </ListItem>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiAccountBox} />
        </span>
        간단 등록
      </ListItem>
      <ListItem>
        <span slot="prepend">
          <Icon path={mdiGavel} />
        </span>
        상품목록
      </ListItem>
    </List>
    <span slot="append" class="pa-2">
      <Button block>Logout</Button>
    </span>
  </NavigationDrawer>
</div>
</MaterialApp>
