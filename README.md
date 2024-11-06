## Myntra Product Dataset Processing
This project focuses on data cleaning and transformation of the Myntra product dataset, containing details about various products, such as names, brands, prices, discounts, ratings, and other attributes.

## Dataset Overview
The initial dataset includes the following columns:

1. product_name: Name of the product.
2. brand_name: Brand of the product.
3. rating: Average rating of the product.
4. rating_count: Number of ratings received.
5. marked_price: Original price of the product.
6. discounted_price: Price after discount.
7. sizes: Available sizes.
8. product_link: URL to the product page.
9. img_link: URL to the product image.
10. product_tag: Category tag (e.g., "wallets," "flip-flops").
11. brand_tag: Brand tag for filtering purposes.
12. discount_amount: Discount amount applied.
13. discount_percent: Discount percentage applied.

#### The dataset initially had 168,029 rows and 13 columns.

#### Data Transformation Steps

1. Adding product_id Column
Extracted a unique product_id from the product_link URL by isolating the ID portion. This helps in uniquely identifying products.

2. Creating product_description Column
Generated a product_description column by extracting descriptive information from the product_link. This provides a brief description of each product.

3. Adding price_range Column
Added a price_range column based on discounted_price to categorize products into price bands:

"Rs 0 - Rs 500" for products priced up to 500.
"Rs 500 - Rs 1000" for products priced between 500 and 1000.
"Rs 1000 - Rs 2000" for products priced between 1000 and 2000.
"Rs 2000 - Rs 5000" for products priced above 2000.

Final Dataset Structure
After processing, the dataset now has 16 columns:

The original 13 columns.
product_id: Unique identifier for each product.
product_description: A brief description generated from product_link.
price_range: Categorized price range.

# Contributing

**Contributions are welcome! If you have ideas for enhancements or spot any issues, feel free to submit a pull request.**
