# AK-Slider
Angular based slider - basic functionality

Directive: ak-slider
Ex: <ak-slider config="sliderConf"></ak-slider> 

$scope.sliderConf = {
			type: "range", // options: data, range
			min: 0.1,
			max: 1.5,
			start: 0.7,
			step: 0.05,
			spacing: "auto", //options: equated, auto
			displayticks: false,
			displayguide: true,
			changeable: true,
			callback: function(data){
				$scope.zoomDemo.zoomValue = data.val;
				$scope.zoomDemo.zoomPercentage = Math.floor($scope.zoomDemo.zoomValue * 100);				
			}
			rangeData: function(data) {
				$scope.creditDemo.creditRangeData = data;
			}
		}
		
Configuration Options:
1. type: 
    Type of slider. Options are -
    range: The slider generates ticks based on min, max and step
    data: The slider uses data (an array) to generate ticks
    
2. min:
    Minimum value of slider ticks. Required for type = range. Not relevant in type = data
    
3. max:
    Maximum value of slider ticks. Required for type = range. Not relevant in type = data
    
4. step:
    Increment step value for slider ticks. Required for type = range. Not relevant in type = data
    
5. start:
    Value at which the slider anchor should star with. Optional. Anchor would sit at minimum value when no start is specified
    
6. spacing:
    Options:
      Auto: The slider generates ticks based on calcualted position for the data value within the slider width
      Equated: All ticks are placed equidistant from each other regardless of the difference in value
      
7. displayticks: 
    Boolean to specify if ticks should be displayed on the slider or not
    
8. displayguide: 
    For future release
    
9. changeable:
    Boolean to allow user to drag the slider anchor
    
10. callback:
    Function that gets called back when the slider moves and when the slider stops. Returns the position of the slider and its corresponding value
    
11. rangeData:
    Function that gets called back when type = range and the range is auto generated. Returns each individual value generated on the slider
    
   
