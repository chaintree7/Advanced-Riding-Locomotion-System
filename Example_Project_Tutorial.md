

&nbsp;
####  1. **Add required assets**
&nbsp;
1. Create a UE5 Third Person Project
2. Add Horse Animset to project
3. Modify some animations
4. Export animation for Rider
5. Import Rider animations into UE4 Skeletons
6. Retarget rider animations from UE4 skeleton to UE5 skeleton
7. Add ALS v4 to project
8. Import Rider animations into ALS skeleton

&nbsp;
#### **Video Tutorial**

https://www.youtube.com/watch?v=cFGqU5NS5KE

#### **When done, please check if the following files exist**

##### **Horse**

+  *Content/HorseAnimsetPro/Animations/Horse/InPlace/Jump/Horse_IP_Jump_Canter_Start*
+  *Content/HorseAnimsetPro/Animations/Horse/InPlace/Jump/Horse_IP_Jump_Forward_Start*
+  *Content/HorseAnimsetPro/Animations/Horse/InPlace/Jump/Horse_IP_Jump_Gallop_Start*
+  *Content/HorseAnimsetPro/Animations/Horse/InPlace/Jump/Horse_IP_Jump_Sprint_Start*

##### **ALS Rider**
+ *Content/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Rider/Jump/Rider_Jump_Canter_Start_v2*
+ *Content/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Rider/Jump/Rider_Jump_Forward_Start_v2*
+ *Content/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Rider/Jump/Rider_Jump_Fall_High*
+ *Content/AdvancedLocomotionV4/CharacterAssets/MannequinSkeleton/AnimationExamples/Rider/Jump/Rider_Jump_Fall_Low*

##### **UE5 Rider**

+  *Content/Characters/Mannequins/Animations/Rider/Jump/Rider_Jump_Canter_Start_v2*
+  *Content/Characters/Mannequins/Animations/Rider/Jump/Rider_Jump_Forward_Start_v2*
+  *Content/Characters/Mannequins/Animations/Rider/Jump/Rider_Jump_Fall_High*
+  *Content/Characters/Mannequins/Animations/Rider/Jump/Rider_Jump_Fall_Low*

&nbsp;
&nbsp;

#### 2 **Add `Advanced Riding Locomotion System` to project**
Marketplace [Advanced Riding Locomotion System](https://www.unrealengine.com/marketplace/en-US/product/advanced-riding-locomotion-system) 
![image](https://user-images.githubusercontent.com/87846878/169574760-bc42d57f-0572-4b7a-b902-5643a0af1330.png)


#### 3. **Add example source code to project**

GoogleDrive [Download example code](https://drive.google.com/file/d/10r-01SC796MJPYDSsUqBP-SvW0DyvZ5k/view?usp=sharing
) 

1. Copy the example code `CT_Example/` to the `/Content/` directory
2. Open `ALS_Base_CharacterBP` and set the parent class to `BP_Rider`
3. Open `BP_ThirdPersonCharacter` and set the parent class to `BP_Rider`
4. Open `CT_Example/Map/DemoMap` and set GameMode to `CT_GameMode`
5. Open `Horse_Skeleton` add Socket `ALS_MountPoint` and modify position of `MountPoint`
6. Open `CT_Example/Characters/ALS/ALS_Copy_Code` and copy code to `ALS_AnimBP` and `OverlayStateSwitcher`
7. Open `CT_Example/Characters/Rider/UE5_Copy_Code` and copy code to `ABP_Manny`
8. Open `ALS_Mannequin_Skeleton` add `Rein_LSocket` and `Rein_rSocket`
9. Open `SK_Mannequin` add `Rein_lSocket` and `Rein_rSocket`

&nbsp;
#### **Video Tutorial**

https://www.youtube.com/watch?v=DpsPtXgV3iw
