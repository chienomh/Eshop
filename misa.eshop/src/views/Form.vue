<template>
  <div class="main-form">
    <div class="form">
      <div class="form-title">
        <span class="title">Thêm mới cửa hàng</span>
        <span class="close-form" @click="closeForm">x</span>
      </div>
      <div class="content-form">
        <div class="shop-code style-margin">
          <div class="style-input">
            <span class="label"
              >Mã cửa hàng <span class="required"> *</span></span
            >
          </div>
          <input type="text" id="shop-code" class="style-boder" v-focus />
        </div>
        <div class="shop-name style-margin">
          <div class="style-input">
            <span class="label"
              >Tên cửa hàng <span class="required"> *</span></span
            >
          </div>
          <input type="text" id="shop-name" class="style-boder" />
        </div>
        <div class="shop-address style-margin">
          <div class="style-input">
            <span class="label">Địa chỉ <span class="required"> *</span></span>
          </div>
          <textarea
            type="text"
            id="shop-address"
            class="style-boder"
            style="resize: none"
          ></textarea>
        </div>
        <div class="phone-number style-margin" style="margin-right: 20px">
          <div class="style-input">
            <span class="label">Số điện thoại</span>
          </div>
          <input
            type="text"
            id="phone-number"
            class="style-input-small style-boder"
          />
        </div>
        <div class="tax-code style-margin">
          <div class="style-input">
            <span class="label">Mã số thuế</span>
          </div>
          <input
            type="text"
            id="tax-code"
            class="style-input-small style-boder"
          />
        </div>
        <div class="mation style-margin" style="float: none">
          <div class="style-input">
            <span class="label">Quốc gia</span>
          </div>
          <select
            name="nation"
            id="nation"
            class="style-input-small style-boder"
          >
            <option value="0"></option>
            <option value="1">Việt Nam</option>
          </select>
        </div>
        <div class="thanh-pho style-margin" style="margin-right: 20px">
          <div class="style-input">
            <span class="label">Tỉnh/Thành phố</span>
          </div>
          <select
            name="nation"
            id="nation"
            class="style-input-small style-boder"
          ></select>
        </div>
        <div class="huyen style-margin">
          <div class="style-input">
            <span class="label">Quận/Huyện</span>
          </div>
          <select
            name="nation"
            id="nation"
            class="style-input-small style-boder"
          ></select>
        </div>
        <div class="xa style-margin" style="margin-right: 20px">
          <div class="style-input">
            <span class="label">Phường/Xã</span>
          </div>
          <select
            name="nation"
            id="nation"
            class="style-input-small style-boder"
          ></select>
        </div>
        <div class="pho style-margin">
          <div class="style-input">
            <span class="label">Đường phố</span>
          </div>
          <input type="text" class="style-input-small style-boder" />
        </div>
      </div>
      <div class="footer-form">
        <div class="help">
          <span class="icon-help">
            <img src="../assets/icon/help.png" alt="" />
          </span>
          <span> Trợ giúp </span>
        </div>

        <div class="footer-active">
          <button class="luu">Lưu</button>
          <button class="luu_va_them_moi">Lưu và thêm mới</button>
          <button class="huy_bo" @click="closeForm">Hủy bỏ</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  focus: {
    inserted: function (el) {
      el.focus();
    },
  },

  methods: {

    // Nhờ cha đóng fomr
    closeForm() {
        this.$emit("closeFormNow")
    },
  },

  data() {
    return {
     
    };
  },
};
</script>

<style scoped>
.main-form {
  width: 100%;
  height: 100vh;
  background-color: rgba(0, 0, 0, 0.4);
  display: flex;
}

.form {
  width: 600px;
  height: 470px;
  background-color: #ffffff;
  margin: auto;
}

.form-title {
  width: 100%;
  height: 40px;
  background-color: #f0f0f0;
  position: relative;
  /* position: absolute; */
}

.form-title .title {
  font-family: Text-Bold;
  font-size: 16px;
  line-height: 40px;
  padding: 10px 14px;
}

.form-title .close-form {
  position: absolute;
  right: 13px;
  font-size: 25px;
  color: #8f8f8f;
  cursor: pointer;
}

.content-form {
  width: 100%;
  height: 365px;
  border-bottom: 1px solid #f0f0f0;
  padding: 20px 16px 0;
  font-weight: 200px;
}

.style-input {
  width: 105px;
  float: left;
  line-height: 32px;
}

input,
textarea {
  border: none;
  outline: none;
}

input:focus {
  border: 1px solid #026b98;
}

textarea:focus {
  border: 1px solid #026b98;
}

.style-input-small {
  width: 167px;
  height: 32px;
}

.style-margin {
  margin-bottom: 8px;
  float: left;
}

.style-boder {
  border: 1px solid #d0d0d0;
}

.required {
  color: red;
}

#shop-code,
#shop-name {
  width: 460px;
  height: 32px;
}

#shop-address {
  width: 460px;
  height: 80px;
}

.footer-form {
  margin: auto;
  margin-top: 15px;
  display: flex;
  position: relative;
}

.help {
  width: 95px;
  height: 35px;
  color: #00577b;
  font-weight: 700;
  line-height: 35px;
  text-align: center;
}

.help .icon-help {
  margin-top: 5px;
}

.footer-active {
  position: absolute;
  right: 8px;
}

.footer-active .luu {
  height: 35px;
  width: 65px;
  font-family: Text-Bold;
  padding: 5px 30px;
  background-image: url("../assets/icon/save-white.png");
  background-repeat: no-repeat;
  background-size: 14px;
  background-position: 19% 50%;
  background-color: #026b98;
  color: #ffffff;
  border: none;
  border-radius: 3px;
  margin-right: 8px;
  cursor: pointer;
}

.footer-active .luu:hover {
  background-color: #0088c2;
}

.footer-active .luu_va_them_moi {
  width: 140px;
  height: 35px;
  background-color: #ffffff;
  border-radius: 3px;
  border: 1px solid #026b98;
  color: #026b98;
  padding-left: 15px;
  background-image: url("../assets/icon/add-blue.png");
  background-repeat: no-repeat;
  background-size: 14px;
  background-position: 7% 50%;
  margin-right: 8px;
  cursor: pointer;
}

.footer-active .luu_va_them_moi:hover {
  color: #9e9e9e;
}

.footer-active .huy_bo {
  width: 80px;
  height: 35px;
  border: 1px solid #ffffff;
  background-color: #ffffff;
  color: #026b98;
  background-image: url("../assets/icon/cance-whtie.png");
  background-repeat: no-repeat;
  background-size: 14px;
  background-position: 7% 50%;
  cursor: pointer;
  padding-left: 15px;
}

.footer-active .huy_bo:hover {
  border: 1px solid #026b98;
  border-radius: 3px;
}
</style>