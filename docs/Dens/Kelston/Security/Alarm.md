# Kelston Burglar Alarm

The burglar alarm at the Kelston den has been configured to function as both intrusion and a fire alarm. The setup of this system is outlined below.
The manual for the Kelston alarm system is here: #TODO

The system is an Arrowhead Elite #TODO

## Zones

The following zone assignments are in use

| Zone | Assignment                         |
| ---- | ---------------------------------- |
| 1    | ??? #TODO                          |
| 2    | ??? #TODO                          |
| 3    | ???? #TODO                         |
| 4    | Not Used #TODO                     |
| 5    | Not Used                           |
| 6    | Not Used                           |
| 7    | Fire Alarm - Emergency Exit #TODO  |
| 8    | Fire Alarm - Front Door #TODO      |

Zones `7` and `8` are configured as 24 hour fire zones, remaining zones are configured as standard N/C circuits.

## Areas

To make the fire alarm operational, and to allow cancelling the fire alarm without the need to publicly display the alarm code, the panel has been set up with two areas. One for intrusion, and one for fire.

| Area | Zone |
| ---- | ---- |
| A    | 1    |
| A    | 2    |
| A    | 3    |
| A    | 4    |
| A    | 5    |
| A    | 6    |
| B    | 7    |
| B    | 8    |

Each area can be armed, disarmed, and reset independently. Area `A` is used for intrusion, and area `B` is used for fire alarm. The fire alarm code `1234E` is only assigned to area `B`, and cannot be used to arm or disarm area `A`. As [zones](#zones) `7` and `8` are configured as 24 hour fire zones, they will always be active regardless of the area armed state.

## Fire Alarm

### Design

Manual call points are connected in [zones](#zones) `7` & `8` these are wired as a N/C circuit to ground. Each zone is configured as a 24 hour fire zone.

### Usage

When a fire alarm circuit is opened the 24 hour fire zone will trigger, to reset the fire alarm the call point needs to be reset, and the code `1234E` entered into a keypad.

In order to reset the fire alarm, the area `B` must be cleared. This can be done by entering the code `1234E` into the keypad. **The alarm cannot be reset until all call points have been reset (switched off).**

## Alarm Codes

The configuration of the alarm is split into [areas](#areas) `A` and `B` to allow for the fire reset code to be visible without compromising the intrusion system. The fire alarm code `1234E` is assigned only to area `B`, and cannot be used for intrusion system in area `A`.

Alarm codes for hall users should be configured to control both areas `A` and `B` to allow hall users to reset the fire alarm with the code they have been provided. The master code for the alarm is available in [Logins](../../Index.md#logins).
