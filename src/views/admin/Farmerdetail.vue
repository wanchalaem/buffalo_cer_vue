<template>
<div>
    <div class="container w-full mx-auto">
        <div class="w-full px-4 md:px-0 md:mt-8 mb-16 text-gray-800 leading-normal">
            <!--Console Content-->
            <div class="flex  justify-center items-center">
                <div class="w-full ">
                    <v-img class="rounded-full shadow-xl w-32 h-32" src="https://cdn.vuetifyjs.com/images/profiles/marcus.jpg"></v-img>

                </div>
            </div>

            <div class="flex flex-wrap">
                <div class="w-full md:w-1/1 xl:w-1/1 p-3">
                    <v-card>
                        <v-tabs>
                            <v-tab>
                                <v-icon left>mdi-account</v-icon>
                                ข้อมูลเกษตกร
                            </v-tab>
                            <v-tab>
                                <v-icon left>mdi-home-group</v-icon>
                                ข้อมูลฟาร์ม
                            </v-tab>
                            <v-tab>
                                <v-icon left>mdi-cow</v-icon>
                                ข้อมูลควาย
                            </v-tab>
                            <v-tab>
                                <v-icon left>mdi-file-image</v-icon>
                                รูปภาพ
                            </v-tab>
                            <v-tab>
                                <v-icon left>mdi-cog</v-icon>
                                ตั้งค่า
                            </v-tab>

                            <v-tab-item>
                                <v-card flat>
                                    <v-card-title primary-title>
                                        <h2 class="font-bold text-2xl">ข้อมูลเกษตกร</h2>
                                    </v-card-title>
                                    <v-card-text>
                                        <div>
                                            <v-expansion-panels v-model="panel" multiple flat>
                                                <v-expansion-panel>
                                                    <v-expansion-panel-header>
                                                        <h5 class="font-bold uppercase text-gray-500 text-2xl">เกี่ยวกับเกษตกร</h5>
                                                    </v-expansion-panel-header>
                                                    <v-expansion-panel-content>
                                                        <v-select :items="prefix" value="นาย" label="คำนำหน้า" prepend-inner-icon="mdi-human-male-female"></v-select>
                                                        <v-text-field value="นายแดง" label="ชื่อ" prepend-inner-icon="mdi-card-account-details-outline"></v-text-field>
                                                        <v-text-field value="มีชัย" label="นามสกุล" prepend-inner-icon="mdi-card-account-details-outline"></v-text-field>
                                                        <v-select :items="gender" value="ชาย" label="เพศ" prepend-inner-icon="mdi-human-male-female"></v-select>
                                                        <v-text-field value="1231231231231" label="หมายเลขบัตรประชาชน" type="number" prepend-inner-icon="mdi-card-account-details-outline"></v-text-field>
                                                        <v-text-field value="55" label="อายุ" prepend-inner-icon="mdi-account-clock-outline"></v-text-field>

                                                    </v-expansion-panel-content>
                                                </v-expansion-panel>

                                                <v-expansion-panel>
                                                    <v-expansion-panel-header>
                                                        <h5 class="font-bold uppercase text-gray-500 text-2xl">ติดต่อและที่อยู่</h5>
                                                    </v-expansion-panel-header>
                                                    <v-expansion-panel-content>
                                                        <v-text-field value="123/123" label="ที่อยู่" prepend-inner-icon="mdi-home-map-marker"></v-text-field>
                                                        <v-text-field value="0123123123" label="เบอร์โทร" type="number" prepend-inner-icon="mdi-phone"></v-text-field>
                                                    </v-expansion-panel-content>
                                                </v-expansion-panel>

                                            </v-expansion-panels>
                                        </div>
                                        <!-- <v-select   :items="prefix" value="นาย" label="คำนำหน้า" outlined prepend-inner-icon="mdi-human-male-female"></v-select>
                                        <v-text-field   value="นายแดง" label="ชื่อ" outlined prepend-inner-icon="mdi-card-account-details-outline"></v-text-field>
                                        <v-text-field   value="มีชัย" label="นามสกุล" outlined prepend-inner-icon="mdi-card-account-details-outline"></v-text-field>
                                        <v-select   :items="gender" value="ชาย" label="เพศ" outlined prepend-inner-icon="mdi-human-male-female"></v-select>
                                        <v-text-field   value="1231231231231" label="หมายเลขบัตรประชาชน" type="number" outlined prepend-inner-icon="mdi-card-account-details-outline"></v-text-field>
                                        <v-text-field   value="55" label="อายุ" outlined prepend-inner-icon="mdi-account-clock-outline"></v-text-field>
                                        <v-text-field   value="123/123" label="ที่อยู่" outlined prepend-inner-icon="mdi-home-map-marker"></v-text-field>
                                        <v-text-field   value="0123123123" label="เบอร์โทร" type="number" outlined prepend-inner-icon="mdi-phone"></v-text-field> -->
                                    </v-card-text>
                                    <v-card-title>
                                        <v-spacer></v-spacer>
                                        <v-btn color="success">แก้ไข</v-btn>
                                    </v-card-title>

                                </v-card>
                            </v-tab-item>

                            <v-tab-item>
                                <v-card flat>
                                    <v-card-title primary-title>
                                        <h2 class="font-bold text-2xl">ข้อมูลฟาร์ม</h2>
                                    </v-card-title>
                                    <v-card-text>
                                        <div>
                                            <v-expansion-panels v-model="panel" multiple>
                                                <v-expansion-panel>
                                                    <v-expansion-panel-header>
                                                        <h5 class="font-bold uppercase text-gray-500 text-2xl">เกี่ยวกับฟาร์ม</h5>
                                                    </v-expansion-panel-header>
                                                    <v-expansion-panel-content>
                                                        <v-text-field value="ฟาร์มนายแดง" prepend-inner-icon="mdi-home-outline" label="ชื่อฟาร์ม"></v-text-field>
                                                        <v-text-field value="12 ตัว" prepend-inner-icon="mdi-cow" type="number" label="จำนวนควายทั้งหมด"></v-text-field>
                                                        <v-select :items="group" value="กลุ่มแม่กา" prepend-inner-icon="mdi-account-group-outline" label="กลุ่มเกษตกร"></v-select>
                                                    </v-expansion-panel-content>
                                                </v-expansion-panel>

                                                <v-expansion-panel>
                                                    <v-expansion-panel-header>
                                                        <h5 class="font-bold uppercase text-gray-500 text-2xl">ที่อยู่ฟาร์ม</h5>
                                                    </v-expansion-panel-header>
                                                    <v-expansion-panel-content>
                                                        <v-text-field value="111 ต.แม่กา" prepend-inner-icon="mdi-home" label="​ที่อยู่ฟาร์ม"></v-text-field>
                                                        <v-select :items="tumbon" value="แม่กา" prepend-inner-icon="mdi-map-marker-multiple" label="ตำบล"></v-select>
                                                        <v-select :items="aumphur" value="แม่กา" prepend-inner-icon="mdi-map-marker-multiple" label="อำเภอ"></v-select>
                                                        <v-select :items="province" value="พะเยา" prepend-inner-icon="mdi-map-marker-multiple" label="จังหวัด"></v-select>
                                                        <v-select :items="postalcode" value="56000" prepend-inner-icon="mdi-postage-stamp" label="รหัสไปรษณีย์"></v-select>
                                                    </v-expansion-panel-content>
                                                </v-expansion-panel>

                                                <v-expansion-panel>
                                                    <v-expansion-panel-header>
                                                        <h5 class="font-bold uppercase text-gray-500 text-2xl">พิกัด GPS</h5>
                                                    </v-expansion-panel-header>
                                                    <v-expansion-panel-content>
                                                        <v-text-field value="1231231231" prepend-inner-icon="mdi-map-marker-multiple-outline" label="พิกัดฟาร์มตามระบบ GPS (ละติจูด)"></v-text-field>
                                                        <v-text-field value="123123123" prepend-inner-icon="mdi-map-marker-multiple-outline" label="พิกัดฟาร์มตามระบบ GPS (ลองติจูด)"></v-text-field>
                                                    </v-expansion-panel-content>
                                                </v-expansion-panel>

                                            </v-expansion-panels>
                                        </div>
                                        <!-- <v-text-field   value="ฟาร์มนายแดง" outlined prepend-inner-icon="mdi-home-outline" label="ชื่อฟาร์ม"></v-text-field> -->
                                        <!-- <v-text-field   value="111 ต.แม่กา" outlined prepend-inner-icon="mdi-home" label="​ที่อยู่ฟาร์ม"></v-text-field>
                                        <v-select   :items="tumbon" value="แม่กา" prepend-inner-icon="mdi-map-marker-multiple" outlined label="ตำบล"></v-select>
                                        <v-select   :items="aumphur" value="แม่กา" prepend-inner-icon="mdi-map-marker-multiple" outlined label="อำเภอ"></v-select>
                                        <v-select   :items="province" value="พะเยา" prepend-inner-icon="mdi-map-marker-multiple" outlined label="จังหวัด"></v-select>
                                        <v-select   :items="postalcode" value="56000" prepend-inner-icon="mdi-postage-stamp" outlined label="รหัสไปรษณีย์"></v-select> -->
                                        <!-- <v-text-field   value="1231231231" outlined prepend-inner-icon="mdi-map-marker-multiple-outline" label="พิกัดฟาร์มตามระบบ GPS (ละติจูด)"></v-text-field>
                                        <v-text-field   value="123123123" outlined prepend-inner-icon="mdi-map-marker-multiple-outline" label="พิกัดฟาร์มตามระบบ GPS (ลองติจูด)"></v-text-field> -->
                                        <!-- <v-text-field   value="12 ตัว" outlined prepend-inner-icon="mdi-cow" type="number" label="จำนวนควายทั้งหมด"></v-text-field>
                                        <v-select   :items="group" value="กลุ่มแม่กา" prepend-inner-icon="mdi-account-group-outline" outlined label="กลุ่มเกษตกร"></v-select> -->
                                    </v-card-text>
                                    <v-card-title>
                                        <v-spacer></v-spacer>
                                        <v-btn color="success">แก้ไข</v-btn>
                                    </v-card-title>

                                </v-card>
                            </v-tab-item>

                            <v-tab-item>
                                <v-card flat>
                                    <v-card-title primary-title>
                                        <h2 class="font-bold text-2xl">ข้อมูลควาย</h2>
                                    </v-card-title>
                                    <div class="container w-full mx-auto">
                                        <div class="w-full md:px-0 text-gray-800 leading-normal">
                                            <!--Console Content-->
                                            <div class="flex flex-wrap">
                                                <div class="w-full md:w-1/1 xl:w-1/1 p-1">
                                                    <!--Metric Card-->
                                                    <div class="bg-white border     p-2">
                                                        <div class="flex flex-row items-center">
                                                            <v-text-field v-model="search" clearable flat hide-details append-icon="mdi-magnify" label="ค้นหา" outlined single-line></v-text-field>
                                                            <v-divider vertical class="ma-1"></v-divider>
                                                            <v-dialog v-model="dialog" scrollable max-width="500px">
                                                                <template v-slot:activator="{ on, attrs }">
                                                                    <v-btn color="success" dark class="" v-bind="attrs" v-on="on">
                                                                        <v-icon>mdi-plus</v-icon>เพิ่มควาย
                                                                    </v-btn>
                                                                </template>
                                                                <v-card>
                                                                    <v-card-title>
                                                                        <h4>เพิ่มควาย</h4>
                                                                    </v-card-title>

                                                                    <v-card-text>
                                                                        <v-container>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-cow" color="green" outlined label="ชื่อหรือหมายเลขควาย"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-numeric-10-box-multiple-outline" color="green" outlined type="number" label="หมายเลข NID"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-numeric" color="green" outlined type="number" label="หมายเลขไมโครชิป"></v-text-field>
                                                                            <v-menu ref="menu" v-model="menu" :close-on-content-click="false" transition="scale-transition" offset-y min-width="290px">
                                                                                <template v-slot:activator="{ on, attrs }">
                                                                                    <v-text-field color="green" outlined v-model="date" class="rounded-lg" label="วัน/เดือน/ปีเกิด" prepend-inner-icon="mdi-calendar" readonly v-bind="attrs" v-on="on"></v-text-field>
                                                                                </template>
                                                                                <v-date-picker color="green" ref="picker" v-model="date" :max="new Date().toISOString().substr(0, 10)" min="1950-01-01" @change="save1"></v-date-picker>
                                                                            </v-menu>
                                                                            <v-select :items="sex" class="rounded-lg" prepend-inner-icon="mdi-gender-male-female" color="green" outlined label="เพศ"></v-select>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-calendar-clock" color="green" outlined type="number" label="อายุ (..ปี..เดือน)"></v-text-field>
                                                                            <v-select :items="color" class="rounded-lg" prepend-inner-icon="mdi-invert-colors" color="green" outlined label="สี"></v-select>
                                                                            <v-select :items="from" class="rounded-lg" prepend-inner-icon="mdi-import" color="green" outlined label="แหล่งที่มา"></v-select>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-tag-outline" color="green" outlined type="number" label="ราคา"></v-text-field>
                                                                            <v-select :items="status" class="rounded-lg" prepend-inner-icon="mdi-post-outline" color="green" outlined label="สถานะควาย"></v-select>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-cow" color="green" outlined label="ชื่อหรือหมายเลขพ่อ"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-numeric-10-box-multiple-outline" color="green" outlined type="number" label="หมายเลข NID พ่อ"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-numeric" color="green" outlined type="number" label="หมายเลขไมโครชิปพ่อ"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-cow" color="green" outlined label="ชื่อหรือหมายเลขแม่"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-numeric-10-box-multiple-outline" color="green" outlined type="number" label="หมายเลข NID แม่"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-numeric" color="green" outlined type="number" label="หมายเลขไมโครชิปแม่"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-weight-kilogram" color="green" outlined type="number" label="น้ำหนัก (กิโลกรัม)"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-arrow-left-right" color="green" outlined type="number" label="ความกว้างรอบอก (เซนติเมตร)"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-arrow-left-right" color="green" outlined type="number" label="ความยาวลำตัว (เซนติเมตร)"></v-text-field>
                                                                            <v-text-field class="rounded-lg" prepend-inner-icon="mdi-human-male-height-variant" color="green" outlined type="number" label="ความสูง (เซนติเมตร)"></v-text-field>
                                                                            <v-file-input class="rounded-lg" prepend-inner-icon="mdi-cow" color="green" outlined multiple label="เพิ่มภาพด้านข้าง"></v-file-input>
                                                                            <v-file-input class="rounded-lg" prepend-inner-icon="mdi-cow" color="green" outlined multiple label="เพิ่มภาพด้านหลัง"></v-file-input>

                                                                        </v-container>
                                                                    </v-card-text>

                                                                    <v-card-actions>
                                                                        <v-spacer></v-spacer>
                                                                        <v-btn color="green" class="rounded-lg" dark @click="save">
                                                                            <h5>บันทึก</h5>
                                                                        </v-btn>
                                                                        <v-btn color="error" class="rounded-lg" @click="close">
                                                                            <h5>ยกเลิก</h5>
                                                                        </v-btn>
                                                                    </v-card-actions>
                                                                </v-card>
                                                            </v-dialog>
                                                        </div>
                                                    </div>
                                                </div>
                                            </div>
                                        </div>
                                    </div>

                                    <v-card-text>
                                        <v-data-table :headers="headers" :items="desserts" :search="search" sort-by="calories" class="elevation-2 pa-2">
                                            <template v-slot:item.actions="{ item }">
                                                <!-- <v-tooltip v-model="show" top> -->
                                                <v-tooltip top>
                                                    <template v-slot:activator="{ on, attrs }">
                                                        <v-btn color="primary" icon v-bind="attrs" v-on="on">
                                                            <v-icon>mdi-clipboard-text-outline</v-icon>
                                                        </v-btn>
                                                    </template>
                                                    <span>ใบพันธุ์ประวัติ</span>
                                                </v-tooltip>

                                                <!-- <v-tooltip v-model="show" top> -->
                                                <v-tooltip top>
                                                    <template v-slot:activator="{ on, attrs }">
                                                        <v-btn color="success" icon v-bind="attrs" v-on="on" @click="$router.push(`buffalo`)">
                                                            <v-icon>mdi-eye-outline</v-icon>
                                                        </v-btn>
                                                    </template>
                                                    <span>ดูข้อมูล</span>
                                                </v-tooltip>

                                                <!-- <v-tooltip v-model="show" top> -->
                                                <v-tooltip top>
                                                    <template v-slot:activator="{ on, attrs }">
                                                        <v-btn color="error" icon v-bind="attrs" v-on="on" @click="deleteItem(item)">
                                                            <v-icon>mdi-delete</v-icon>
                                                        </v-btn>
                                                    </template>
                                                    <span>ลบ</span>
                                                </v-tooltip>

                                            </template>
                                            <template v-slot:no-data>
                                                <v-btn color="primary" @click="initialize">Reset</v-btn>
                                            </template>
                                        </v-data-table>
                                    </v-card-text>
                                </v-card>
                            </v-tab-item>

                            <v-tab-item>
                                <v-card flat>
                                    <v-card-title primary-title>
                                        <h2 class="font-bold text-2xl">รูปภาพ</h2>
                                    </v-card-title>
                                    <v-card-title primary-title>
                                        <div class="md:ml-20">
                                            <center>
                                                <h3>ภาพถ่ายบัตรประจำตัวประชาชน</h3>
                                                <v-img class=" elevation-1" :aspect-ratio="1.5" src="https://encrypted-tbn0.gstatic.com/images?q=tbn%3AANd9GcSNf3OTIf1lugjQhtLRTP8cwuosPAJmIykTsry1UL87ArfVFx84&usqp=CAU"></v-img>
                                                <v-btn color="success">
                                                    <v-icon>mdi-upload</v-icon>อัพโหลดบัตรประชาชน
                                                </v-btn>
                                            </center>
                                        </div>
                                        <v-spacer></v-spacer>
                                        <div class="md:mr-20">
                                            <center>
                                                <h3>ภาพถ่ายฟาร์ม</h3>
                                                <v-img class=" elevation-1" :aspect-ratio="1.5" src="https://images.pexels.com/photos/158179/lake-constance-sheep-pasture-sheep-blue-158179.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"></v-img>
                                                <v-btn color="success">
                                                    <v-icon>mdi-upload</v-icon>อัพโหลดบัตรประชาชน
                                                </v-btn>
                                            </center>
                                        </div>
                                    </v-card-title>
                                </v-card>
                            </v-tab-item>

                            <v-tab-item>
                                <v-card flat>
                                    <v-card-title primary-title>
                                        <h2 class="font-bold text-2xl">แก้ไขรหัสผ่าน</h2>
                                    </v-card-title>
                                    <v-card-text>
                                        <v-text-field value="dang1234" label="รหัสผ่านเก่า" type="password" outlined></v-text-field>
                                        <v-text-field value="123456789" label="รหัสผ่านใหม่" type="password" outlined></v-text-field>
                                        <v-text-field value="123456789" label="ยืนยันรหัสผ่าน" type="password" outlined></v-text-field>
                                    </v-card-text>
                                    <v-card-title primary-title>
                                        <v-spacer></v-spacer>
                                        <v-btn color="success">แก้ไข</v-btn>
                                    </v-card-title>
                                </v-card>
                            </v-tab-item>

                        </v-tabs>
                    </v-card>
                </div>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data: () => ({
        panel: [0, 1, 2, 3],
        prefix: ['นาย', 'นาง', 'นางสาว'],
        gender: ['ชาย', 'หญิง'],
        tumbon: ['แม่กา', 'แม่ใจ'],
        aumphur: ['แม่กา', 'แม่ใจ'],
        province: ['พะเยา', 'น่าน'],
        postalcode: ['56000', '56100'],
        group: ['แม่กา', 'แม่ใจ'],

        sex: ['ตัวผู้', 'ตัวเมีย'],
        color: ['ดำ', 'น้ำตาล'],
        from: ['พ่อค้าคนกลาง', 'คลอด'],
        status: ['ท้อง', 'ไม่ท้อง'],
        date: null,
        menu: false,
        tab: null,
        search: '',
        dialog: false,

        headers: [{
                text: 'ชื่อ',
                value: 'name',
                sortable: false
            },
            {
                text: 'เบอร์หู',
                value: 'number',
                sortable: false
            },
            {
                text: 'อายุ',
                value: 'age',
                sortable: false
            },
            {
                text: 'เพศ',
                value: 'sex',
                sortable: false
            },
            {
                text: 'การจัดการ',
                value: 'actions',
                sortable: false
            },
        ],

        desserts: [],
        editedIndex: -1,
        editedItem: {
            IDcardFarmer: '',
            nonb: '',
            nid: '',
            nmi: '',
            birth: ''
        },
        defaultItem: {
            name: '',
            number: '',
            gene: '',
            age: '',
            certifacate: ''
        },
    }),

    watch: {
        dialog(val) {
            val || this.close()
        },
        menu(val) {
            val && setTimeout(() => (this.$refs.picker.activePicker = 'YEAR'))
        },
    },

    created() {
        this.initialize()
    },

    methods: {
        initialize() {
            this.desserts = [{
                    name: 'กระบือ1',
                    number: '3',
                    gene: 'thai',
                    age: '4ปี0เดือน',
                    sex: 'เมีย'
                },
                {
                    name: 'กระบือ2',
                    number: '2',
                    gene: 'thai',
                    age: '2ปี1เดือน',
                    sex: 'ผู้'
                },
                {
                    name: 'กระบือ3',
                    number: '9',
                    gene: 'thai',
                    age: '6ปี2เดือน',
                    sex: 'ผู้'
                },
                {
                    name: 'กระบือ4',
                    number: '7',
                    gene: 'thai',
                    age: '1ปี',
                    sex: 'เมีย'
                },
                {
                    name: 'กระบือ5',
                    number: '1',
                    gene: 'thai',
                    age: '2ปี',
                    sex: 'เมีย'
                },
                {
                    name: 'กระบือ6',
                    number: '2',
                    gene: 'thai',
                    age: '3ปี',
                    sex: 'เมีย'
                },
            ]
        },

        editItem(item) {
            this.editedIndex = this.desserts.indexOf(item)
            this.editedItem = Object.assign({}, item)
            this.dialog = true
        },

        deleteItem(item) {
            const index = this.desserts.indexOf(item)
            confirm('Are you sure you want to delete this item?') && this.desserts.splice(index, 1)
        },

        close() {
            this.dialog = false
            this.$nextTick(() => {
                this.editedItem = Object.assign({}, this.defaultItem)
                this.editedIndex = -1
            })
        },

        save() {
            if (this.editedIndex > -1) {
                Object.assign(this.desserts[this.editedIndex], this.editedItem)
            } else {
                this.desserts.push(this.editedItem)
            }
            this.close()

        },
        save1(date) {
            this.$refs.menu.save(date)
        },

    },

}
//<script>
</script>
