---
layout: page
nav_order: 4
parent: DIY trackers guide
---

# IMU Comparison
The community has been hard at work testing various IMUs for DIY SlimeVR trackers.
A survey was held within the DIY community for a clearer picture of the current state of available IMUs.
This page is based on user feedback and weighed against the survey, with scores showing the average answer given to the chip.
Following completing your own trackers, you can complete an extended version of that original survey yourself, or view previous responses on the [SlimeVR Experience Survey page](../slimevr-experience-survey.html).

## Index
- [MPU6050](#mpu6050)
- [MPU6500](#mpu6500)
- [BNO055](#bno055)
- [BMI160](#bmi160)
- [MPU+QMC5883L](#mpuqmc5883l)
- [MPU9250](#mpu9250)
- [ICM20948](#icm20948)
- [BNO085](#bno085)
- [Addendum](#addendum)

## Criteria
We rank these chips in the following categories: Reset Time, Cost, Availability and Build quality.
These factors are meant to give a quick indication as to what to expect from various IMUs, your mileage may vary.
For clarification purposes: If 3 out of 10 chips are dead on arrival or die during early use, we refer to that as poor build quality.

---
## MPU6050
The MPU6050 is the current go-to alternative for DIY SlimeVR.
Whilst being less reliable than BNO chips they offer a great value for money proposition and will get you started with SlimeVR for cheap.

|Reset time |Cost  |Availability|Build quality|
|:---------:|:----:|:----------:|:-----------:|
|1 - 10 min |~$1.04|Sufficient  |Poor         |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o" ></i>

|Pros             |Cons             |
|-----------------|-----------------|
|Cheap            |Higher drift rate|
|High availability|Older technology |
|Smooth           |High failure rate|

`Comment: Order more than you need because of the higher failure rate, it is not uncommon to find 2 to 3 bad chips in a batch.`

---
## MPU6500
The MPU6500 is the middle ground of the MPU chips available.
Even though it is a 6DOF sensor (same as the 6050), the drift time of the chips is a slight improvement over the MPU6050.

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|5 - 10 min |~$1  |Sufficient  |Mediocre     |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-o" ></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                    |
|-----------------|----------------------------------------|
|Affordable       |High drift rate                         |
|Available        |More expensive than the 6050 counterpart|
|Smooth           |Failure rate inconsistent               |

`Comment: Tracking slightly better than the MPU6050.`

---
## BNO055
Earlier version of the BNO085 without stabilisation firmware.

*This chip does not have sufficient test results for a conclusive summary.*

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|1 -10 min  |~$55 |Mediocre    |Good         |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i><i class="fa fa-star-o">

|Pros                           |Cons                                          |
|-------------------------------|----------------------------------------------|
|Build Quality                  |Expensive                                     |
|Available                      |Can supposedly lose tracking with rapid motion|
|Smooth                         |Insufficient testing                          |

`Comment: Insufficient testing for a accurate description, but cannot compete with BNO085.`

---
## BMI160
The BMI 160 is a relatively new chip with decent performance.
This chip's ratings could potentially improve with more testing.


|Reset time |Cost  |Availability|Build quality|
|:---------:|:----:|:----------:|:-----------:|
|5 - 10min  |~$1.42|Sufficient  |Good         |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-o"></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                             |
|-----------------|-------------------------------------------------|
|Cheap            |Currently still in testing                       |
|Reliable         |Requires manual calibration the first time       |

`Comment: Still in very early stages of testing, but appears to be better or equal to the MPU6050 and with better build quality.`

---
## MPU+QMC5883L
This is a highly experimental setup that approximately matches an MPU9250.
Unlike other IMUs which consist of a single PCB, this instead relies on connecting a magnetometer to an MPU6050 or MPU6500.
That being said, a breakout board which includes both an MPU6050 and an HMC5883L does exist: the GY-87.
Both the QMC5883L and HMC5883L may be used, however, the QMC5883L may potentially perform better.


|Reset time |Cost  |Availability|Build quality|
|:---------:|:----:|:----------:|:-----------:|
|10 - 40min |~$2.50|Sufficient  |Mixed        |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                             |
|-----------------|-------------------------------------------------|
|Cheap            |Very experimental                                |
|Smooth           |Requires manual calibration the first time       |
|Reliable         |Sensitive to bad magnetic enviroments            |

`Comment: Requires experimental firmware.`

---
## MPU9250
The MPU9250 (currently ran in several modes) is a newer installment of the MPU lineup.

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|10 - 40 min|~$7  |Insufficient|Mediocre     |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-o" ></i><i class="fa fa-star-o" ></i>

|Pros             |Cons                                             |
|-----------------|-------------------------------------------------|
|Affordable       |Very prone to counterfeit/DOA units              |
|Smooth           |Sensitive to bad magnetic enviroments            |
|Reliable         |Requires manual calibration the first time       |

`Comment: Finding legitimate MPU9250s has become exceedingly difficult due to counterfeits and DOA IMUs. Buy at your own risk.`

---
## ICM20948
The ICM 20948 is a comparatively modern chip.
While initial testing seems positive, this chip has not had enough field time for conclusive results.

There are quite a few variants of the ICM-20948, most of which operate at 3.3v.
Pimoroni ICM-20948 (Please note this board requires you to cut the bridge on the back to change the address)
Adafruit ICM-20948 (Please note this board requires you to solder the bridge on the back to change the address)
SparkFun ICM-20948 (Please note this board requires you to solder the bridge on the back to change the address)
GY-912 (Please note this board requires you to bridge SD0 to GND to change the address)

CJMCU-20948 is known to run on 1.8v and needs additional hardware to work.
A 1.8v Linear Voltage regulator and Logic Level Converter is needed and as such this board is not recommended.



|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|15 - 60 min|~$15 |Insufficient|Good         |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o"></i>

|Pros             |Cons                                 |
|-----------------|-------------------------------------|
|Accurate         |Currently still in testing           |
|Reliable         |Sensitive to bad magnetic enviroments|
|Smooth           |Availability is not guaranteed       |

`Comment: Prone to some drift when moving really fast (in 6DoF mode).`

---
## BNO085
This is the IMU used in production slimes.
They are reliable and stable chips, but at the time of writing they are impossible to find.

*Please note these boards are both hard to get and may cost up to $80.*

|Reset time |Cost |Availability|Build quality|
|:---------:|:---:|:----------:|:-----------:|
|30 - 60 min|~$60 |Insufficient|Excellent    |

Score: <i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star"></i><i class="fa fa-star-half-o">

|Pros          |Cons                                   |
|--------------|---------------------------------------|
|Accurate      |High price during shortages            |
|Reliable      |Extra wiring required compared to MPUs |
|Smooth        |Expensive                              |

`Comment: Due to the chip shortage these are near impossible to find, please do not buy these at the listed prices.`

---
# Addendum

## How can I check if I have an acceptable magnetic environment?

You can check by downloading any magnetometer app that show what your magnetic field strength is in uT and by walking around your playspace. You may want to check at varying heights, such as at chest level, waist level, and ankle level. An option available on both iOS and Android is the app, Physics Toolbox Magnetometer. If you do use Physics Toolbox Magnetometer, you only need to pay attention to the total, not the X, Y, or Z components. Most phones have a magnetometer, but if yours does not, then there is no way to be exactly sure of your magnetic environment, but you can make some educated assumptions.

## My app show around X uT is that okay?

There's no one value that's acceptable. What matters is that the range of values is low. There is currently limited data to give an exact range, but a good baseline seems to be a range of less than or equal to 5 uT. For example, 20-25 uT would be okay as would 40-45 uT, but a range of 20-40 uT would likely be too unstable to use.

## What determines a "poor magnetic environment"?

Often things made of steel or other ferromagnetic materials contribute most to a poor magnetic environment. Some common examples of things that might affect your magnetic environment include, but are not limited to: spring mattresses, radiators, PC cases, desktop speakers, or furniture that's made of steel. In most cases, the effect that these things will have extend about 6-12 inches (15-30 cm) and within that range may cause the IMU to rotate incorrectly. The size and amount of mass directly impacts the size of the effected area; a paper clip might only affect your IMU if it's directly next to it, whereas a steel bedframe might affect an area 6-12 inches (15-30 cm) away as previous mentioned. In most cases, depending on the size of your playspace, these issues of certain objects causing interference can be mitigated by avoiding or reposition them. Regardless, other factors such as the wiring or rebar in your building could also affect your magnetic environment. These last few examples are harder to predict and illustrate why it's important to test with an app before assuming you might have a stable magnetic environment.

## Can I still use my IMU with a magnetometer if I don't have a stable magnetic environment?

This cannot be recommended. When run without the magnetometer, IMUs with magnetometers such as the MPU9250 and ICM20948, perform much worse. That said, if for whatever reason you do want to use your IMU without the magnetometer, the MPU6500 or MPU6050 firmware can be used on the MPU9250 instead, and the ICM20948 can run in 6DOF mode.

## IMU Calibration

Some IMUs, such as the MPU9250, BMI160, and MPU+QMC5883L, require manual calibration. This only needs to be performed once upon first setting up your SlimeVR tracker, however, you may need to perform the calibration multiple times before reaching satisfactory results. More information on how you would calibrate your IMUs can be [found here.](https://docs.slimevr.dev/server-setup/installing-and-connecting.html#imu-calibration)

---
### Credits
*Created by Smeltie#1999, edited by #calliePepper#0666 and NWB#5135*

A big thanks to everyone who took the time to fill out the survey.

Icons used in this document are provided by fork awesome.
*https://forkaweso.me*

<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/fork-awesome@1.2.0/css/fork-awesome.min.css" integrity="sha256-XoaMnoYC5TH6/+ihMEnospgm0J1PM/nioxbOUdnM8HY=" crossorigin="anonymous">
