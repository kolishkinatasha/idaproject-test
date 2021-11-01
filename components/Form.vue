<template>
    <form class='sidebar-wrapper' 
    @submit.prevent="someAction()">        
        <div class='sidebar-item'>
            <label class='sidebar-label'>Наименование товара</label>
            <div class='label__important'></div>
            <input class='sidebar-input'
            placeholder='Введите наименование товара'
            v-model="title"
            type="text"
            @blur="isTitleTouched = true"
            :class="{ error: isTitleError }"
            />
            <div v-if="isTitleError" class='error-mes'>
                Поле является обязательным
            </div>
        </div>
        <div class='sidebar-item'>
            <label  class='sidebar-label'>Описание товара</label>
            <textarea class='sidebar-input sidebar-input__long' placeholder='Введите описание товара'/>
        </div>
        <div class='sidebar-item'>
            <label  class='sidebar-label'>Ссылка на изображение товара</label>
            <div class='label__important'></div>
            <input class='sidebar-input' 
            placeholder='Введите ссылку'
            v-model="link"
            type="text"
            @blur="isLinkTouched = true"
            :class="{ error: isLinkError }"/>
            <div v-if="isLinkError" class='error-mes'>
                Поле является обязательным
            </div>
        </div>
        <div class='sidebar-item'>
            <label  class='sidebar-label'>Цена товара</label>
            <div class='label__important'></div>
            <input class='sidebar-input' 
            placeholder='Введите цену'
            v-model="price"
            type="text"
            @blur="isPriceTouched = true"
            :class="{ error: isPriceError }"/>
            <div v-if="isPriceError" class='error-mes'>
                Поле является обязательным
            </div>
        </div>
        
        <button type="submit" :disabled="!isTitleValid || !isLinkValid || !isPriceValid" class='sidebar-btn'>Добавить товар</button>
    </form>
</template>

<script>
const checkRegex = /^\s*$/;

export default {

  data() {
    return {
      title: '',
      link: '',
      price: '',
      isTitleTouched: false,
      isLinkTouched: false,
      isPriceTouched: false,
    };
  },

  computed: {
    isTitleValid() {
      return !checkRegex.test(this.title);
    },
    isTitleError() {
      return !this.isTitleValid && this.isTitleTouched;
    },

    isLinkValid() {
      return !checkRegex.test(this.link);
    },

    isLinkError() {
      return !this.isLinkValid && this.isLinkTouched;
    },

    isPriceValid() {
      return !checkRegex.test(this.price);
    },

    isPriceError() {
      return !this.isPriceValid && this.isPriceTouched;
    },
  },
  methods: {
    someAction() {
      if (!this.isTitleValid && !this.isLinkValid && !this.isPriceValid) {
        return;
      }

      alert("Форма отправлена");
    }
  }
};
</script>


<style lang='scss'>
@import url('https://fonts.googleapis.com/css?family=Source+Sans+Pro');

.sidebar-wrapper {
    width: 284px;

    padding: 24px;
    margin-top: 16px;
    margin-left: 32px;
    text-align: center;

    background: #FFFEFB;
    box-shadow: 0px 20px 30px rgba(0, 0, 0, 0.04), 0px 6px 10px rgba(0, 0, 0, 0.02);
    border-radius: 4px;
}

.sidebar-item {
    display: flex;
    flex-wrap: wrap;
    padding: 0;
    margin: 0 auto;
}

.sidebar-label {
    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: normal;
    font-size: 10px;
    line-height: 13px;
    letter-spacing: -0.02em;
    color: #49485E;
}

.label__important {
    width: 4px;
    height: 4px;
    left: 151px;
    top: 107px;

    background: #FF8484;
    border-radius: 50%;
}

.sidebar-input {
    width: 100%;
    height: 34px;
    border: none;
    padding-left: 16px;
    margin: 4px 0px 16px 0px;

    background: #FFFEFB;
    box-shadow: 0px 2px 5px rgba(0, 0, 0, 0.1);
    border-radius: 4px;

    ::placeholder {
    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 15px;

    margin-top: 10px;

    text-align: left;
    color: #B4B4B4;
    }
}

.sidebar-input__long {
    height: 108px;
    resize: none;
    padding-top: 10px;
}

input, textarea:focus {
    outline:none;
}

.sidebar-btn{
    width: 100%;
    height: 36px;
    border: none;
    border-radius: 10px;

    font-family: Inter;
    font-style: normal;
    font-weight: 600;
    font-size: 12px;
    line-height: 15px;
    text-align: center;
    letter-spacing: -0.02em;

    background: #7BAE73;
    color: white;   
}

button:disabled {
    background: #EEEEEE;
    color: #B4B4B4;
}

.error-mes{
    margin-bottom: 10px;
    font-family: Source Sans Pro;
    font-style: normal;
    font-weight: normal;
    font-size: 10px;
    line-height: 13px;
    letter-spacing: -0.02em;
    color: #FF8484;
}

.error{
    border: 1px solid #FF8484;
    margin-bottom: 5px;
}

// button:disabled {
//     background: #7BAE73;
//     color: white;
// }
</style>
