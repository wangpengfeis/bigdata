<template>
  <el-card>
    <div slot="header" class="clearfix">
      <span>城市推荐资料</span>
      <el-button style="float: right; padding: 3px 0" type="text">操作按钮</el-button>
    </div>
    <el-form ref="form" :model="form" label-position="top" label-width="120px">
      <el-form-item label="城市推荐方案">
        <el-input
          v-model="textarea2"
          type="textarea"
          :autosize="{ minRows: 2, maxRows: 4}"
          placeholder="请输入内容"
        />
      </el-form-item>
      <el-form-item>
        <el-upload
          class="upload-demo"
          action="https://jsonplaceholder.typicode.com/posts/"
          :file-list="fileList"
        >
          <el-button size="small" type="primary">点击上传</el-button>
          <div slot="tip" class="el-upload__tip">只能上传jpg/png文件，且不超过500kb</div>
        </el-upload>
        <div class="img-box">
          <div v-for="it in fileList" :key="it" class="img-lib">
            <img :src="it.url" alt="">
          </div>
        </div>
      </el-form-item>
      <el-form-item label="城市荣誉与名片">
        <el-input
          v-model="textarea2"
          type="textarea"
          :autosize="{ minRows: 2, maxRows: 4}"
          placeholder="请输入内容"
        />
      </el-form-item>
      <el-form-item>
        <el-upload
          class="upload-demo"
          action="https://jsonplaceholder.typicode.com/posts/"
          :file-list="fileList"
        >
          <el-button size="small" type="primary">点击上传</el-button>
          <div slot="tip" class="el-upload__tip">只能上传jpg/png文件，且不超过500kb</div>
        </el-upload>
        <div class="img-box">
          <div v-for="it in fileList" :key="it" class="img-lib">
            <img :src="it.url" alt="">
          </div>
        </div>
      </el-form-item>
      <el-form-item label="城市区位优势">
        <el-input
          v-model="textarea2"
          type="textarea"
          :autosize="{ minRows: 2, maxRows: 4}"
          placeholder="请输入内容"
        />
      </el-form-item>
      <el-form-item>
        <el-upload
          class="upload-demo"
          action="https://jsonplaceholder.typicode.com/posts/"
          :file-list="fileList"
        >
          <el-button size="small" type="primary">点击上传</el-button>
          <div slot="tip" class="el-upload__tip">只能上传jpg/png文件，且不超过500kb</div>
        </el-upload>
        <div class="img-box">
          <div v-for="it in fileList" :key="it" class="img-lib">
            <img :src="it.url" alt="">
          </div>
        </div>
      </el-form-item>
    </el-form>
  </el-card>
</template>
<script>
export default {
  data() {
    return {
      fileList: [{ name: '', url: 'https://fuss10.elemecdn.com/3/63/4e7f3a15429bfda99bce42a18cdd1jpeg.jpeg?imageMogr2/thumbnail/360x360/format/webp/quality/100' }, { name: 'food2.jpeg', url: 'https://fuss10.elemecdn.com/3/63/4e7f3a15429bfda99bce42a18cdd1jpeg.jpeg?imageMogr2/thumbnail/360x360/format/webp/quality/100' }]

    }
  },
  methods: {
    handleRemove(file, fileList) {
      console.log(file, fileList)
    },
    handlePreview(file) {
      console.log(file)
    }
  }
}
</script>
<style lang="scss" >
.box-card{
    width: 50%;
}
.el-upload-list{
    display: none;
}
.img-box{
    width: 100%;

    overflow: hidden;
    .img-lib{
        width: 160px;
        height: 160px;
        float: left;
        padding: 10px 0;
        margin-right: 10px;
        border-radius: 10px;
        img{
            width: 100%;
            height: 100%;
            display: block;

        }
    }
}
</style>
