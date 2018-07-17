# CIGraphLib Graphing Library

### CIGraphLib is a lightweight PHP graphing library based on the open source PHPGraphLib project that creates slick graphs for usage in your CodeIgniter framework based application.

Since CodeIgniter framework doesn't come with a graphing library included, I decided to adopt one and fork it to make if fully CodeIgniter compatible. The reasons because I choosed PHPGraphLib as a base for my project are three:

1. It's simple. It's programmed in a very clear and simple way, without being bloat by unnecesary functionality.
2. It's lightweight. Even though it uses the GD library it is very fast to be an image generation library.
3. It's very easy to adapt and integrate into CodeIgniter which is my favorite PHP framework.

As it parent, CIGraphLib has some powerful customization features, allowing you to generate the bar, line, stacked bar, or pie graphs for any application based on CodeIgniter, but as an added bonus you can also customize all the fonts used in the graphs. Used with dynamic data, allows easy visual interpretation of sophisticated data sets. Simply feed CIGraphLib an array of data points, and it will generate a .png chart of your data dynamically for browser display or saved to your filesystem.

### History

In this first version of CIGraphLib I have included functionality to customize only the graph title font family and size, but I'm currently working on adding font customization for all the text on the graph so you can use ttf fonts anywhere in your chart.
This has been tested on PHP versions 5.6.18 and 7.0.3, which are the versions I have on my WAMP powered local development machine, but having GD enabled in PHP it should work in other versions of PHP too, feel free to give it a test and report any bug you find on it.

### Documentation

Documentation is a work in progress yet but it will be available soon. In the meantime you can use the PHPGraphLib documentation as a starting point which is available at [http://www.ebrueggeman.com/phpgraphlib](http://www.ebrueggeman.com/phpgraphlib) and see the following added features.

### Added features

#### setTitleFont (string $fontfile)

Uses the ttf file specified in $fontfile to format the graph title. You can place the ttf file in any folder you like but remember to reference it related to the root of your CodeIgniter folder. For example: if you have a font file named Roboto-Regular.ttf inside a fonts folder at the root of your project you should use this function inside your CodeIgniter code like this:

$this->load->library('Cigraphlib');
$this->cigraphlib->setTitleFont('fonts/Roboto-Regular.ttf');

#### setTitleFontSize (integer $fontsize)

Size in points of the ttf font used to format the graph title. The library automatically calculates the size in pixels used by it to fit it into the graph. It's set to 16 points by default. In case you want to set it to 20 points and continuing with the previous example code you just need to add the following line of code:

$this->cigraphlib->setTitleFontSize(20);

I will be adding more features to this library so keep updated!

