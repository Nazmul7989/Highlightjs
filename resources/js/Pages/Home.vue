<script setup>
import {Link} from "@inertiajs/vue3";
import {onMounted,onUpdated} from "vue";
import hljs from 'highlight.js';

onMounted(()=> {
    hljs.highlightAll();
})

onUpdated(()=>{
    hljs.highlightAll();
})

</script>

<template>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
        <div class="container">
            <Link class="navbar-brand" href="/">Navbar</Link>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarSupportedContent">
                <ul class="navbar-nav me-auto mb-2 mb-lg-0">
                    <li class="nav-item">
                        <Link class="nav-link active" aria-current="page" href="/">Home</Link>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">About</a>
                    </li>
                </ul>
                <form class="d-flex" role="search">
                    <input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
                    <button class="btn btn-outline-success" type="submit">Search</button>
                </form>
            </div>
        </div>
    </nav>
    <div class="container mt-3">
        <div class="row">
            <div class="col-12">
                <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    <pre>
                        <code>
                        $products = ProductFilterResource::collection(
            QueryBuilder::for(Product::class)
                ->allowedFilters($this->allowedFilters())
                ->where('live_at', '!=', null)
                ->where(function ($query) {
                    $query->whereHas('variations.stocks', function ($subquery) {
                        $subquery->where('amount', '>', 0);
                    })->orWhere('show_evenif_stockout', true);
                })
                ->with(['brand', 'media', 'comments', 'categories','variations.product', 'variations.stocks', 'variations' => function ($query) {
                    $query->withSum('stocks', 'amount');
                },'categories' => function($q){
                    $q->where('status', true);
                }])
                ->paginate()
                ->appends($request->query())
        );
                        </code>
                    </pre>
                    Error est fugiat nostrum. Rerum saepe sit temporibus voluptates. Accusamus architecto assumenda beatae commodi distinctio ea, eius et excepturi, impedit ipsa iure laborum libero nemo officia optio perferendis sunt! Consequatur debitis facilis in magni, mollitia obcaecati officiis? A ab adipisci asperiores aspernatur, atque consectetur culpa cumque delectus, deserunt dicta distinctio eius enim et ex explicabo illo ipsa itaque iure laboriosam libero magnam maxime molestias natus obcaecati odit optio porro quasi quibusdam quos recusandae reiciendis rerum sequi ut. Ducimus, eaque enim et ex exercitationem facere optio quia. Accusamus aliquid aspernatur at autem blanditiis commodi delectus eligendi, excepturi exercitationem fuga iste itaque laudantium, libero nemo nulla numquam odio odit perferendis porro praesentium quidem quis recusandae repellendus saepe voluptatibus. Accusamus ad amet consectetur culpa eius esse expedita illo iusto nihil provident quasi quibusdam rem repellendus, repudiandae rerum sapiente sit sunt, voluptatum? Ad amet animi aspernatur blanditiis consectetur consequuntur cum esse expedita explicabo fuga illo laborum minima minus mollitia non nostrum obcaecati officia perspiciatis placeat qui recusandae reiciendis, tempora tempore vel veniam veritatis voluptatibus, voluptatum. Consequuntur culpa earum est natus quibusdam sequi veniam. Eaque error itaque molestias praesentium similique.</div>
            </div>
        </div>
    </div>
</template>
