<template>
  <div class="card">
    <div class="card-body">
      <table class="table table-condensed table-hover table-bordered table-striped" id="items">
        <thead>
          <tr>
            <th>Imagen</th>
            <th>Codigo</th>
            <th>Nombre del producto</th>
            <th>Precios</th>
            <th>Cantidad</th>
            <th>Categoria</th>
            <th>Fabricante</th>
            <th>Estado</th>
            <th>Opciones</th>
          </tr>
        </thead>
      </table>
    </div>
    <!-- /.card-body -->
  </div>
  <!-- /.card -->

  <!-------------------------------------Remove Product ------------------------------------------->
  <div class="modal fade" tabindex="-1" role="dialog" id="removeProductModal">
    <div class="modal-dialog">
      <div class="modal-content">
        <div class="modal-header">
          <h4 class="modal-title"><i class="bx bx-cube"></i> Eliminar producto</h4>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">×</span>
          </button>
        </div>
        <div class="modal-body">
          <form action="" method="POST">
            <p id="message">¿Realmente deseas eliminar el producto? Se movera a la palera</p>
            <input type="hidden" name="identifier" id="identifier" />
            <div class="modal-footer">
              <button type="button" class="btn btn-default" data-dismiss="modal">
                <i class="bx bx-times"></i> Cancelar
              </button>
              <button
                type="submit"
                class="btn btn-primary"
                id="removeProductBtn"
                data-loading-text="Loading..."
              >
                <i class="bx bx-trash"></i> Eliminar
              </button>
            </div>
          </form>
        </div>
      </div>
      <!-- /.modal-content -->
    </div>
    <!-- /.modal-dialog -->
  </div>
  <!-- /.modal -->
</template>
