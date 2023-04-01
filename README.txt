How to run?

First install numpy, os, cv2 libraries using pip
Then run it using colab, jupyter notebook or dataspell.

********

What are the functions?

image_stats(x) => returns a tuple of the Mean and Std for LAB channels
return (lMean, lStd, aMean, aStd, bMean, bStd)

transfer_img(source_img, target_img) => returns color transferred image using formula
return transfer

ssd(X,Y) => returns SSD
return np.sum((X - Y) ** 2)

cor(X, Y) => returns NCC
return np.sum(X * Y) / np.sum(X) / np.sum(Y)

ssd_and_cor(X, Y) => returns multiple of SSD and NCC
return ssd(X, Y) * cor(X, Y)

split(img, m, n) => split image into m*n equal parts, and returns subimages array
return imgs

concat_vh(list_2d) => concatenate m*n equal parts, and returns an image
return cv.vconcat(np.array(arr))

func(sImg, tImg, method) => divide image into m*n parts, and calculates the mean of a method (ssd, cor, ssd_and_cor) for every (m,n) values, and transfer colors looking at this data then concatenate final images and returns a dict for every m,n values
return imgs
