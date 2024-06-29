<script lang="ts">
  let groups = [
    {
      "id": 1,
      "group": "กลุ่มการบริหารราชการแผ่นดินและความมั่นคง"
    },
    {
      "id": 2,
      "group": "กลุ่มกฎหมายและกระบวนการยุติธรรม"
    },
    {
      "id": 3,
      "group": "กลุ่มการศึกษา"
    },
    {
      "id": 4,
      "group": "กลุ่มการสาธารณสุข"
    },
    {
      "id": 5,
      "group": "กลุ่มอาชีพทำนา ปลูกพืชล้มลุก"
    },
    {
      "id": 6,
      "group": "กลุ่มอาชีพทำสวน ป่าไม้ ปศุสัตว์ ประมง"
    },
    {
      "id": 7,
      "group": "กลุ่มพนักงานหรือลูกจ้าง ที่ไม่ใช่ส่วนราชการหรือหน่วยงานของรัฐ ผู้ใช้แรงงาน"
    },
    {
      "id": 8,
      "group": "กลุ่มอาชีพด้านสิ่งแวดล้อม ผังเมือง อสังหาริมทรัพย์และสาธารณูปโภค ทรัพยากรธรรมชาติ พลังงาน"
    },
    {
      "id": 9,
      "group": "กลุ่มผู้ประกอบกิจการขนาดกลางและขนาดย่อม"
    },
    {
      "id": 10,
      "group": "กลุ่มผู้ประกอบกิจการอื่นนอกจากกลุ่มที่ 9"
    },
    {
      "id": 11,
      "group": "กลุ่มผู้ประกอบธุรกิจหรืออาชีพด้านการท่องเที่ยว"
    },
    {
      "id": 12,
      "group": "กลุ่มผู้ประกอบอุตสาหกรรม"
    },
    {
      "id": 13,
      "group": "กลุ่มผู้ประกอบอาชีพด้านวิทยาศาสตร์ เทคโนโลยี การสื่อสาร การพัฒนานวัตกรรม"
    },
    {
      "id": 14,
      "group": "กลุ่มสตรี"
    },
    {
      "id": 15,
      "group": "กลุ่มผู้สูงอายุ คนพิการ กลุ่มชาติพันธุ์ กลุ่มอัตลักษณ์อื่น"
    },
    {
      "id": 16,
      "group": "กลุ่มศิลปะ วัฒนธรรม ดนตรี การแสดงและบันเทิง นักกีฬา"
    },
    {
      "id": 17,
      "group": "กลุ่มประชาสังคม องค์กรสาธารณประโยชน์"
    },
    {
      "id": 18,
      "group": "กลุ่มสื่อสารมวลชน ผู้สร้างสรรค์วรรณกรรม"
    },
    {
      "id": 19,
      "group": "กลุ่มผู้ประกอบวิชาชีพ ผู้ประกอบอาชีพอิสระ"
    },
    {
      "id": 20,
      "group": "กลุ่มอื่น ๆ"
    }
  ];
</script>

<svelte:head>
  <title>Sorwor (Senator) Description</title>
</svelte:head>

<main>
  <header>
    <h1>Sorwor (Senator) Description</h1>
  </header>
  <section id="input-section">
    <label for="name">คุณชื่ออะไร</label>
    <input type="text" id="name" name="name" placeholder="ชื่อของคุณ">
    <label for="occupation">คุณทำอะไร</label>
    <input type="text" id="occupation" name="occupation" placeholder="อาชีพของคุณ">
    <label for="group">กลุ่มอาชีพ</label>
    <select name="group" id="group">
      <option value="">--เลือกกลุ่มอาชีพที่คุณต้องการ--</option>
      {#each groups as {id, group}}
        <option value={id}>{group}</option>
      {/each}
    </select>

  </section>
  <section id="generate-section">
    <button>Generate Description</button>
  </section>
  <section id="description-section">

  </section>
  <footer>
    Copyright (c) 2023, by <a href="https://github.com/lebrancconvas" target="_blank">Poom Yimyuean (@lebrancconvas)</a> <a href="https://github.com/lebrancconvas/Sorwor-Description" target="_blank">Github</a>
  </footer>
</main>

<style>
  header > h1 {
    text-align: center;
  }
  footer {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    text-align: center;
    padding: 10px;
  }
</style>
