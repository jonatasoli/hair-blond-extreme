<template>
  <main>
    <HistoryCourse />
    <Bonus />
    <TimeRunningOut />
    <Risk />
    <Bio />
    <FacebookComments />
  </main>
</template>

<script>
import HistoryCourse from './CourseHistory'
import Bonus from './Bonus'
import TimeRunningOut from './TimeRunningOut'
import Risk from './Risk'
import Bio from './Bio'
import FacebookComments from './FacebookComments'
export default {
  name: 'SalesPageContent',
  components: {
    HistoryCourse,
    Bonus,
    TimeRunningOut,
    Risk,
    Bio,
    FacebookComments
  }
}
</script>

<style scoped></style>
