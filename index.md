# greetings
## Coding for my meme
``` library(magick)

#\n for break in text line

#panel 1
Excited_Man <- image_read("https://i.kym-cdn.com/photos/images/newsfeed/001/553/696/a42.jpg") %>%
  image_scale(400)



#panel 2
happy_text <- image_blank(width = 400, height = 534, color ="#000000") %>% 
  image_annotate(text = "Excited to start my \nsecond year at uni",
                 color = "#FFFFFF",size = 37, font = "Impact", gravity = "center") 



#panel 3 
crying_man <- image_read("https://newfastuff.com/wp-content/uploads/2019/02/PMU2Xjq.png") %>%
  image_scale(400)



#panel 4
sad_text <- image_blank(width = 400, height = 400, color ="#000000") %>% 
  image_annotate(text = "Covid and 3 assignments \nin the first week",
                 color = "#FFFFFF",size = 37, font = "Impact", gravity = "center")


#combining 
happy_vector <- c(Excited_Man, happy_text)
First_row <- image_append(happy_vector)

sad_vector <- c(crying_man, sad_text)
second_row <- image_append(sad_vector)

#final
Meme <- c(First_row,second_row) %>%
  image_append(stack = TRUE) %>%
  image_scale(800)

Meme

image_write(Meme, "My_Meme.png")
```

## My Meme produced:
![](My_Meme.png)
