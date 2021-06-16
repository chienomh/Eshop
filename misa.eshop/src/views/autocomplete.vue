<template>
    <div class="autocomplete">
       <div class="input-search">
            <input type="text"  @keyup="getValue">
            <div class="keydown" @click="isShow">x</div>
       </div>
       <div class="wrapper" v-if="isShowList">
           <div class="list"
                v-for="(item, index) in this.searched" :key="index"
                @click="selectOption"
            >
                {{item}}
            </div>
       </div>
       
    </div>
</template>

<script>
export default {

    data() {
        return {
            customers : [
                'Tạ Đức Chiến',
                'Cao Thế Thắng',
                'Nguyễn Văn Thàng',
                'Nguyễn Đức Thành',
                'Tạ Nhật Anh'
            ],
            isShowList : false,
            searched: [],
        }
    },

    methods: {
        getValue(e) {
            let dataInput = e.target.value;
            this.searched = [],
            this.searched = this.customers.filter(x => x.indexOf(dataInput) > -1)
            if (this.searched)
                this.isShowList = true;
            else this.isShowList = false;
        },

        isShow(){
            this.searched = this.customers
            this.isShowList = !this.isShowList
        },

        selectOption(e){
            let t = e.target;
            console.log(t)
            this.isShowList = false;
        }
    }
}
</script>

<style scoped>
    .autocomplete {
        width: 100%;
        height: 100vh;
        background-color: rgb(56, 79, 87);
    }

    .input-search{
        display: flex;
    }

    .input-search input{
        width: 137px;
        height: 32px;
    }

    .input-search .keydown {
        border: 1px solid #d0d0d0;
        width: 30px;
        background-color: white;
        cursor: pointer;
    }

    .list {
        background-color: white;
        width: 137px;
        cursor: pointer;
        height: 32px;
        line-height: 37px;
    }

    .list:hover {
        background-color: wheat;
    }
</style>