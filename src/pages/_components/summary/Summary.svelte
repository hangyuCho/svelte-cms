<script>
    import {
        MaterialApp, 
        DataTable, 
        DataTableHead, 
        DataTableRow, 
        DataTableCell, 
        DataTableBody
    } from 'svelte-materialify'
</script>
<style lang="scss" src="./Summary.scss" Global>
</style>

<div class="summary">summary</div>
<MaterialApp>
    <DataTable class="datatable">
      <DataTableHead>
        <DataTableRow>
          <DataTableCell>Dessert</DataTableCell>
          <DataTableCell numeric>Carbs (g)</DataTableCell>
          <DataTableCell numeric>Protein (g)</DataTableCell>
          <DataTableCell>Comments</DataTableCell>
        </DataTableRow>
      </DataTableHead>
      <DataTableBody>
        <DataTableRow>
          <DataTableCell>Frozen yogurt</DataTableCell>
          <DataTableCell numeric>24</DataTableCell>
          <DataTableCell numeric>4.0</DataTableCell>
          <DataTableCell>Super tasty</DataTableCell>
        </DataTableRow>
      </DataTableBody>
    </DataTable>
</MaterialApp>