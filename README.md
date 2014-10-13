video-hadoop-template
=====================
This project aims to implement video processing on Hadoop. We cutomize the `FileInputFormat` and  `RecordReader` class in Hadoop. Please follow the following steps to run a demo job.


###Step 1
Clone the repository.

	git clone git@github.com:xmpy/video-hadoop-template.git

###Step 2
Build this project.

	mvn assembly:assembly
	
###Step 3
Run the jar.
	
	hadoop jar  target/metadata-0.0.1-SNAPSHOT.jar edu.bupt.videodatacenter.input.MRVideoReader /user/zhaoxm/vehicle_1min.avi /user/zhaoxm/metadata_output2
	
The last two argument are the `input video path` and `output path`.

### Step 4
See result. First column is the key, which is filename_framecount. Second column is the metadata of this frame image.

	vehicle_1min.avi_1      BufferedImage@19ed13da: type = 5 ColorModel: #pixelBits = 24 numComponents = 3 color space = java.awt.color.ICC_ColorSpace@1bb25a82 transparency = 1 has alpha = false isAlphaPre = false ByteInterleavedRaster: width = 640 height = 360 #numDataElements 3 dataOff[0] = 2
		
	vehicle_1min.avi_10     BufferedImage@19412332: type = 5 ColorModel: #pixelBits = 24 numComponents = 3 color space = java.awt.color.ICC_ColorSpace@1bb25a82 transparency = 1 has alpha = false isAlphaPre = false ByteInterleavedRaster: width = 640 height = 360 #numDataElements 3 dataOff[0] = 2
