# EMLOv4 - Assignment S06 - Lightning + Hydra + DVC

![Train and Report](https://github.com/mHemaAP/s06-emlov4-hydra/actions/workflows/cml.yml/badge.svg)

![Python CI/CD](https://github.com/mHemaAP/s06-emlov4-hydra/actions/workflows/ci.yml/badge.svg)

## Tasks Accomplished

- pyproject.toml
- Dockerfile
- pytest
- codecov
- Docker Image to GHCR
- added dvc for dogs breed
- sample inference
- added vit model
- comet logs

## Predictions
The prediction results / images are being sent to `test_metrics.md` in the `cml.yml` and not sent to README.md, hence these are not shown here.

## Comet Logs

### Train Logs

```
COMET INFO: ---------------------------------------------------------------------------------------
COMET INFO: Comet.ml Experiment Summary
COMET INFO: ---------------------------------------------------------------------------------------
COMET INFO:   Data:
COMET INFO:     display_summary_level : 1
COMET INFO:     name                  : raspy_capitol_2122
COMET INFO:     url                   : https://www.comet.com/mhemaap/general/c2d5e37543aa474e92d27d1176220db2
COMET INFO:   Metrics [count] (min, max):
COMET INFO:     epoch [116]           : (0, 19)
COMET INFO:     hp_metric             : -1
COMET INFO:     lr-Adam [152]         : (0.0003999999999999993, 0.0010542433293314456)
COMET INFO:     train/acc_epoch [40]  : (0.16638655960559845, 1.0)
COMET INFO:     train/acc_step [152]  : (0.09375, 1.0)
COMET INFO:     train/loss_epoch [40] : (0.005857521668076515, 2.2438015937805176)
COMET INFO:     train/loss_step [152] : (0.0031126474495977163, 2.325953245162964)
COMET INFO:     val/acc_epoch [40]    : (0.20863309502601624, 0.971222996711731)
COMET INFO:     val/acc_step [200]    : (0.0, 1.0)
COMET INFO:     val/loss_epoch [40]   : (0.10269735753536224, 2.214803457260132)
COMET INFO:     val/loss_step [200]   : (0.0014227889478206635, 2.3351786136627197)
COMET INFO:   Parameters:
COMET INFO:     lr                 : 0.001
COMET INFO:     min_lr             : 1e-06
COMET INFO:     model_name         : resnet18
COMET INFO:     num_classes        : 10
COMET INFO:     pretrained         : False
COMET INFO:     scheduler_factor   : 0.1
COMET INFO:     scheduler_patience : 10
COMET INFO:     trainable          : False
COMET INFO:     weight_decay       : 1e-05
COMET INFO:   Uploads:
COMET INFO:     environment details : 1
COMET INFO:     filename            : 1
COMET INFO:     git metadata        : 1
COMET INFO:     installed packages  : 1
COMET INFO:     model graph         : 1
COMET INFO:     os packages         : 1
COMET INFO:     source_code         : 2 (20.51 KB)
COMET INFO: 
```

### Evaluate Logs

```
COMET INFO: ---------------------------------------------------------------------------------------
COMET INFO: Comet.ml ExistingExperiment Summary
COMET INFO: ---------------------------------------------------------------------------------------
COMET INFO:   Data:
COMET INFO:     display_summary_level : 1
COMET INFO:     name                  : raspy_capitol_2122
COMET INFO:     url                   : https://www.comet.com/mhemaap/general/c2d5e37543aa474e92d27d1176220db2
COMET INFO:   Metrics [count] (min, max):
COMET INFO:     epoch               : 20
COMET INFO:     hp_metric           : -1
COMET INFO:     test/acc_epoch      : 0.9939758777618408
COMET INFO:     test/acc_step [12]  : (0.96875, 1.0)
COMET INFO:     test/loss_epoch     : 0.046923309564590454
COMET INFO:     test/loss_step [12] : (0.015886088833212852, 0.15863052010536194)
COMET INFO:   Parameters:
COMET INFO:     lr                 : 0.001
COMET INFO:     min_lr             : 1e-06
COMET INFO:     model_name         : resnet18
COMET INFO:     num_classes        : 10
COMET INFO:     pretrained         : False
COMET INFO:     scheduler_factor   : 0.1
COMET INFO:     scheduler_patience : 10
COMET INFO:     trainable          : False
COMET INFO:     weight_decay       : 1e-05
COMET INFO:   Uploads:
COMET INFO:     model graph : 1
COMET INFO: 
```

### Infer Logs

```
COMET INFO: ---------------------------------------------------------------------------------------
COMET INFO: Comet.ml Experiment Summary
COMET INFO: ---------------------------------------------------------------------------------------
COMET INFO:   Data:
COMET INFO:     display_summary_level : 1
COMET INFO:     name                  : pink_cow_5496
COMET INFO:     url                   : https://www.comet.com/mhemaap/general/ccdb211608ff46d58085332cbe4dcaee
COMET INFO:   Metrics [count] (min, max):
COMET INFO:     epoch               : 0
COMET INFO:     hp_metric           : -1
COMET INFO:     test/acc_epoch      : 0.9939758777618408
COMET INFO:     test/acc_step [12]  : (0.96875, 1.0)
COMET INFO:     test/loss_epoch     : 0.046923309564590454
COMET INFO:     test/loss_step [12] : (0.015886088833212852, 0.15863052010536194)
COMET INFO:   Parameters:
COMET INFO:     lr                 : 0.001
COMET INFO:     min_lr             : 1e-06
COMET INFO:     model_name         : resnet18
COMET INFO:     num_classes        : 10
COMET INFO:     pretrained         : True
COMET INFO:     scheduler_factor   : 0.1
COMET INFO:     scheduler_patience : 10
COMET INFO:     trainable          : False
COMET INFO:     weight_decay       : 1e-05
COMET INFO:   Uploads:
COMET INFO:     environment details      : 1
COMET INFO:     filename                 : 1
COMET INFO:     git metadata             : 1
COMET INFO:     git-patch (uncompressed) : 1 (805 bytes)
COMET INFO:     installed packages       : 1
COMET INFO:     model graph              : 1
COMET INFO:     os packages              : 1
COMET INFO:     source_code              : 2 (19.46 KB)
COMET INFO: 
```
