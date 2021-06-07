# A-robust-real-time-polyp-detection

# A robust real-time deep learning based automatic polyp detection system
# https://www.sciencedirect.com/science/article/pii/S0010482521003139



Our method is based on Scaled-YOLOv4, please go to YOLOv4 repo and follow instructions for quick installation: https://github.com/WongKinYiu/ScaledYOLOv4 
Our trainin dataset can be downloaded here (MICCAI 2015 Sub-Challenge on Automatic Polyp Detection in Colonoscopy) , CVC-ClinicDB: https://polyp.grand-challenge.org/CVCClinicDB/, Test dataset, Etis-larib: https://polyp.grand-challenge.org/EtisLarib/ and other test dataset CVC-ColonDB: http://mv.cvc.uab.es/projects/colon-qa/cvccolondb 

# Proposed Models:

![model](https://user-images.githubusercontent.com/58702074/120996810-57124d00-c78f-11eb-8641-eea4128463a2.PNG)


# Data Augmentation and Hyper-paramps optimization

![data-aaug](https://user-images.githubusercontent.com/58702074/120996849-609bb500-c78f-11eb-819f-9f9eb25a4429.PNG)




# Our best model can be downloaded here" https://drive.google.com/file/d/1hJzAiFG8DuW5hC1ecZH4ClCvwe4QLnU9/view?usp=sharing "

download {https://drive.google.com/file/d/1hJzAiFG8DuW5hC1ecZH4ClCvwe4QLnU9/view?usp=sharing } and put them in /yolo/weights/ folder.

# To test ETIS_LARIB Data set, use below command;(please also change pad = 0.5 to pad = 0.0 https://github.com/WongKinYiu/ScaledYOLOv4/blob/8579a59652930be203a266122b6db695ddeacc1b/test.py#L77 )

python test.py --weights weights/model1.pt --img-size 544 --conf-thres 0.291 --iou-thres 0.5

![reslts1](https://user-images.githubusercontent.com/58702074/120996885-6abdb380-c78f-11eb-8f98-0b2c465267bc.PNG)




# To test CVC-ColonDB Data set, use below command (do not change pad, so pad is default, pad = 0.5)
python test.py --weights weights/model1.pt --img-size 384 --conf-thres 0.25 --iou-thres 0.5

![result2](https://user-images.githubusercontent.com/58702074/120996995-81fca100-c78f-11eb-822c-db7e2263a41b.PNG)

# Citation
Pacal, Ishak & Karaboga, Dervis. (2021). A Robust Real-Time Deep Learning Based Automatic Polyp Detection System. Computers in Biology and Medicine. 134. 104519. 10.1016/j.compbiomed.2021.104519. 

