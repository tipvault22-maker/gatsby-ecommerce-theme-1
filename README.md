import { Button } from "@/components/ui/button";
import { ArrowRight, Headphones, Shirt, Package, TrendingUp } from "lucide-react";
import audioImage from "@/assets/audio-category.jpg";
import tshirtImage from "@/assets/tshirt-category.jpg";

const categories = [
{
title: "Audio Products",
description: "Audiobooks, podcasts, music, and digital audio content",
image: audioImage,
icon: Headphones,
color: "bg-audio-player text-audio-controls",
stats: "2,500+ products",
trending: "+15% this month"
},
{
title: "T-shirts & Apparel",
description: "Custom designs, print-on-demand, and branded merchandise",
image: tshirtImage,
icon: Shirt,
color: "bg-secondary text-secondary-foreground",
stats: "1,200+ designs",
trending: "+23% this month"
},
{
title: "Products",
description: "Curated products from verified suppliers worldwide",
image: "https://images.unsplash.com/photo-1586953208448-b95a79798f07?w=800&h=600&fit=crop&crop=center",
icon: Package,
color: "bg-primary text-primary-foreground",
stats: "5,000+ products",
trending: "+31% this month"
}
];

export default function CategorySection() {
return (
<section className="py-20 bg-muted/30">
<div className="container mx-auto px-4">
<div className="text-center mb-16">
<h2 className="text-3xl lg:text-5xl font-bold mb-4">
Explore Our <span className="text-primary">Categories</span>
</h2>
<p className="text-xl text-muted-foreground max-w-2xl mx-auto">
Discover thousands of products across multiple categories. Start selling in minutes with our comprehensive marketplace.
</p>
</div>

<div className="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
{categories.map((category, index) => {
const Icon = category.icon;
return (
<div
key={index}
className="group relative overflow-hidden rounded-xl bg-card hover:shadow-hover transition-all duration-300 hover:-translate-y-2"
>
{/* Background Image */}
<div className="relative h-64 overflow-hidden">
<img
src={category.image}
alt={category.title}
className="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500"
/>
<div className="absolute inset-0 bg-gradient-to-t from-black/80 via-black/20 to-transparent"></div>

{/* Category Icon */}
<div className={`absolute top-4 left-4 p-3 rounded-lg ${category.color} shadow-card`}>
<Icon className="h-6 w-6" />
</div>

{/* Trending Badge */}
<div className="absolute top-4 right-4 bg-success text-success-foreground px-3 py-1 rounded-full text-sm font-medium flex items-center space-x-1">
<TrendingUp className="h-3 w-3" />
<span>{category.trending}</span>
</div>
</div>

{/* Content */}
<div className="p-6">
<h3 className="text-xl font-bold mb-2 group-hover:text-primary transition-colors">
{category.title}
</h3>
<p className="text-muted-foreground mb-4">
{category.description}
</p>

<div className="flex items-center justify-between mb-4">
<span className="text-sm font-medium text-primary">
{category.stats}
</span>
</div>

<Button
className="w-full group/btn"
variant="outline"
>
Explore Category
<ArrowRight className="h-4 w-4 ml-2 group-hover/btn:translate-x-1 transition-transform" />
</Button>
</div>
</div>
);
})}
</div>

{/* Call to Action */}
<div className="text-center mt-16">
<Button variant="premium" size="lg">
View All Categories
<ArrowRight className="h-5 w-5 ml-2" />
</Button>
</div>
</div>
</section>
);
}


  ```

 
