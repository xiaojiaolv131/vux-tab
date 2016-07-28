<template>
    <tab :line-width="2" active-color="#fc378c">
      <tab-item :selected="selectTabTitle === item.title" v-for="item in tabTitlelist" @click="tabClick($index)">{{item.title}}</tab-item>
    </tab>
    <swiper :show-dots="false" height="500px">
      <swiper-item :selected="selectTabTitle === tabInfo.title" v-for="tabInfo in tabTitlelist">
      <div class="tab-swiper">
      <scroller lock-x :scrollbar-y="true" height="450px">
        <ul class="job-list">
          <li class="com-border-bottom" v-for="jobInfo in tabInfo.jobList">
            <a href="#">
              <img class="pic" src="https://ss2.baidu.com/6ONYsjip0QIZ8tyhnq/it/u=4267047014,3229650163&fm=58?size=130x130">
              <div class="info">
                <h3>{{jobInfo.name}}</h3>
                <div><span class="location">{{jobInfo.adrr}}</span><span class="date">{{jobInfo.time}}</span></div>
                <div><span class="money"><em>{{jobInfo.salary}}</em>元/天</span><span class="mod-tag tag_orange">每日结算</span><span class="mod-tag tag_red">有提成</span></div>
              </div>
              <span class="source">斗米</span>
            </a>
          </li>
        </ul>
        </scroller>
        </div>
      </swiper-item>
    </swiper>
</template>

<script>
import Tab from 'vux/dist/components/tab'
import TabItem from 'vux/dist/components/tab-item'
import Swiper from 'vux/dist/components/swiper'
import SwiperItem from 'vux/dist/components/swiper-item'
import Scroller from 'vux/dist/components/scroller'

export default {
  components: {
    Tab,
    TabItem,
    Swiper,
    SwiperItem,
    Scroller
  },
  data  () {
    return {
      selectTabTitle: '美食',
      tabTitlelist: [
        {
          'title': '精选',
          'jobList': [
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '10'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访1',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            }
          ]
        },
        {
          'title': '美食',
          'jobList': [
            {
              'name': '魏公村一带电话回访2',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '30'
            },
            {
              'name': '魏公村一带电话回访2',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访2',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访2',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            }
          ]
        },
        {
          'title': '电影',
          'jobList': [
            {
              'name': '魏公村一带电话回访3',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '60'
            },
            {
              'name': '魏公村一带电话回访3',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访3',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访3',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            }
          ]
        },
        {
          'title': '酒店',
          'jobList': [
            {
              'name': '魏公村一带电话回访4',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '90'
            },
            {
              'name': '魏公村一带电话回访4',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访4',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访4',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            }
          ]
        },
        {
          'title': '外卖',
          'jobList': [
            {
              'name': '魏公村一带电话回访5',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访5',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访5',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            },
            {
              'name': '魏公村一带电话回访5',
              'addr': '朝阳区望京',
              'time': '10.23-10.30',
              'salary': '130'
            }
          ]
        }
      ],
      selectedJobList: []
    }
  },
  methods: {
    tabClick (index) {
      this.selectTabTitle = this.tabTitlelist[index]
      this.selectedJobList = this.tabTitlelist[index].jobList
    }
  },
  created () {
    this.selectedJobList = this.tabTitlelist[0].jobList
  }
}
</script>

<style>
@import '~vux/dist/vux.css';
</style>