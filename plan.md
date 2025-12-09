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
#Given a new tyre with a pressure and tread depth
#It returns the properties correctly and an empty readings list
def test_new_tyre_returns_properties_correctly():
    tyre = Tyre()
    assert tyre.readings == []

#Given a tyre with updated tread depth and pressure
#It will add a new reading with add_reading()
def test_add_reading_takes_in_pressure_and_depth_updates_readings
    tyre = Tyre()
    tyre.add_reading({depth: 23, pressure: 2})    
    assert tyre.readings == [{depth: 23, pressure: 2, time_added: 10/12/25}]
    tyre.add_reading({depth: 62, pressure: 12})
    assert tyre.readings == [{depth: 23, pressure: 2, time_added: 10/12/25},{depth: 62, pressure: 12, time_added: 10/12/25}]

#Given a car with a name and tyres, it will return the correct properties 
def test_car_initialised_with_name_and_tyres():
    tyre1 = Tyre()
    tyre2 = Tyre()
    tyre3 = Tyre()
    tyre4 = Tyre()
    car = Car({"front right":tyre1,
                "front left":tyre2,
                "back right":tyre3,
                "back left":tyre4
                })
    assert car.tyres == {"front right":tyre1,
                "front left":tyre2,
                "back right":tyre3,
                "back left":tyre4
                }

#Given a car with tyres, it will return the newest reading with newest_reading()
def test_newest_reading_returns_most_recent_tyre_readings_for_singular_tyre():
    tyre1 = Tyre()
    tyre.add_reading({depth: 23, pressure: 2}) 
    tyre2 = Tyre()
    tyre3 = Tyre()
    tyre4 = Tyre()
    car = Car({"front right":tyre1,
                "front left":tyre2,
                "back right":tyre3,
                "back left":tyre4
                })

    assert car.newest_reading("front right") == {depth: 23, pressure: 2, time_added: 10/12/25}

#Given a car with tyres, return all the history of a singular tyre's readings     
def test_return_history_for_tyre():
    tyre1 = Tyre()
    tyre.add_reading({depth: 23, pressure: 2})
    tyre.add_reading({depth: 73, pressure: 12}) 
    tyre2 = Tyre()
    tyre3 = Tyre()
    tyre4 = Tyre()
    car = Car({"front right":tyre1,
                "front left":tyre2,
                "back right":tyre3,
                "back left":tyre4
                })
    assert car.tyre_history("front right") == [{depth: 23, pressure: 2, time_added: 10/12/25},{depth: 73, pressure: 12, time_added: 10/12/25}]
```
