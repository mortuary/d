
// image URLs or even binary code from image files.
// All sorted in order to appear.
$frames = array(
    imagecreatefrompng("/../images/pic1.png"), // Resource var
    "/../images/pic2.png", // Image file path
    file_get_contents("/../images/pic3.jpg"), // Binary source code
    'http://thisisafakedomain.com/images/pic4.jpg', // URL
);

// Create an array containing the duration (in millisecond) of each frames (in order too)
$durations = array(40, 80, 40, 20);

// Initialize and create the GIF !
$gc = new GifCreator();
$gc->create($frames, $durations, 5);

