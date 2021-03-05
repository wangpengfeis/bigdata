<template>
  <el-card>
    <div slot="header" class="clearfix">
      <span>产业政策与发展状况</span>
      <el-button style="float: right; padding: 3px 0" type="text">操作按钮</el-button>
    </div>
    <el-form ref="form" :model="form" label-position="top" label-width="120px">
      <el-form-item label="产业综述">
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
      <el-row>
        <el-select v-model="value" size="small" placeholder="请选择">
          <el-option
            v-for="item in options"
            :key="item.value"
            :label="item.label"
            :value="item.value"
          />
        </el-select>
        <el-button type="primary" icon="el-icon-plus" size="small" style="margin-left:10px" circle />

      </el-row>
    </el-form>
  </el-card>
</template>
<script>
export default {
  data() {
    return {
      fileList: [{ name: '', url: 'https://fuss10.elemecdn.com/3/63/4e7f3a15429bfda99bce42a18cdd1jpeg.jpeg?imageMogr2/thumbnail/360x360/format/webp/quality/100' }, { name: 'food2.jpeg', url: 'https://fuss10.elemecdn.com/3/63/4e7f3a15429bfda99bce42a18cdd1jpeg.jpeg?imageMogr2/thumbnail/360x360/format/webp/quality/100' }],
      options: [{
        value: '选项1',
        label: '黄金糕'
      }, {
        value: '选项2',
        label: '双皮奶'
      }, {
        value: '选项3',
        label: '蚵仔煎'
      }, {
        value: '选项4',
        label: '龙须面'
      }, {
        value: '选项5',
        label: '北京烤鸭'
      }],
      value: ''

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
