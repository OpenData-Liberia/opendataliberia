<script lang="ts">
    const allBlogPosts = [
        {
            id: 1,
            title: "Leveraging Open Data for Economic Growth in Liberia",
            excerpt:
                "Explore how open data initiatives are driving economic development and attracting investment in Liberia.",
            date: "2024-03-15",
            readTime: "5 min read",
            author: "John Doe",
        },
        {
            id: 2,
            title: "The Impact of Open Health Data on Public Health Policies",
            excerpt:
                "Discover how access to open health data is shaping public health strategies and improving healthcare outcomes in Liberia.",
            date: "2024-03-10",
            readTime: "7 min read",
            author: "Jane Smith",
        },
        {
            id: 3,
            title: "Open Education Data: Transforming Liberia's Education System",
            excerpt:
                "Learn how open education data is being used to identify gaps, allocate resources, and improve educational outcomes across Liberia.",
            date: "2024-03-05",
            readTime: "6 min read",
            author: "Robert Johnson",
        },
        {
            id: 4,
            title: "The Role of Open Data in Liberia's Agricultural Sector",
            excerpt:
                "Examine how open data is revolutionizing farming practices and boosting agricultural productivity in Liberia.",
            date: "2024-02-28",
            readTime: "8 min read",
            author: "Emily Brown",
        },
        {
            id: 5,
            title: "Open Data and Transparency in Liberian Government",
            excerpt:
                "Analyze the impact of open data initiatives on government transparency and accountability in Liberia.",
            date: "2024-02-20",
            readTime: "6 min read",
            author: "Michael Wilson",
        },
    ];
</script>

<main class="flex-grow container mx-auto px-4 py-12">
    <h1 class="text-4xl font-bold mb-8 text-center">OpenDataLiberia Blog</h1>

    <div class="max-w-3xl mx-auto mb-8">
        <div class="relative">
            <input
                type="text"
                id="search"
                placeholder="Search blog posts..."
                class="w-full p-2 pl-10 border rounded-md"
            />
            <i
                data-lucide="search"
                class="absolute left-3 top-1/2 transform -translate-y-1/2 text-gray-400"
            ></i>
        </div>
    </div>

    <div id="blog-posts" class="max-w-3xl mx-auto space-y-12">
        <!-- Blog posts will be dynamically inserted here -->
        {#each allBlogPosts as post}
            <article class="border-b pb-8">
                <h2 class="text-2xl font-semibold mb-2">
                    <a href="blog-post.html?id=${post.id}" class="hover:text-[#1B3B67]">
                        {post.title}
                    </a>
                </h2>
                <div class="flex items-center text-gray-600 text-sm mb-4">
                    <i data-lucide="calendar" class="h-4 w-4 mr-2"></i>
                    <span>{post.date}</span>
                    <i data-lucide="clock" class="h-4 w-4 ml-4 mr-2"></i>
                    <span>{post.readTime}</span>
                    <span class="ml-4">By {post.author}</span>
                </div>
                <p class="text-gray-700">{post.excerpt}</p>
                <a href="blog-post.html?id={post.id}" class="inline-block mt-4 text-[#1B3B67] font-medium hover:underline">
                    Read more
                </a>
            </article>
        {/each}
    </div>

    <div
        id="pagination"
        class="flex justify-center items-center space-x-4 mt-12"
    >
        <!-- Pagination controls will be dynamically inserted here -->
    </div>
</main>
