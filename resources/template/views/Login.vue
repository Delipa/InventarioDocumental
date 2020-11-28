<template class="fondo">
  <div class="row justify-content-center">
    <div class="col-lg-5 col-md-7">
      <div class="card bg-secondary shadow border-0">
        <!-- <div class="card-header bg-transparent pb-5">
                        <div class="text-muted text-center mt-2 mb-3"><small>Sign in with</small></div>
                        <div class="btn-wrapper text-center">
                            <a href="#" class="btn btn-neutral btn-icon">
                                <span class="btn-inner--icon"><img src="img/icons/common/github.svg"></span>
                                <span class="btn-inner--text">Github</span>
                            </a>
                            <a href="#" class="btn btn-neutral btn-icon">
                                <span class="btn-inner--icon"><img src="img/icons/common/google.svg"></span>
                                <span class="btn-inner--text">Google</span>
                            </a>
                        </div>
                    </div>-->
        <div class="card-body px-lg-5 py-lg-5">
          <div class="text-center text-muted mb-4">
            <small class= "letra">Iniciar sesión</small>
          </div>
          <form role="form">
            <base-input
              class="input-group-alternative mb-3"
              placeholder="Email"
              addon-left-icon="ni ni-email-83"
              v-model="model.email"
            >
            </base-input>

            <base-input
              class="input-group-alternative"
              placeholder="Password"
              type="password"
              addon-left-icon="ni ni-lock-circle-open"
              v-model="model.password"
            >
            </base-input>
            <div class="row mt-3">
              <div class="col-6">
                <a href="#" class="text-light"
                  ><small>Olvidó su contraseña</small></a
                >
              </div>
             <!-- <div class="col-6 text-right">
                <router-link to="/register" class="text-light"
                  ><small>Create new account</small></router-link
                >
              </div>-->
            </div>
            <!--<base-checkbox class="custom-control-alternative">
                                <span class="text-muted">Recordarme</span>
                            </base-checkbox>-->
            <div class="text-center">
              <base-button type="primary" class="my-4">Ingresar</base-button>
            </div>
          </form>
        </div>
      </div>
      <!--<div class="row mt-3">
        <div class="col-6">
          <a href="#" class="text-light"><small>Olvidó su contraseña</small></a>
        </div>
        <div class="col-6 text-right">
          <router-link to="/register" class="text-light"
            ><small>Create new account</small></router-link
          >
        </div>
      </div>-->
    </div>
  </div>
</template>
<script>
export default {
  name: "login",
  data() {
    return {
      model: {
        email: "",
        password: "",
      },
    };
  },
};
</script>
<style scoped>

.letra{
    color: #4E6470;
    font-size: large;
}
.card-body {
    background-color: #F7FAFC;
}
.my-4 {
  background-color: #8f141b;
}

.btn-primary {
  color: #dfd4a6;
  border-color: #8f141b;
}

.fondo {
  background-color: #8f141b;
}
</style>>

