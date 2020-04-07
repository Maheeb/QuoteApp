<template>
    <div class="row">

        <form>
                <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
            <!--<div class="col-md-12">-->
                    <label for="">Quote</label>

                    <textarea  class="form-control" cols="100" rows="6" style="width: 100%" v-model="quote"></textarea>
                </div>
            <div class="col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3 form-group">
                <!--<label for="">Quote</label>-->
               <button class="btn btn-primary" @click.prevent="CreateNew">Add Quote</button>
            </div>
        </form>


    </div>
</template>

<script>
    export default {
        data:function () {
            return {

                quotes: ''
            };
        },
        methods:{
            CreateNew(){
                this.$emit('quoteAdded', this.quote)
                this.quote='';

            }

        }
    }
</script>

<style scoped>

</style>