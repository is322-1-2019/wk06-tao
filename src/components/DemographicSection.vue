<template>
<div>
  <form>
    <div class="form-row">
      <div class="form-group col-md-2">
        <label for="prefix">Prefix</label>
        <select id="prefix" class="form-control" v-model="demoInfo.prefix">
          <option selected>Not specified</option>
          <option>Mr</option>
          <option>Mrs</option>
          <option>Miss</option>
        </select>
      </div>
      <div class="form-group col-md-5">
        <label for="firstName">FirstName</label>
        <input type="text" v-model="demoInfo.firstName" class="form-control" id="firstName" placeholder="FirstName" />
      </div>
      <div class="form-group col-md-5">
        <label for="lastName">LastName</label>
        <input type="text" v-model="demoInfo.lastName" class="form-control" id="lastName" placeholder="LastName" />
      </div>
    </div>
    <div class="form-row">
      <div class="form-group col-md-2">
        <label for="sex">Sex</label>
        <select  v-model="demoInfo.sex" id="sex" class="form-control">
          <option selected>Not specified</option>
          <option>Male</option>
          <option>Female</option>
        </select>
      </div>
      <div class="form-group col-md-2">
        <label for="age">Age</label>
        <select  v-model="demoInfo.age" id="age" class="form-control">
          <option selected>Choose...</option>
          <option v-for="age in ageList"
            v-bind:key="age"
            v-bind:value="age"
            >{{ age }}</option>
        </select>
      </div>
      <div class="form-group col-md-8">
        <label for="occupation">Occupation</label>
        <input type="text" v-model="demoInfo.occupation" class="form-control" id="occupation" placeholder="Occupation" />
      </div>
    </div>
    <div class="form-group">
      <label for="address">Address</label>
      <input type="text" v-model="demoInfo.address" class="form-control" id="address" placeholder="1234 Main St" />
    </div>
    <div class="form-row">
      <div class="form-group col-md-6">
        <label for="district">District</label>
        <input type="text" v-model="demoInfo.district" class="form-control" id="district" />
      </div>
      <div class="form-group col-md-4">
        <label for="city">City</label>
        <select  v-model="demoInfo.city" id="age" class="form-control">
          <option selected>Choose...</option>
          <option v-for="city in cityList"
            v-bind:key="city.id"
            v-bind:value="city.name"
            >{{ city.name }}</option>
        </select>
      </div>
      <div class="form-group col-md-2">
        <label for="postcode">Postcode</label>
        <input type="text" v-model="demoInfo.postcode" class="form-control" id="postcode" />
      </div>
    </div>
  </form>
</div>
</template>

<script>
export default {
  data() {
    return {
      demoInfo : {
        prefix : '',
        firstName : '',
        lastName : '',
        sex : '',
        age : 1,
        address : '',
        district : '',
        city : '',
        postcode : '',
      },
      maxAge : 100,

      cityList : [
          {id: 1, name: "กระบี่"},
          {id: 2, name: "กรุงเทพมหานคร"},
          {id: 3, name: "กาญจนบุรี"},
          {id: 4, name: "กาฬสินธุ์"},
          {id: 5, name: "กำแพงเพชร"},
          {id: 6, name: "ขอนแก่น"},
          {id: 7, name: "จันทบุรี"},
          {id: 8, name: "ฉะเชิงเทรา"} ,
          {id: 9, name: "ชลบุรี"},
          {id: 10, name: "ชัยนาท"},
          {id: 11, name: "ชัยภูมิ"},
          {id: 12, name: "ชุมพร"},
          {id: 13, name: "เชียงราย"},
          {id: 14, name: "เชียงใหม่"},
          {id: 15, name: "ตรัง"},
          {id: 16, name: "ตราด"},
          {id: 17, name: "ตาก"},
          {id: 18, name: "นครนายก"},
          {id: 19, name: "นครปฐม"},
          {id: 20, name: "นครพนม"},
          {id: 21, name: "นครราชสีมา"} ,
          {id: 22, name: "นครศรีธรรมราช"},
          {id: 23, name: "นครสวรรค์"},
          {id: 24, name: "นนทบุรี"},
          {id: 25, name: "นราธิวาส"},
          {id: 26, name: "น่าน"},
          {id: 27, name: "บึงกาฬ"},
          {id: 28, name: "บุรีรัมย์"},
          {id: 29, name: "ปทุมธานี"},
          {id: 30, name: "ประจวบคีรีขันธ์"},
          {id: 31, name: "ปราจีนบุรี"},
          {id: 32, name: "ปัตตานี" },
          {id: 33, name: "พะเยา"},
          {id: 34, name: "พังงา"},
          {id: 35, name: "พัทลุง"},
          {id: 36, name: "พิจิตร"},
          {id: 37, name: "พิษณุโลก"},
          {id: 38, name: "เพชรบุรี"},
          {id: 39, name: "เพชรบูรณ์"},
          {id: 40, name: "แพร่"},
          {id: 41, name: "ภูเก็ต"},
          {id: 42, name: "มหาสารคาม"},
          {id: 43, name: "มุกดาหาร"},
          {id: 44, name: "แม่ฮ่องสอน"} ,
          {id: 45, name: "ยโสธร"},
          {id: 46, name: "ยะลา"},
          {id: 47, name: "ร้อยเอ็ด"},
          {id: 48, name: "ระนอง"},
          {id: 49, name: "ระยอง"},
          {id: 50, name: "ราชบุรี"},
          {id: 51, name: "ลพบุรี"},
          {id: 52, name: "ลำปาง"},
          {id: 53, name: "ลำพูน"},
          {id: 54, name: "เลย"},
          {id: 55, name: "ศรีสะเกษ"},
          {id: 56, name: "สกลนคร"},
          {id: 57, name: "สงขลา"} ,
          {id: 58, name: "สตูล"},
          {id: 59, name: "สมุทรปราการ"},
          {id: 60, name: "สมุทรสงคราม"},
          {id: 61, name: "สมุทรสาคร"},
          {id: 62, name: "สระแก้ว"},
          {id: 63, name: "สระบุรี"},
          {id: 64, name: "สิงห์บุรี"},
          {id: 65, name: "สุโขทัย"},
          {id: 66, name: "สุพรรณบุรี"},
          {id: 67, name: "สุราษฎร์ธานี"} ,
          {id: 68, name: "สุรินทร์"},
          {id: 69, name: "หนองคาย"},
          {id: 70, name: "หนองบัวลำภู"},
          {id: 71, name: "อยุธยา"},
          {id: 72, name: "อ่างทอง"},
          {id: 73, name: "อำนาจเจริญ"},
          {id: 74, name: "อุดรธานี"},
          {id: 75, name: "อุตรดิตถ์"},
          {id: 76, name: "อุทัยธานี"},
          {id: 77, name: "อุบลราชธานี"}
      ]

    };
  },
  computed: {
    ageList: function() {
        return Array(this.maxAge)
                .fill(null).map( (x,i) => i )
                .filter( (x) => x > 15);
    },
  }
};
</script>