To train the YOLOv5 model: 
python train.py --img 512 --batch 12 --noval --epochs 30 --data data/custom.yaml --weights yolov5m.pt --cfg models/yolov5m_custom.yaml --hyp data/hyps/hyp.scratch-med.yaml --device 0 --name ./experiment_X

Inference Code: 
python detect.py --weights runs\train\experiment13\weights\best.pt --source custom_dataset\test_images --device 0
