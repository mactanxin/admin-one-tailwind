<script setup>
import { mdiMonitorCellphone, mdiAccountMultiple, mdiTableBorder, mdiTableOff, mdiGithub } from '@mdi/js'
import SectionMain from '@/components/SectionMain.vue'
import NotificationBar from '@/components/NotificationBar.vue'
import TableSampleClients from '@/components/TableSampleClients.vue'
import CardBox from '@/components/CardBox.vue'
import LayoutAuthenticated from '@/layouts/LayoutAuthenticated.vue'
import SectionTitleLineWithButton from '@/components/SectionTitleLineWithButton.vue'
import BaseButton from '@/components/BaseButton.vue'
</script>

<template>
  <LayoutAuthenticated>
    <SectionMain>
      <SectionTitleLineWithButton
        :icon="mdiTableBorder"
        title="Tables"
        main
      >
        <BaseButton
          href="https://github.com/justboil/admin-one-vue-tailwind"
          target="_blank"
          :icon="mdiGithub"
          label="Star on GitHub"
          color="contrast"
          rounded-full
          small
        />
      </SectionTitleLineWithButton>
      <NotificationBar
        color="info"
        :icon="mdiMonitorCellphone"
      >
        <b>Responsive table.</b> Collapses on mobile
      </NotificationBar>

      <CardBox
        class="mb-6"
        title="Clients"
        :icon="mdiAccountMultiple"
        has-table
      >
        <TableSampleClients checkable />
      </CardBox>

      <SectionTitleLineWithButton
        :icon="mdiTableBorder"
        title="Wrapped variation"
      />

      <NotificationBar
        color="success"
        :icon="mdiTableBorder"
      >
        <b>Tightly wrapped</b> &mdash; table header becomes card header
      </NotificationBar>

      <CardBox
        class="mb-6"
        has-table
      >
        <TableSampleClients checkable />
      </CardBox>

      <SectionTitleLineWithButton
        :icon="mdiTableOff"
        title="Empty variation"
      />

      <NotificationBar
        color="danger"
        :icon="mdiTableOff"
      >
        <b>Empty table.</b> When there's nothing to show
      </NotificationBar>

      <CardBox empty />
    </SectionMain>
  </LayoutAuthenticated>
</template>
