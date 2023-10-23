import React from 'react';
import { View, Text, TouchableOpacity, StyleSheet, Alert } from 'react-native';

const App = () => {
  const data = [
    { id: '1', name: 'Alert' },
    { id: '2', name: 'Collapse' },
    { id: '3', name: 'Drawer' },
    { id: '4', name: 'FlatList' },
    { id: '5', name: 'Forms' },
    { id: '6', name: 'Highlight' },
    { id: '7', name: 'Icon' },
    { id: '8', name: 'Image' },
    { id: '9', name: 'List' },
    { id: '10', name: 'Map' },
    { id: '11', name: 'Modal' },
    { id: '12', name: 'Picker' },
    { id: '13', name: 'ScrollView' },
    { id: '15', name: 'StatusBar' },
    { id: '16', name: 'Switch' },
    { id: '17', name: 'Tab' },
    { id: '18', name: 'Text' },
    { id: '19', name: 'TextInput' },
    { id: '20', name: 'TouchableOpacity' },
    // Add more components here
  ];

  const handleComponentPress = (name) => {
    Alert.alert('Clicked Component', name);
  };
  return (
    <View style={styles.container}>
      {data.map((item) => (
        <TouchableOpacity
          key={item.id}
          onPress={() => handleComponentPress(item.name)}
          style={styles.componentContainer}
        >
          <Text style={styles.component}>{item.name}</Text>
        </TouchableOpacity>
      ))}
    </View>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    padding: 16,
    backgroundColor:'gray',
    justifyContent:'center',
    alignItems:'center'
  },
  componentContainer: {
    marginBottom: 16,
  },
  component: {
    fontSize: 13,
    fontWeight: 'bold',
  },
});

export default App;
