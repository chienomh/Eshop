<template>
    <div class="main-form">
        <div class="form">
            <div class="form-title">
                <span class="title">Thêm mới cửa hàng</span>
                <span class="close-form">x</span>
            </div>
            <div class="content-form">
                <div class="shop-code style-margin">
                    <div class="style-input">
                        <span class="label">Mã cửa hàng <span class="required"> *</span></span>
                    </div>
                    <input type="text" id="shop-code">
                </div>
                <div class="shop-name style-margin">
                    <div class="style-input">
                        <span class="label">Tên cửa hàng <span class="required"> *</span></span>
                    </div>
                    <input type="text" id="shop-name">
                </div>
                <div class="shop-address style-margin">
                    <div class="style-input">
                        <span class="label">Địa chỉ <span class="required"> *</span></span>
                    </div>
                    <input type="text" id="shop-address">
                </div>
                <div class="phone-number style-margin" style="margin-right: 20px">
                     <div class="style-input">
                        <span class="label">Số điện thoại</span>
                    </div>
                    <input type="text" id="phone-number" class="style-input-small">
                </div>
                <div class="tax-code style-margin">
                     <div class="style-input">
                        <span class="label">Mã số thuế</span>
                    </div>
                    <input type="text" id="tax-code" class="style-input-small">
                </div>
                <div class="mation style-margin" style="float: none;"> 
                     <div class="style-input">
                        <span class="label">Quốc gia</span>
                    </div>
                    <select name="nation" id="nation"  class="style-input-small">
                        <option value="1">Việt Nam</option>
                    </select>
                </div>
                <div class="thanh-pho style-margin" style="margin-right: 20px">
                     <div class="style-input">
                        <span class="label">Tỉnh/Thành phố</span>
                    </div>
                    <select name="nation" id="nation"  class="style-input-small"> 
                    </select>
                </div>
                <div class="huyen style-margin">
                     <div class="style-input">
                        <span class="label">Quận/Huyện</span>
                    </div>
                    <select name="nation" id="nation"  class="style-input-small"> 
                    </select>
                </div>
                <div class="xa style-margin" style="margin-right: 20px">
                     <div class="style-input">
                        <span class="label">Phường/Xã</span>
                    </div>
                    <select name="nation" id="nation"  class="style-input-small"> 
                    </select>
                </div>
                <div class="pho style-margin">
                     <div class="style-input">
                        <span class="label">Đường phố</span>
                    </div>
                    <input type="text" class="style-input-small"> 
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
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
        height: 480px;
        background-color: #FFFFFF;
        margin: auto
    }

    .form-title {
        width: 100%;
        height: 40px;
        background-color: #f0f0f0;
        position: relative;
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

    .style-input-small {
        width: 167px;
        height: 32px;
    }

    .style-margin {
        margin-bottom: 8px;
        float: left;
    }

    .required {
        color: red;
    }

    #shop-code,#shop-name{
        width: 460px;
        height: 32px;
    }

    #shop-address{
        width: 460px;
        height: 80px;
    }

</style>