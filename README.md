# homework4a
#urn with 9 balls, 3 green, 3 white, 3 red... draw 3 balls...calculate prob. of drawing all colors WITH replacement
u = 1:9
j = 0
i = 1
while (i <= 1000000) {
  result = sample(u, replace = TRUE, 3)
  if (1 %in% result || 2 %in% result || 3 %in% result) {
    if (4 %in% result || 5 %in% result || 6 %in% result) {
      if (7 %in% result || 8 %in% result || 9 %in% result) {
        j = j + 1
      }
    }
  }
  i = i + 1
}
print(j/1000000)
