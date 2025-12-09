As a car owner
So that I can keep a record of details about my tyres
I want to keep track of the tyres individually, by their position on my car

As a car owner
So that I have the two important pieces of data for a tyre
I want to be able to record both tyre pressure and tyre tread depth

As a car owner
So that I have a history of tyre readings
I want to be able to keep a record of historical readings, when those were, as well as current readings

As a car owner
So that I can see the details of my car at a glance
I want to list the tyres' positions, latest readings and when those were


Classes:
- Tyre
- Car 

Tyre
Properties:
- Position

Methods: 
- update readings

Car 
Properties:
- Tyre Positions
- Readings [{depth: 23, pressure, 2},...]

Methods:
- List Readings
- Update Readings
- List latest readings 

```python
Given a new tyre with a position, pressure and tread depth
It returns the properties correctly and an empty readings list
def test_new_tyre_returns_properties_correctly():
    tyre = Tyre("front left")
    assert tyre.position == "front left"
    assert tyre.readings == []

Given a tyre with updated tread depth and pressure
It will add a new reading with add_reading()
def test_add_reading_takes_in_pressure_and_depth_updates_readings
    tyre = Tyre("front left")
    tyre.add_reading({depth: 23, pressure, 2})    
    assert tyre.readings == [{depth: 23, pressure, 2}]
    tyre.add_reading({depth: 62, pressure, 12})
    assert tyre.readings == [{depth: 23, pressure, 2},{depth: 62, pressure, 12}]


```
