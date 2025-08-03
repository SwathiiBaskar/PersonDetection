# PersonDetection
This is a custom-trained object detection model using YOLOv5 to identify human presence through Thermal Imaging.  It enables accurate person detection in low-light or no-light environments by leveraging Infrared thermal data instead of regular RGB input.  This system is ideal for Surveillance, Search and rescue operations and Security use cases

## Dataset

The dataset contains annotated thermal images labeled for **person detection**, structured in YOLO format.

- **Location**: [`/content/PersonDection.v5i.yolov5pytorch.zip`](#)
- **Format**: YOLOv5
- **Classes**: `['person']`
- **Source**: Infrared thermal imaging

---

## Training Configuration

- **Model**: YOLOv5s
- **Image Size**: 256×256
- **Epochs**: 25
- **Batch Size**: 16
- **Framework**: PyTorch
- **Training Platform**: Google Colab

**Command:**
```bash
python train.py --img 256 --batch 16 --epochs 25 --data data.yaml --weights yolov5s.pt --cache
