<style scoped>
 .mapouter{
     position:relative;
     text-align:right;
     height:260px;
     width:260px;
 }
 .gmap_canvas {
     overflow:hidden;
     background:none!important;
     height:260px;
     width:260px;
 }
</style>

<template>

<!--    <div role="status" class="p-4 space-y-4 rounded border border-gray-200 divide-y divide-gray-200 shadow animate-pulse light:divide-gray-700 md:p-6 light:border-gray-700">-->
<!--        <div class="flex justify-between items-center">-->
<!--            <div style="width: 100%;">-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-80 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-40 mb-2.5" style="background: #0a0;"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40"></div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex justify-between items-center pt-4">-->
<!--            <div style="width: 100%;">-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-80 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-40 mb-2.5" style="background: #a00;"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40"></div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex justify-between items-center pt-4">-->
<!--            <div style="width: 100%;">-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-80 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-40 mb-2.5" style="background: #0a0;"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40"></div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex justify-between items-center pt-4">-->
<!--            <div style="width: 100%;">-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-80 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-40 mb-2.5" style="background: #a00;"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40"></div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex justify-between items-center pt-4">-->
<!--            <div style="width: 100%;">-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-80 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-40 mb-2.5" style="background: #0a0;"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40"></div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <div class="flex justify-between items-center pt-4">-->
<!--            <div style="width: 100%;">-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-80 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-40 mb-2.5" style="background: #a00;"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-2 bg-gray-200 rounded-full light:bg-gray-700 w-100 mb-2.5"></div>-->
<!--                <div class="h-4 bg-gray-300 rounded-full light:bg-gray-600 w-40"></div>-->
<!--            </div>-->
<!--        </div>-->
<!--        <span class="sr-only">Loading...</span>-->
<!--    </div>-->

    <div class="pt-3 mt-5">
        <h1 class="mt-3 text-lg font-semibold sm:text-slate-900 text-4xl light:sm:text-black mb-5">Dog walk locations</h1>

        <div class="max-w-sm w-full lg:max-w-full lg:flex mb-5">
            <div class="h-48 lg:h-auto lg:w-48 flex-none bg-cover rounded-t lg:rounded-t-none lg:rounded-l text-center overflow-hidden" title="Woman holding a mug">
                <div class="mapouter">
                    <div class="gmap_canvas">
                        <iframe width="260" height="260" id="gmap_canvas" src="https://maps.google.com/maps?q=Beacon%20Wood%20Country%20Park&t=&z=13&ie=UTF8&iwloc=&output=embed" frameborder="0" scrolling="no" marginheight="0" marginwidth="0"></iframe><a href="https://fmovies-online.net"></a><br>
                        <a href="https://www.embedgooglemap.net">google embed map</a>
                    </div>
                </div>
            </div>
            <div class="border-r border-b border-l border-gray-400 lg:border-l-0 lg:border-t lg:border-gray-400 bg-white rounded-b lg:rounded-b-none lg:rounded-r p-4 flex flex-col justify-between leading-normal">
                <div class="mb-8">
                    <p class="text-sm text-gray-600 flex items-center">
                        <svg class="fill-current text-gray-500 w-3 h-3 mr-2" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                            <path d="M4 8V6a6 6 0 1 1 12 0v2h1a2 2 0 0 1 2 2v8a2 2 0 0 1-2 2H3a2 2 0 0 1-2-2v-8c0-1.1.9-2 2-2h1zm5 6.73V17h2v-2.27a2 2 0 1 0-2 0zM7 6v2h6V6a3 3 0 0 0-6 0z" />
                        </svg>
                        Rember money for parking
                    </p>
                    <div class="text-gray-900 font-bold text-xl mb-2">{{currentDateTime()}}</div>
                    <p class="text-gray-700 text-base">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Voluptatibus quia, nulla! Maiores et perferendis eaque, exercitationem praesentium nihil.</p>
                </div>
            </div>
        </div>

        <div style="margin-top: 50px !important;" class="mb-2 mb-5 mt-5" v-for="(article, index) in articles" v-bind:key="article.id" >
            <div v-if="index == articles.length -1">
                <h2 class="mt-1 text-lg font-semibold sm:text-slate-900 md:text-2xl dark:sm:text-black">{{ article.title }}</h2>
                <a class="text-sm leading-4 font-medium sm:text-slate-500 light:sm:text-slate-400" target="_blank" :href="article.map_url">Show in Google Maps</a>
                <p v-if="article.status == 0" style="color:#75933e;">Not visited</p>
                <p v-else style="color:#ce2761;">Visited</p>
                <p class="mt-2 text-sm leading-6 col-start-1 sm:col-span-2 lg:mt-2 lg:row-start-4 lg:col-span-1 light:text-slate-400">
                    {{ article.body }}
                </p>
                <button @click="editArticle(article)" type="button" class="mt-3 bg-indigo-600 text-white text-sm leading-6 font-medium py-2 px-3 rounded-lg">Edit</button>
                <button @click="deleteArticle(article.id)" type="button" class="ml-3 mt-3 bg-red-600 text-white text-sm leading-6 font-medium py-2 px-3 rounded-lg">Delete</button>
            </div>
            <div v-else style="border-bottom: 1px solid #ddd; width: 100%; padding-bottom: 30px; margin-bottom: 30px;">
                <h2 class="mt-1 text-lg font-semibold sm:text-slate-900 md:text-2xl dark:sm:text-black">{{ article.title }}</h2>
                <a class="text-sm leading-4 font-medium sm:text-slate-500 light:sm:text-slate-400" target="_blank" :href="article.map_url">Show in Google Maps</a>
                <p v-if="article.status == 0" style="color:#75933e;">Not visited</p>
                <p v-else style="color:#ce2761;">Visited</p>
                <p class="mt-2 text-sm leading-6 col-start-1 sm:col-span-2 lg:mt-2 lg:row-start-4 lg:col-span-1 light:text-slate-400">
                    {{ article.body }}
                </p>
                <button @click="editArticle(article)" type="button" class="mt-3 bg-indigo-600 text-white text-sm leading-6 font-medium py-2 px-3 rounded-lg">Edit</button>
                <button @click="deleteArticle(article.id)" type="button" class="ml-3 mt-3 bg-red-600 text-white text-sm leading-6 font-medium py-2 px-3 rounded-lg">Delete</button>
            </div>

        </div>
    </div>
    <div class="bg-white px-4 py-3 flex items-center justify-between sm:px-6">
        <div class="flex-1 flex justify-between sm:hidden">
            <a href="#" v-bind:class="[{disabled: !pagination.prev_page_url}]" class="relative inline-flex items-center px-4 py-2 border border-gray-300 text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50" @click="fetchArticles(pagination.prev_page_url)"> Previous </a>
            <a href="#" v-bind:class="[{disabled: !pagination.next_page_url}]" class="ml-3 relative inline-flex items-center px-4 py-2 border border-gray-300 text-sm font-medium rounded-md text-gray-700 bg-white hover:bg-gray-50" @click="fetchArticles(pagination.next_page_url)"> Next </a>
        </div>
        <div class="hidden sm:flex-1 sm:flex sm:items-center sm:justify-between">
            <div>
                <nav class="relative z-0 inline-flex rounded-md shadow-sm -space-x-px" aria-label="Pagination">
                    <a href="#" v-bind:class="[{disabled: !pagination.prev_page_url}]" class="relative inline-flex items-center px-2 py-2 rounded-l-md border border-gray-300 bg-white text-sm font-medium text-gray-500 hover:bg-gray-50" @click="fetchArticles(pagination.prev_page_url)">
                        <span class="sr-only">Previous</span>
                        <!-- Heroicon name: solid/chevron-left -->
                        <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                            <path fill-rule="evenodd" d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z" clip-rule="evenodd" />
                        </svg>
                    </a>
                    <!-- Current: "z-10 bg-indigo-50 border-indigo-500 text-indigo-600", Default: "bg-white border-gray-300 text-gray-500 hover:bg-gray-50" -->
                    <span class="relative inline-flex items-center px-4 py-2 border border-gray-300 bg-white text-sm font-medium text-gray-700"> {{ pagination.current_page }} of {{ pagination.last_page }} </span>
                    <a href="#" v-bind:class="[{disabled: !pagination.next_page_url}]" class="relative inline-flex items-center px-2 py-2 rounded-r-md border border-gray-300 bg-white text-sm font-medium text-gray-500 hover:bg-gray-50" @click="fetchArticles(pagination.next_page_url)">
                        <span class="sr-only">Next</span>
                        <!-- Heroicon name: solid/chevron-right -->
                        <svg class="h-5 w-5" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
                            <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd" />
                        </svg>
                    </a>
                </nav>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Articles",
    data() {
        return {
            articles: [],
            article: {
                id: '',
                title: '',
                status: false,
                map_url: '',
                body: ''
            },
            article_id: '',
            pagination: {},
            edit: false,
        };
    },

    created() {
        this.fetchArticles();
    },

    methods: {
        startOfWeek(date) {

            var day = date.getDate();

            switch (new Date().getDay()) {
                case 0:
                    day = date.getDate()+7;
                    break;
                case 1:
                    day = date.getDate()+5;
                    break;
                case 2:
                    day = date.getDate()+4;
                    break;
                case 3:
                    day = date.getDate()+3;
                    break;
                case 4:
                    day = date.getDate()+2;
                    break;
                case 5:
                    day = date.getDate()+1;
                    break;
                case 6:
                    day = "Saturday";
            }

            return day;
        },
        currentDateTime() {
            const current = new Date();

            var month = current.toLocaleString('default', { month: 'long' });

            return "Coming up Saturday " + this.startOfWeek(current).toString() + " " + month;
        },
        fetchArticles(page_url) {
            let vm = this;
            page_url = page_url || 'api/articles';
            fetch(page_url)
                .then(res => res.json())
                .then(res => {
                    this.articles = res.data;
                    vm.makePagination(res.meta, res.links);
                })
                .catch(err => console.log(err));
        },
        makePagination(meta, links) {
            let pagination = {
                current_page: meta.current_page,
                last_page: meta.last_page,
                next_page_url: links.next,
                prev_page_url: links.prev
            };

            this.pagination = pagination;
        },
        deleteArticle(id) {
            if (confirm('Are You Sure?')) {
                fetch(`api/article/${id}`, {
                    method: 'delete'
                })
                    .then(res => res.json())
                    .then(data => {
                        alert('Article Removed');
                        this.fetchArticles();
                    })
                    .catch(err => console.log(err));
            }
        },
        addArticle() {
            if (this.edit === false) {
                // Add
                fetch('api/article', {
                    method: 'post',
                    body: JSON.stringify(this.article),
                    headers: {
                        'content-type': 'application/json'
                    }
                })
                    .then(res => res.json())
                    .then(data => {
                        this.clearForm();
                        alert('Article Added');
                        this.fetchArticles();
                    })
                    .catch(err => console.log(err));
            } else {
                // Update
                fetch('api/article', {
                    method: 'put',
                    body: JSON.stringify(this.article),
                    headers: {
                        'content-type': 'application/json'
                    }
                })
                    .then(res => res.json())
                    .then(data => {
                        this.clearForm();
                        alert('Article Updated');
                        this.fetchArticles();
                    })
                    .catch(err => console.log(err));
            }
        },
        editArticle(article) {
            this.edit = true;
            this.article.id = article.id;
            this.article.article_id = article.id;
            this.article.title = article.title;
            this.article.body = article.body;
        },
        clearForm() {
            this.edit = false;
            this.article.id = null;
            this.article.article_id = null;
            this.article.title = '';
            this.article.body = '';
        }
    }
};
</script>

