#### Video Tutorial

**[Tutorials playlist](https://www.youtube.com/playlist?list=PL3wXnfaYKI8TwfoK_wtQ3oYVUqqynwOK7)**

https://www.youtube.com/watch?v=JkTmVhS9owo&list=PL3wXnfaYKI8TwfoK_wtQ3oYVUqqynwOK7&index=2


## **Function `Input Move Forward/Backward`**
![image](https://user-images.githubusercontent.com/87846878/169575402-b01fbd22-8158-46a5-8de2-0f91763eb405.png)

**This function controls speed by timeline**

#### **Forward Timeline**
![image](https://user-images.githubusercontent.com/87846878/169575431-f0502bcf-3fe2-478b-8fdf-0b35a459d09a.png)
*/CT_Components/RidingSystem/Components/Timeline/CT_Timeline_Forward*
&nbsp;
 **Max speed `1000` and time is `5 seconds`**
&nbsp;
| Config   | Default   | Description |
| ----------- | ----------- | ----------- |
| Speed Scale Forward |  1.2 |  Default max speed `1000` When the value is `1.2` the max speed is `1200`
| Timeline Forward Play Rate |  2 |  Acceleration time default is `5 seconds`  When the value is `2`, the acceleration time is `2.5 seconds` 
| Timeline Forward Reverse Play Rate |  2 |   Deceleration time default is `5 seconds`  When the value is `2`, the deceleration time is `2.5 seconds` 
| Keep Moving |  150 |  When the speed is greater than 150, it will keep the current speed even if it stops accelerating
&nbsp;
#### **Backward timeline**
![image](https://user-images.githubusercontent.com/87846878/169575483-848ffe56-05c8-4f36-a390-c628bc87527d.png)
*Path: /CT_Components/RidingSystem/Components/Timeline/CT_Timeline_Backward*

**Max speed is `-100` and time is `1 seconds`** 
&nbsp;
| Config   | Default   | Description |
| ----------- | ----------- | ----------- |
| Speed Scale Backward  |  1.5 |  Default max speed `100` When the value is `1.5` the max speed is `150`
| Timeline Backward Play Rate |  4 |  Acceleration time default is `1 seconds`  When the value is `4`, the acceleration time is `0.25 seconds` 
| Timeline Backward Reverse Play Rate |  4 |   Deceleration time default is `1 seconds`  When the value is `4`, the deceleration time is `0.25 seconds` 
&nbsp;
## **Function `Input Move Right/Left`**
![image](https://user-images.githubusercontent.com/87846878/169575568-e3c6c07c-9446-4e7e-be2c-7ac5fbf6ead4.png)

This function controls rotate by timeline


#### **Rotation Timeline**
![image](https://user-images.githubusercontent.com/87846878/169575682-e5238e61-5b43-4732-bb32-8341550f9d62.png)
*Path: /CT_Components/Riding/Components/Timeline/CT_Timeline_Rotation*

**Angle is `45` and time is `1 seconds`** 

| Config   | Default   | Description |
| ----------- | ----------- | ----------- |
| Timeline Rotation Play Rate |  2 |  Default `1 seconds` When the value is `2` the max speed is `0.5 seconds`
| Timeline Rotation Reverse Play Rate |  4 |  Default `1 seconds` When the value is `4` the max speed is `0.25 seconds`
| Rotation Reverse Alpha |  1 | Rotate during `Timeline Rotation Reverse` no rotation when value is `0`
| Turning Deceleration |  0.9 |  Decelerate when turning, When the value is  `1`  to not decelerate
| Turning Deceleration Speed Lower Limit |  500 |  `Turning Deceleration` does not trigger when speed is less than `500`

| Rotation Rate |  40 |  Rotation rate
| Rotation Rate InPlace |  40 |  Rotation rate when in place `(Mainly to match the turn animation)`
| Turning in Place Speed |  40 |  Add speed when turning in place `(Mainly to match the turn animation)`

## **`Using custom timeline`**

![image](https://user-images.githubusercontent.com/87846878/169575867-9e80af99-76ad-4be1-96cf-2c7a4cd8108c.png)

## **Function `ClearTimelineForward/Backward`**
**Clear Forward & Backward timeline. This function will stop character immediately**


## **Function `ClearTimelineRotation`**
**Clear Rotation timeline**

## **Function `ClearTimeline`**
**Call `ClearTimelineForward/Backward` and  `ClearTimeline`**


## **Function `Reset Control Rotation`**
**For example, Horse Animset has an animation `Horse_RM_Turn_Neigh_Left` It's rotated 180°  should be used like this**

![image](https://user-images.githubusercontent.com/87846878/169576093-0225c3f1-1e36-48b2-9ee4-ee9b2b1040d3.png)

## **Function `Stop Moving`**
**Deceleration and stop the character**




## **Function `Simple Move To Actor`**
**For example, call horse. When the `Acceptance Radius` value is `-1`  it will always follow**

![image](https://user-images.githubusercontent.com/87846878/169576249-0ba24ea2-230a-4ba7-884c-ed101a6ffd84.png)

## **Function `Simple Move To Location`**

![image](https://user-images.githubusercontent.com/87846878/169576341-1ac75390-8667-4e81-85d5-7b1d626da598.png)

## **Function `Stop Simple Move to`**
**Cancel `Simple Move to XXX` and stop**

## **Function `Is Simple Moving`**
**Is currently in `Simple Move to XXX`**

&nbsp;
# Event Despatch

## **Event `OnSimpleMoveTo`**
**When `Simple Move to XXX` is called`**

## **Event `OnSimpleMoveToComplete`**
**When `Simple Move to XXX` is complete**

&nbsp;
# Add Animation
&nbsp;

![image](https://user-images.githubusercontent.com/87846878/169576393-c3602575-54df-495d-87fb-80426f0de3a6.png)

**CT Anim Graph Animal Movement **

| Params | Type | Description |
| ----------- | ----------- | ----------- |
| CT_Cmpt_AnimalMovement |  Component| Can be ignored if owner adds `CT_Cmpt_AnimalMovement`
| Movement BS |  Blendspace |   X = Rotation Y = Speed
| Idle Anim |  Animation |  Idle Animation


**Movement Blendspace example**
![image](https://user-images.githubusercontent.com/87846878/169576435-22dbefba-819f-459b-93f6-8c8e6b71fac0.png)

**CT Anim Graph Animal Jump**

| Params | Type | Description |
| ----------- | ----------- | ----------- |
| CT_Cmpt_AnimalMovement |  Component|  Can be ignored if owner adds `CT_Cmpt_AnimalMovement`
| Jumps |  Map | Play different animations based on speed

`Jumps` Example

| Params | Type | Description  |
| ----------- | ----------- |----------- |
| Key |  Float |  Speed
| Value -> Jump Start |  Animation |  Jump start animation
| Value -> Jump Land |  Animation |  Jump landing animation
| Value -> Jump Fall|   Blendspace 1D |  Jump fall animation

![image](https://user-images.githubusercontent.com/87846878/169576473-6c3e7432-939d-4edb-86dd-1963e95fd1bd.png)
