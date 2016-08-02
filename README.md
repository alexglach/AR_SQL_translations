Part I
1. User.all
2. User.find(1)
3. Post.first
4. User.joins(:posts).where("created_at >= ?", "2014-08-31 00:00:00")
5. User.select("COUNT(*) AS color_count").group(:favorite_color).having("color_count > ?", 1)
6. User.order("created_at DESC").first
7. User.order(:age).last
8. User.all
9. Post.order("created_at DESC")

Part II
1. SELECT * FROM posts

2. SELECT * FROM posts LIMIT 1

3. 
SELECT * 
FROM posts 
ORDER BY DESC 
LIMIT 1

4. 
SELECT *
FROM posts
WHERE posts.id = 4

5.
SELECT *
FROM posts
WHERE posts.id = 4

6.
SELECT COUNT(*)
FROM users

7.
SELECT posts.name
FROM posts
WHERE posts.created_at > (CURRENT_DATE - INTERVAL 3 DAY)
ORDER BY created_at

8.
SELECT COUNT(*)
FROM posts
GROUP BY posts.category_id

9.
SELECT posts.*
FROM posts
WHERE EXTRACT(YEAR FROM posts.created_at) < 2014

10.
FROM users JOIN posts ON users.post