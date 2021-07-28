<template>
  <div>
    <v-row align="center">
      <v-col md="6">
        <v-card>
          <v-card-title class="headline"> Đắc Tâm </v-card-title>
          <v-card-text>
            <p>
              Từ nguồn dược liệu được chọn lọc chất lượng cao, ĐẮC TÂM đã chiết
              xuất thành công các sản phẩm bột cao khô vẫn giữ nguyên hoạt chất
              quý giá từ nguồn dược liệu gốc, đảm bảo chuẩn hóa các tiêu chuẩn,
              đồng thời mang lại sự tiện dụng cho người sử dụng và nhận được sự
              đánh giá cao của các thầy thuốc chuyên môn.
            </p>

            <p>
              ĐẮC TÂM là địa chỉ tin cậy cung ứng những vị thuốc y học cổ truyền
              uy tín, chất lượng, giá từ nguồn dược liệu gốc, đảm bảo chuẩn hóa
              các tiêu chuẩn, đồng thời mang lại sự tiện dụng cho người sử dụng
              và nhận được sự đánh giá cao của các thầy thuốc chuyên môn.
            </p>
          </v-card-text>
        </v-card>
      </v-col>
      <v-col md="6">
        <v-img src="/img/index_img_1.jpg"></v-img>
      </v-col>
    </v-row>
    <div class="text-center mt-16 display-1">
        SẢN PHẨM
    </div>
    <v-row>
      <v-col cols="12" md="4">
        <MyCard imgUrl="/img/index_img_1.jpg" 
                title="duoc lieu"
                routerTo="/"/>
      </v-col>
      <v-col cols="12" md="4">
         <MyCard imgUrl="/img/index_img_1.jpg" 
                title="tra hoa"
                routerTo="/"/>
      </v-col>
      <v-col cols="12" md="4">
         <MyCard imgUrl="/img/index_img_1.jpg" 
                title="thiet bi y te"
                routerTo="/"/>
      </v-col>
    </v-row>
    <div class="text-center mt-16 display-1">
        TIN NỔI BẬT
    </div>
    <v-row class="mb-10">

    </v-row>
  </div>
</template>
