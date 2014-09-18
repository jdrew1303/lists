# [ l [ i [ s ] t ] s ] -- ***pending release***

Lists is a library of higher-order functions for working with collections (arrays/objects/strings). The library was inspired directly from Haskell's Data.List module by the powerful people over at [The University of Glasgow](http://www.gla.ac.uk/). You can view the original source [here](https://hackage.haskell.org/package/base-4.7.0.0/docs/src/Data-List.html). You could then scroll through each function closely and see a purposefully similar correlation between the Haskell implementation and [this](www.google.com) implementation.

Use the unorthodox style of passing functions to functions to functions to solve complex problems. Most of the functions featured in Lists produce new arrays, to reinforce the paradigm of stateless programming, which means "retaining no information about previous events".

**Disclaimer**: Almost all of these functions are naive recursive definitions. The idea behind this library is to maximize problem-solving expressivity, that is, this library provides an alternative toolbox by which one could use to solve computational problems. This library should be sufficient for most projects but I recommend using UnderscoreJS for problems that require ~ 1 million iterations until ListsJS provides iterative definitions of its functions.

-----
### Contents

**Basic Functions**

1. append :: [a] -> [a] -> [a]
2. head :: [a] -> a
3. last :: [a] -> a
4. init :: [a] -> [a]
5. tail :: [a] -> [a]
6. nil :: [a] -> Bool

**List Transformations**

7. map :: (a -> b) [a] -> [b]
8. rev :: [a] -> [a]
9. intersperse :: a -> [a] -> [a]
10. intercalate :: [a] -> [[a]] -> [a]
11. transpose :: [[a]] -> [[a]]
12. subsequences :: [a] -> [[a]]
13. permutations :: [a] -> [[a]]

**Reducing Lists (folds)**

14. foldl :: (b -> a -> b) -> b -> [a] -> b
15. foldl1 :: (a -> a -> a) -> [a] -> a
16. foldr :: (a -> b -> b) -> b -> [a] -> b
17. foldr1 :: (a -> a -> a) -> [a] -> a

**Special Folds**

18. flatten || concat :: [[a]] -> [a]
19. concatMap :: (a -> [b]) -> [a] -> [b]
20. and :: [Bool] -> Bool
21. or :: [Bool] -> Bool
22. any :: (a -> Bool) -> [a] -> Bool
23. all :: (a -> Bool) -> [a] -> Bool
24. sum :: Num a => [a] -> a
25. product :: Num a => [a] -> a
26. maximum :: Ord a => [a] -> a
27. minimum :: Ord a => [a] -> a
28. maxList :: Ord a => [a] -> a
29. minList :: Ord a => [a] -> a

**Building Lists**

30. scanl :: (b -> a -> b) -> b -> [a] -> [b]
31. scanr :: (a -> b -> b) -> b -> [a] -> [b]
32. mapAccumL :: (acc -> x -> (acc,y)) -> acc -> [x] -> (acc, [y])
33. iterate :: (a -> a) -> a -> [a]
34. replicate :: Int -> a -> [a]
35. cycle :: [a] -> [a]
36. unfold || unfoldr :: (b -> Maybe (a, b)) -> b -> [a]

**Sublists**

37. take :: Int -> [a] -> [a]
38. drop :: Int -> [a] -> [a]
39. splitAt :: Int -> [a] -> ([a], [a])
40. takeWhile :: (a -> Bool) -> [a] -> [a]
41. dropWhile :: (a -> Bool) -> [a] -> [a]
42. span :: (a -> Bool) -> [a] -> ([a], [a])
43. break :: (a -> Bool) -> [a] -> ([a], [a])
44. stripPrefix :: Eq a => [a] -> [a] -> Maybe [a]
45. group :: Eq a => [a] -> [[a]]
46. 
