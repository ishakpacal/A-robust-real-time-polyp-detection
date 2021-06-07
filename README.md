# A-robust-real-time-polyp-detection




Our method is based on Scaled-YOLOv4, please go to YOLOv4 repo and follow instructions for quick installation: https://github.com/WongKinYiu/ScaledYOLOv4 
Our trainin dataset can be downloaded here (MICCAI 2015 Sub-Challenge on Automatic Polyp Detection in Colonoscopy) , CVC-ClinicDB: https://polyp.grand-challenge.org/CVCClinicDB/, Test dataset, Etis-larib: https://polyp.grand-challenge.org/EtisLarib/ and other test dataset CVC-ColonDB: http://mv.cvc.uab.es/projects/colon-qa/cvccolondb 

Proposed Models:

![model](https://user-images.githubusercontent.com/58702074/117352476-b7c01880-aeb7-11eb-8fe2-4e51aeb5f7f1.PNG)

Data Augmentation and Hyper-paramps optimization

![data augment](https://user-images.githubusercontent.com/58702074/117353047-56e51000-aeb8-11eb-8640-398f52b59e11.PNG)
![hyper-param](https://user-images.githubusercontent.com/58702074/117353054-58aed380-aeb8-11eb-9aa5-cf53cfd76524.PNG)

Results

![result2](https://user-images.githubusercontent.com/58702074/117353102-62d0d200-aeb8-11eb-8be9-1b76c2e1f20b.PNG)
![results](https://user-images.githubusercontent.com/58702074/117353111-649a9580-aeb8-11eb-8d01-d114cefd86ad.PNG)


Our best model can be downloaded here" https://drive.google.com/file/d/1hJzAiFG8DuW5hC1ecZH4ClCvwe4QLnU9/view?usp=sharing "

# download {https://drive.google.com/file/d/1hJzAiFG8DuW5hC1ecZH4ClCvwe4QLnU9/view?usp=sharing } and put them in /yolo/weights/ folder.

#To test ETIS_LARIB Data set, use below command;(please also change pad = 0.5 to pad = 0.0 https://github.com/WongKinYiu/ScaledYOLOv4/blob/8579a59652930be203a266122b6db695ddeacc1b/test.py#L77 )

python test.py --weights weights/model1.pt --img-size 544 --conf-thres 0.291
