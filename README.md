<!doctype html>
<html>
<title>muntadher </title>
<head>
<style >

 
  &__line-container {
    display: block;
    height: 4px;
    position: relative;
    width: 100%;
  }
 
  &__line {
    height: 2px;
    background: $brand-color;
    position: absolute;
    width: auto;
    transition: 0.25s ease;
  }
 
  &__content {
    display: none;
    padding-top: 24px;
    padding-bottom: 32px;

    &.ai-tabs__content--active {
     display: block;
    }
  }
  
  &--active {
   // background: #ff0000;
  }
}



</style >
<script>

      
      setActive = (e, $tabs) => {
        e.preventDefault();
        const divId = e.currentTarget.getAttribute('href');

        $tabs.forEach(($tab) => {
          $tab.classList.remove('ai-tabs--active');
        });

        document.querySelectorAll('.ai-tabs__content').forEach(($content) => {
         $content.classList.remove('ai-tabs__content--active');
        });

        e.currentTarget.classList.add('ai-tabs--active');
        document.querySelector(divId).classList.add('ai-tabs__content--active');
      };

$tabs.forEach(($tab) => {
  onLoadLine();
  $tab.addEventListener('click', (e) => {
    setActive(e, $tabs);
    animateLine(e.currentTarget, $line);
  });
});

</script>
<body>

<main>
   <section class="ai-content">
      <header class="ai-content__title">
         <h1 class="text-center"> Animated Tabs </h1>
      </header>

      <section class="ai-content__main">
         <div class="ai-content__content">
           <div class="ai-tabs">
            <nav class="ai-tabs__tab-header">
             <ul>
              <li><a href="#one" class="ai-tabs__link">Tab one</a></li>
              <li><a href="#two" class="ai-tabs__link ai-tabs--active">Tab two</a></li>
              <li><a href="#three" class="ai-tabs__link">Tab three</a></li>
             </ul>
             <div class="ai-tabs__line-container">
              <div class="ai-tabs__line"></div>
             </div>
            </nav>
            <div class="ai-tabs__content-container">
             <div class="ai-tabs__content" id="one">
              Lorem ipsum dolor amet 3 wolf moon next level mixtape jianbing single-origin coffee knausgaard banh mi yuccie four loko four dollar toast. Slow-carb typewriter ugh gentrify, crucifix post-ironic mustache. 
             </div>
             <div class="ai-tabs__content"  id="two">
              Pinterest art party gluten-free, keytar banh mi vinyl synth aesthetic. Gentrify selvage photo booth ennui, viral fanny pack meggings whatever lo-fi lumbersexual offal beard. 
             </div>
             <div class="ai-tabs__content"  id="three">
              Tumblr ennui squid, literally typewriter sartorial celiac cloud bread hot chicken umami palo santo. Artisan meditation cray echo park intelligentsia pok pok health goth pop-up drinking vinegar pabst.
             </div>
            </div>
          </div>
         </div>
         <footer class="ai-image__container">
            <img src="https://spaceholder.cc/800x600" class="ai-image__img" />
         </footer
      </section>

      <footer class="ai-madeby">
         Made By <a href="http://beautiful-tragedy.com" _target="blank">Amanda Iaria</a>
      </footer>
   </section>
</main>
</body>

