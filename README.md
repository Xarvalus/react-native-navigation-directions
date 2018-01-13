[![NPM version](https://img.shields.io/npm/v/react-native-navigation-directions.svg?style=flat-square)](https://www.npmjs.com/package/react-native-navigation-directions)
[![Build](https://travis-ci.org/laki944/react-native-navigation-directions.svg?branch=master)](https://travis-ci.org/laki944/react-native-navigation-directions)
[![js-standard-style](https://img.shields.io/badge/code%20style-standard-brightgreen.svg)](http://standardjs.com/)

# react-native-navigation-directions

A simple module which allows you to open default navigation app(**IOS**: Apple Maps, **Android**: Google Maps) with drive direction between two points. After open the navigation app OpenMapDirections receive callback. Also work with the EXPO(https://expo.io/).

![alt text](https://media.giphy.com/media/3oFzmgxYq1MctUbXTW/giphy.gif)

**Example:**

    import { OpenMapDirections} from 'react-native-navigation-directions';
    
	export default class App extends React.Component {
	 _callShowDirections = () => {
	    const startPoint = {
	      longitude: -8.945406,
	      latitude: 38.575078
	    } 

	    const endPoint = {
	      longitude: -8.9454275,
	      latitude: 38.5722429
	    }

	    OpenMapDirections(startPoint, endPoint).then(res => {
	      console.log(res)
	    });
	  }
	  
	  render() {
	    return (
	      <View style={styles.container}>
	        <Text>Show direction between two random points!</Text>
	        <Button
            onPress={() => { this._callShowDirections() }}
            title="Open map"
            color="#841584"
          />
	      </View>
	    );
	  }
	}
    

**Issues**
----------
Feel free to submit issues and enhancement requests.

