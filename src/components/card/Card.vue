<script setup></script>

<template>
  <div class="card">
    <div class="card__box">
      <div class="card__box-intro">
        <h2 class="card__box-intro-title">
          Get <span>insights</span> that help your business grow.
        </h2>

        <p class="card__box-intro-txt">
          Discover the benefits of data analytics and make better decisions
          regarding revenue, customer experience, and overall efficiency.
        </p>
      </div>
      <div class="card__box-stats">
        <div class="card__box-stats-stat">
          <span>10k+</span>
          <p>companies</p>
        </div>
        <div class="card__box-stats-stat">
          <span>314</span>
          <p>templates</p>
        </div>
        <div class="card__box-stats-stat">
          <span>12M+</span>
          <p>queries</p>
        </div>
      </div>
    </div>

    <div class="card__img">
        <img
      src="@/assets/images/image-header-desktop.jpg"
      alt=""
    />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  background: var(--cardBgColor);
  display: flex;
  justify-content: space-between;
  border-radius: 10px;
  width: 100%;
  gap: 50px;
  overflow: hidden;
  
  @media (max-width: 850px) {
    flex-direction: column-reverse;
    gap: 40px;
  }

  &__box {
    max-width: 500px;
    width: 100%;
    padding: 50px 60px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    @media (max-width: 850px) {
        gap: 50px;
        text-align: center;
        padding: 40px 40px 50px ;
    }

    &-intro {
      &-title {
        font-size: 35px;
        color: var(--statsColor);
        span {
          color: var(--accentColor);
        }

        margin-bottom: 30px;
      }

      &-txt {
        color: var(--mainParagraphColor);
      }
    }

    &-stats {
        display: flex;
        justify-content: space-between;
        
        @media (max-width: 850px) {
            flex-direction: column;
            gap: 30px;
            
        }
        
        &-stat {
            display: flex;
            flex-direction: column;
            gap: 10px;
            
            span {
                font-size: 28px;
                color: var(--statsColor);
                font-weight: 700;
            }
            
            p {
                text-transform: uppercase;
                font-family: 'Lexend Deca';
                color: var(--statHeadingsColor);
            }
        }
    }
  }

  &__img {
    height: 100%;
    max-width: 500px;
    width: 100%;
    position: relative;
    overflow: hidden;

    &::before {
        content: '';
        height: 100%;
        width: 100%;
        background: var(--imageFilterColor);
        inset: 0;
        position: absolute;
    }

    img {
        object-fit: cover;
    }
  }
  
}
</style>
