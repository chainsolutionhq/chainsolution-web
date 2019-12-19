<template>
  <div class="chainsolution">
    <!-- header -->
    <header>
      <div class="logo"></div>
      <ul class="navs">
        <li v-for="(nav, key) in navlists" :key="key" :class="key == activce ? 'active': ''" @click="activce=key">
          <a :href="'#p'+key"> {{ nav }} </a>
        </li>
      </ul>
    </header>
    <!-- page1 -->
    <div class="page1" id="p0" style="backgroundImage: url('http://q2a6kfuu5.bkt.clouddn.com/p1.png?imageView/2/w/960/h/505')">
      <!-- {{ msg }} -->
      <div class="page1logo"></div>
      <div class="page1desc">
        <p class="p1h1">链卡结合，打造区块链信任基石</p>
        <p class="p1h2">从芯片到链，让您服务客户更简单</p>
      </div>
      <div class="p1common p1t1">金融领域</div>
      <div class="p1common p1t2">艺术藏品</div>
      <div class="p1common p1t3">数字版权</div>
    </div>
    <!-- page2 -->
    <div class="page2" id="p1" style="backgroundImage: url('http://q2a6kfuu5.bkt.clouddn.com/p2.png?imageView/2/w/960/h/540')">
      <h2>区块链到卡一站式解决方案</h2>
      <p class="p2c">企业和组织是建立在信任的基础之上。有了信任，就会相信企业间的交易是合法的，企业生产的产品不是伪造的，企业就如显现出来的这般诚实可靠令人信赖。链卡科技将这种信任提升了一个全新的水平。我们的芯片供应链技术创造了一种前所未有的数字信任形式。</p>
      <!-- <div class="p2btn"></div> -->
      <a href="mailto:business@chainsolution.cn?subject=联系我们&body=欢迎您提出意见建议" class="p2btn">联系我们</a>
    </div>
    <!-- page3 -->
    <div class="page3" id="p2" style="backgroundImage: url('http://q2a6kfuu5.bkt.clouddn.com/p3.png?imageView/2/w/960/h/540&ver=1')">
      <h2>6大应用场景</h2>
      <div class="" v-for="(sence, key) in scenes" :key="key" :class="'sence sence'+key">
        <h3>{{ sence.name }}</h3>
        <p>{{ sence.content }}</p>
      </div>
    </div>
    <div class="page4" id="p3" style="backgroundImage: url('http://q2a6kfuu5.bkt.clouddn.com/ys.png?imageView/2/w/1280/h/720')">
      <h2>链卡团队的优势</h2>
      <p>从芯片到链，代码全部开源，代码灵活度高且可控性强，根据需求定制化。</p>
      <p>行业顶级专家顾问团队，从方案到项目落地全程参与，为企业赋能，助理企业解决行业区块链从升级到应用落地遇到技术问题。</p>
    </div>
    <footer id="p4">
      <div class="p4logo"></div>
      <div class="p4contect">
        <div class="desc"><span>帮助与支持</span><span>联系我们 test</span></div>
        <div class="desc"><span>Q&A</span><span>Email:business@chainsolution.cn</span></div>
        <div class="line"></div>
      </div>
      <div class="p4logo2"></div>
      <div class="copyrihts">Copyright &#169; 2019 链卡科技版权所有 粤ICP备19155218号</div>
      <div class="qrcode">
        <img src="../assets/qrcode.png" alt="...">
        <p>扫码关注链卡科技了解最新动态</p>
      </div>
    </footer>
  </div>
</template>

<script>
import './index.scss'

export default {
  name: 'Website',
  data() {
    return {
      navlists: ['首页', '应用场景', '解决方案', '优势', '公司介绍'],
      scenes: [
        { name: '身份存储',
          content: '提供更安全的去中心化的个人身份线上、线下鉴别方案，保护隐私。避免隐私侵占及身份盗用的问题。'
        },
        { name: '政府与公益',
          content: '通过搭建包含政府监管机构、第三方公共服务机构的联盟链，可以探索创新管理机制，实现政务实时监管，并借助区块链的不可篡改、可追溯特性，极大提高仲裁效率及公正透明的信任基础'
        },
        { name: '数字版权',
          content: '提供数字版权的受限分发及版权流量管控，为数字版权的所属权保管及转让提供一站式解决方案。'
        },
        { name: '艺术藏品',
          content: '基于数字介子的创作具备限量价值，同时为现有艺术藏品的流通、鉴别提供更安全且低成本的解决方案。'
        },
        { name: '金融领域',
          content: '依托区块链去中心化账本，链接金融机构的信任。结合去中心化的加密卡，交易双方或多方可以共享一套可信、互认的账本，所有的交易清结算记录全部在链可查，安全透明、不可篡改、可追溯，极大提升对账准确度和效率。'
        },
        { name: '零售行业',
          content: '商品打造“身份证”，上传数据不可篡改，商品从原材料的采购到终端零售商，之间环节验证过的信息源头添加到区块链防伪溯源系统中，实现精细到一物一码的全流程正品追溯。'
        }
      ],
      activce: 0
    }
  }
}
</script>
