# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Zero-Inflated Negative Binomial Mixed Models Use glmm.zinb (NBZIMM) With (In) R Software
install.packages("remotes")
remotes::install_github("nyiuab/NBZIMM")
library("NBZIMM")
# Estimate Zero-Inflated Negative Binomial Mixed Models Use glmm.zinb (NBZIMM) With (In) R Software
glmm.zinb = read.csv("https://raw.githubusercontent.com/timbulwidodostp/glmm.zinb/main/glmm.zinb/glmm.zinb.csv",sep = ";")
glmm.zinb_Y <- glmm.zinb$glmm.zinb
glmm.zinb_X1 <- glmm.zinb$glmm.zinb_1
glmm.zinb_X2 <- glmm.zinb$glmm.zinb_2
glmm.zinb_X3 <- glmm.zinb$glmm.zinb_3
glmm.zinb_X4 <- glmm.zinb$glmm.zinb_4
glmm.zinb_X5 <- glmm.zinb$glmm.zinb_5
glmm.zinb_X6 <- glmm.zinb$glmm.zinb_6
glmm.zinb_ <- data.frame(glmm.zinb_Y, glmm.zinb_X1, glmm.zinb_X2, glmm.zinb_X3, glmm.zinb_X4, glmm.zinb_X5, glmm.zinb_X6)
glmm.zinb = glmm.zinb(fixed = glmm.zinb_Y ~ glmm.zinb_X1 + glmm.zinb_X2 + glmm.zinb_X3 
+ glmm.zinb_X4 + glmm.zinb_X5, random = ~ 1 | glmm.zinb_X6, data = glmm.zinb_, zi_fixed = ~1)
summary(glmm.zinb)
# Zero-Inflated Negative Binomial Mixed Models Use glmm.zinb (NBZIMM) With (In) R Software
# Olah Data Semarang
# WhatsApp : +6285227746673
# IG : @olahdatasemarang_
# Finished
