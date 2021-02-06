<template>
  <div class="content-header-left col-12">
    <div class="card">
        <div class="card-body">
            <div class="row breadcrumbs-top">
                <div class="col-6">
                    <h4 class="content-header-title float-left pr-1 mb-0">
                      <slot name="breadcrumb-title"></slot>
                    </h4>
                    <div class="breadcrumb-wrapper col-12">
                        <ol class="breadcrumb p-0 mb-0">
                          <li class="breadcrumb-item">
                            Aca falta hacer funcionar los breadcrumbs
                          </li>
                        </ol>
                    </div>
                </div>
                <div class="col-6">
                   <div class="float-right">
                     <slot name="tools"></slot>
                   </div>
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Breadcrumbs',
};
</script>
