<script setup>
const dishes = [
  {
    "name": "砂锅菌菇鸡",
    "description": "鸡肉与香菇同炖，汤鲜，肉嫩。",
    "price": "¥68"
  },
  {
    "name": "青椒炒黄牛肉",
    "description": "薄切黄牛肉，大火快炒，青椒鲜辣。",
    "price": "¥58"
  },
  {
    "name": "清炒时令鲜蔬",
    "description": "随季节换菜，蒜香清爽。",
    "price": "¥128"
  }
]
</script>

<template>
  <header>
    <a class="brand" href="#"><span class="seal" aria-hidden="true">山</span>山野小馆</a>
    <nav aria-label="主导航">
      <a href="#menu">招牌菜</a>
      <a href="#visit">到店信息</a>
    </nav>
  </header>

  <main>
    <div class="hero">
      <div class="wrap">
        <div class="eyebrow">时令晚餐哈哈风味</div>
        <h1>山野小馆</h1>
        <p>循着节气挑食材，慢火做一桌家常好菜。</p>
        <a class="button" href="#menu">看看招牌菜</a>
      </div>
    </div>

    <section id="menu">
      <div class="wrap">
        <div class="eyebrow">菜单选粹</div>
        <h2>小馆招牌</h2>
        <div class="grid">
          <article v-for="dish in dishes" :key="dish.name">
            <h3>{{ dish.name }}</h3>
            <p>{{ dish.description }}</p>
            <span class="price">{{ dish.price }}</span>
          </article>
        </div>
      </div>
    </section>

    <section id="visit" class="visit">
      <div class="wrap">
        <div class="eyebrow">到店信息</div>
        <h2>去小馆吃饭</h2>
        <div class="details">
          <div>
            <strong>营业时间（示例）</strong>
            <p>午餐 11:30–14:00<br>晚餐 17:30–21:00</p>
          </div>
          <div>
            <strong>地址与订位</strong>
            <p>门店地址及订位电话待补充。</p>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>山野小馆 · 餐馆首页示例，菜品及价格仅供展示。</footer>
</template>
