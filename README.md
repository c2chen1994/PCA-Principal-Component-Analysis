# PCA-Principal-Component-

	Background
		Let X be an N × D data matrix, where N is the number of images and D is the number of pixels of
	each image. For a given parameter K < D, use PCA to compress X into an N × K matrix. this is done via first 
	centering the data, then finding the top K eigenvectors of the covariance matrix XTX, and finally projecting 
	the original data onto these eigenvectors. Since each of these eigenvectors has dimensionality D, it can also 
	be represented as an image of the same size as the dataset.

	Compression
		Implement PCA in function pca of pca.py file, which returns the compressed representation Y ∈ RN×K and a matrix 
	M ∈ RD×K that consists of the top K eigenvectors, represented as column vectors. Note that we have subtracted the 
	mean values from the data before passing it to pca, so you do not need to do this step.
	
	Decompression
		With the eigenvector matrix M, we can approximately reconstruct the original dataset as X~ = YMT. Implement
	this step in function decompress of pca.py.
		It is easy to see that larger K leads to better reconstruction. To quantify the reconstruction error
	between the original image x and the reconstructed one ˆx, we calculate the pixel-wise mean-square-error
	as 1/D||x − x~||2. Implement this step in function reconstruction_error of pca.py.

