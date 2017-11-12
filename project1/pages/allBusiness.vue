<template>
    <div id="wholePage">
        <script src="https://use.fontawesome.com/c17a47c7ea.js"></script>
        <div id="indexbody">
            
            <br/><br/><br/><br/><br/><br/><br/>
            <b-container id="topTitle">
                <b-row>
                    <b-col cols="1"></b-col>
                    <b-col cols="5">
                        <br/>
                        <p id="allBusinessTitle">  业务领域</p>
                    </b-col>
                    <b-col>
                        <template>
                            <b-form-group
                            id="fieldset1"
                            label="搜索相关业务"
                            :feedback="feedback" 
                            :state="state"
                            >
                            <b-form-input id="input1" :state="state" v-model.trim="name"></b-form-input>
                            </b-form-group>
                        </template>
                    </b-col>
                    <b-col></b-col>
                </b-row>
            </b-container>

            <hr id="hr1">
            <div id="allBusinesDetail">
            <b-container class="bodyText">
                <b-row>
                    <b-col>
                        <tempalte v-for="ele in title1" :key="ele.id">
                        <b-btn variant="link" id="subtitleText">{{ele}} <i class="fa fa-angle-right" aria-hidden="true"></i></b-btn>
                        <div id="leftDetail">
                            <br/>
                            <ul>
                                <li>细则1</li>
                                <li>细则2</li>
                            </ul>
                        </div>
                        <hr id="leftHr">
                        </tempalte>
                    </b-col>
                    <b-col>
                        <tempalte v-for="ele in title2" :key="ele.id">
                        <b-btn variant="link" id="subtitleText">{{ele}} <i class="fa fa-angle-right" aria-hidden="true"></i></b-btn>
                        <div id="leftDetail">
                            <br/>
                            <ul>
                                <li>细则1</li>
                                <li>细则2</li>
                                <li>细则3</li>
                            </ul>
                        </div>
                        <hr id="leftHr">
                        </tempalte>
                    </b-col>
                </b-row>
            </b-container>
            </div>
            <br/>
            <hr id="hr1">

        </div>

    </div>
  
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  data () {
    return {
      infoP: '  Q Z  & W D (JIANG XI)   L A W    F I R M',
      logoURL: require('~/assets/logo.jpg'),
      wxImg: require('~/assets/wx.jpeg'),
      title1: ['知识产权', '银行与融资', '仲裁', '竞争,贸易与监管', '房地产'],
      title2: ['破产重组', '私募股权', '争议解决与诉讼', '税务', '证券'],
      name: ''
    }
  },

  components: {
    Logo
  },

  methods: {

  },

  computed: {
    randomNumber: function () {
      return Math.random() * 4 + 1
    },
    feedback: function () {
      return this.name.length > 0 ? 'Enter at least 4 characters' : 'Please enter something'
    },
    state: function () {
      return this.name.length > 4 ? 'valid' : 'invalid'
    }
  }
}
</script>

<style scoped>
#leftHr {
    border-width: 3px;
}

#rightHr {
    border-width: 3px;
}

#subtitleText {
    font-size: 24px;
}

#subtitleText:hover {
    cursor: pointer;
}

#allBusinesDetail {
    margin-left: 200px;
    margin-right: 200px;
}

#topTitle {
    
}

#allBusinessTitle {
    font-size: 40px;
    white-space: pre;
}

#hr1 {
    margin-left: 200px;
    margin-right: 200px;
    border-width: 3px;
    margin-top: 0px;
}

.bodyText {
    color: gray;
}

#wholePage {
    background-color: rgb(250, 250, 250);
}

#buttons {
    color: white;
    cursor: pointer;
    text-decoration: none;
}

#buttons:hover {
    color: rgb(6, 132, 228);
}
</style>
