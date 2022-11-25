Both the YOLOv5 and YOLOv7 model files are separated by branches.

To train the YOLOv5 model: 
python train.py --img 512 --batch 12 --noval --epochs 30 --data data/custom.yaml --weights yolov5m.pt --cfg models/yolov5m_custom.yaml --hyp data/hyps/hyp.scratch-med.yaml --device 0 --name ./experiment_X

To train the YOLOv7 model: 
python train.py --device 0 --batch-size 12 --nosave --notest --data data/custom.yaml --img 256 256 --cfg cfg/training/yolov7_custom.yaml --weights 'yolov7_training.pt' --hyp data/hyp.scratch.custom.yaml --epochs 30 --name ./experiment_X

Inference Code: 
python detect.py --weights runs\train\experiment13\weights\best.pt --source custom_dataset\test_images --device 0
