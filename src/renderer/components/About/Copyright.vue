<template>
  <el-row class="copyright">
    <el-col :span="6" class="copyright-left">
      <a>
        &copy;{{ year }} Motrix
      </a>
    </el-col>
    <el-col :span="18" class="copyright-right">
      <a>
        {{ $t('about.license') }}
      </a>
      <a>
        {{ $t('about.about') }}
      </a>
      <a>
        {{ $t('about.support') }}
      </a>
      <a>
        {{ $t('about.release') }}
      </a>
    </el-col>
  </el-row>
</template>

<script>
  export default {
    name: 'mo-copyright',
    data () {
      const year = new Date().getFullYear()
      return {
        year
      }
    }
  }
</script>

<style lang="scss">
.copyright {
  width: 100%;
  font-size: $--font-size-small;
  a {
    color: $--app-copyright-color;
    text-decoration: none;
  }
}
.copyright-left {
  text-align: left;
}

.copyright-right {
  text-align: right;
  a {
    margin-left: 30px;
  }
}
</style>
