<template>
    <div class="app-container">
        <el-form :inline="true" :model="formInline" class="demo-form-inline">
            <el-form-item label="审批人">
                <el-input
                    v-model="formInline.user"
                    placeholder="审批人"
                ></el-input>
            </el-form-item>
            <el-form-item label="活动区域">
                <el-select v-model="formInline.region" placeholder="活动区域">
                    <el-option label="区域一" value="shanghai"></el-option>
                    <el-option label="区域二" value="beijing"></el-option>
                </el-select>
            </el-form-item>
            <el-form-item>
                <el-button type="primary" @click="onSubmit">查询</el-button>
            </el-form-item>
        </el-form>
        <el-row>
            <el-button type="success" size="medium">新增</el-button>
            <el-button type="danger" size="medium">删除</el-button>
        </el-row>
        <el-table :data="tableData" border fit stripe>
            <el-table-column prop="date" label="日期" width="180">
            </el-table-column>
            <el-table-column prop="name" label="姓名" width="180">
            </el-table-column>
            <el-table-column prop="address" label="地址"> </el-table-column>
        </el-table>
    </div>
</template>

<script>
export default {
    data() {
        return {
            formInline: {},
            tableData: [
                {
                    date: "2016-05-02",
                    name: "王小虎",
                    address: "上海市普陀区金沙江路 1518 弄"
                },
                {
                    date: "2016-05-04",
                    name: "王小虎",
                    address: "上海市普陀区金沙江路 1517 弄"
                }
            ]
        };
    }
};
</script>

<style>
</style>
