

# EMCVImage

A wrapped image class. The default color format should be BGR when image opened from file.


- **[ObjC]**: Means this property or method can be used on Objective-C.
- **[ObjC++]**: Means this property or method can only be used on Objective-C++.

# Property

- **[ObjC++]**: `_mat`: A `cv::Mat` object. It's image data.
- **[ObjC++]**: `_hist`: A `cv::MatND` object. It's histogram data.
- **[ObjC]**: `channalCount`: How much channals in current image;
- **[ObjC]**: `imageSize`: Get size of the image.

# Instance Method

## Initialization

- **[ObjC++]**: `initWithMat`: Init a instance with a `cv::Mat`.
- **[ObjC++]**: `initWithNoCopyMat`: Init a instance with a `cv::Mat` and will not copy memory.
- **[ObjC++]**: `initWithMat:cvtColor`: Init a instance with a `cv::Mat` and color format like `CV_BGR2RGB` whitch is defined by OpenCV.
- **[ObjC]**: `initWithPath`: Open a local image file with a `NSString` path.
- **[ObjC]**: `initWithSize:andType:andColor`: Init a empty `EMCVImage` instance with type and color. Type must be like `CV_8UC3` whitch is defined by OpenCV. Color is a RGB value array.
- **[ObjC]**: `initWithCVImage`: Init a instance with a `EMCVImage` instance. Means to make a copy.
- **[ObjC]**: `initWithCVImage:cvtColor`: Init a instance with a `EMCVImage` instance and color format. like `CV_BGR2RGB` whitch is defined by OpenCV.
- **[ObjC]**: `initWithCVSplitedImage`: Init a instance with a `EMCVSpritedImage` instance. Means to merge multi channel image.
- **[ObjC]**: `initWithCVSplitedImage:atChannal`: Init a instance with one of a `EMCVSpritedImage` instance's channal image.

## Others

- **[ObjC]**: `makeACopy`: Make a copy. It will copy memory.
- **[ObjC]**: `cvtColor`: Converts image from one color space to another. the Param must be like `CV_BGR2RGB` whitch is defined by OpenCV. The same as `cv::cvtColor`.
- **[ObjC]**: `pyrUpWithRatio`: PyrUp with a ratio.
- **[ObjC]**: `pyrDownWithRatio`: PyrDown with a ratio.
- **[ObjC]**: `splitImage`: Split image's channels.
- **[ObjC]**: `toImage`: Converts image to a `NSImage` instance.
- **[ObjC]**: `calHistWithSize:range`: Calculate histogram using all channals with the same size and range.
- **[ObjC]**: `calHistWithDims:size:range`: Calculate histogram with the same size and range.
- **[ObjC]**: `calHistWithDims:sizes:ranges`: Calculate histogram with the sizes and ranges.
- **[ObjC]**: `normalizeHistWithValue`: Normalize histogram to some value.
- **[ObjC]**: `drawALineWithPoint:andPoint:andColor:andThickness`:Draw a line with specified points, color and thickness. 
- **[ObjC]**: `drawARectWithCenter:size:rgbColor:thickness`: Draw a rect with specified center, size and thickness.
- **[ObjC]**: `drawARect:rgbColor:thickness`: Draw a rect with specified rect and thickness.
- **[ObjC]**: `drawACircleWithCenter:andRadius:andColor:andThickness`: Draw a circle with specified center, radius, color and thickness.	
- **[ObjC]**: `blurWithSize`: Use Normalized Box Filter to smooth a image.
- **[ObjC]**: `medianBlurWithSize`: Use Median Filter to smooth a image.
- **[ObjC]**: `bilateralFilterWithDelta:andSigmaColor:andSigmaSpace`: Use Bilateral Filter to smooth a image.
- **[ObjC]**: `gaussianBlurWithSize`: Do Gaussian Blur with a specified kernel size.


# Class Method

empty

