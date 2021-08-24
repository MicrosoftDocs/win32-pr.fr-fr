---
description: 'Les objets de stockage sont répartis en trois types : contrôleurs, lecteurs et médias.'
ms.assetid: CF38F6E8-A43D-4A97-8055-6B17E323524C
title: Classes de stockage
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90c46efc17b3df5e1a509cec3565c6aaa7b65ff06d189951b100ac06d93a957e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829669"
---
# <a name="storage-classes"></a>Classes de stockage

Les objets de stockage sont répartis en trois types : contrôleurs, lecteurs et médias.

Il existe deux contrôleurs : un contrôleur IDE émulé et un contrôleur SCSI synthétique. Les deux contrôleurs prennent en charge l’attachement des lecteurs qui hébergent le support.

Les classes WMI de virtualisation associées au stockage sont les suivantes. La prise en charge des disquettes synthétiques est également prise en charge. L’attachement à un lecteur de disquette physique n’est pas pris en charge.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                      | Description                                                                                                                                                                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MSVM \_ AffectedStorageJobElement**](msvm-affectedstoragejobelement.md)<br/>       | Représente l’association entre un travail et les éléments managés qui peuvent être affectés par son exécution.<br/>                                                                                               |
| [**MSVM \_ BasedOn**](msvm-basedon.md)<br/>                                           | Association qui décrit comment les extensions de stockage peuvent être assemblées à partir d’extensions de niveau inférieur.<br/>                                                                                                           |
| [**MSVM \_ ControlledBy**](msvm-controlledby.md)<br/>                                 | Associe un appareil de stockage au contrôleur de stockage qui possède l’appareil.<br/>                                                                                                                          |
| [**MSVM \_ DiskDrive**](msvm-diskdrive.md)<br/>                                       | Représente un lecteur de disque dur à l’intérieur d’une machine virtuelle.<br/>                                                                                                                                              |
| [**MSVM \_ DisketteController**](msvm-diskettecontroller.md)<br/>                     | Représente le contrôleur de disquette sur l’ordinateur virtuel.<br/>                                                                                                                                               |
| [**MSVM \_ DisketteDrive**](msvm-diskettedrive.md)<br/>                               | Représente un lecteur de disquette à l’intérieur de la machine virtuelle.<br/>                                                                                                                                                  |
| [**MSVM \_ DVDDrive**](msvm-dvddrive.md)<br/>                                         | Représente un lecteur de DVD à l’intérieur d’une machine virtuelle.<br/>                                                                                                                                                    |
| [**MSVM \_ IDEController**](msvm-idecontroller.md)<br/>                               | Représente un contrôleur IDE.<br/>                                                                                                                                                                          |
| [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)<br/>             | Gère les fichiers de média virtuel (. vhd,. vhdx,. ISO ou. VFD) pour un ordinateur virtuel.<br/>                                                                                                                    |
| [**\_Disque logique MSVM**](msvm-logicaldisk.md)<br/>                                   | Représente un support de lecteur de stockage et est utilisé pour alimenter les lecteurs de stockage.<br/>                                                                                                                             |
| [**MSVM \_ MediaPresent**](msvm-mediapresent.md)<br/>                                 | Associe un lecteur de stockage au support inséré dans le lecteur.<br/>                                                                                                                                     |
| [**MSVM \_ MountedStorageImage**](msvm-mountedstorageimage.md)<br/>                   | Fournit des informations détaillées sur une image de stockage montée manuellement.<br/>                                                                                                                                  |
| [**MSVM \_ ProtocolControllerForUnit**](msvm-protocolcontrollerforunit.md)<br/>       | Cette Association indique qu’une sous-classe de l’unité logique (par exemple, un volume de stockage) est connectée par le biais d’un contrôleur de protocole spécifique.<br/>                                                       |
| [**MSVM \_ SCSIProtocolController**](msvm-scsiprotocolcontroller.md)<br/>             | Représente un contrôleur SCSI synthétique.<br/>                                                                                                                                                                |
| [**MSVM \_ StorageAlert**](msvm-storagealert.md)<br/>                                 | Représente un événement déclenché chaque fois que la propriété **OperationalStatus** de la classe [**MSVM \_ ResourcePool**](msvm-resourcepool.md) ou [**MSVM \_ LogicalDisk**](msvm-logicaldisk.md) change.<br/> |
| [**MSVM \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md)<br/> | Représente des paramètres spécifiquement liés à l’allocation de stockage virtuel.<br/>                                                                                                                         |
| [**MSVM \_ StorageJob**](msvm-storagejob.md)<br/>                                     | représente un travail d’opération de stockage créé par le Service de gestion d’images Microsoft Hyper-V.<br/>                                                                                                          |
| [**MSVM \_ VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md)<br/>     | Fournit des données de définition pour un disque dur virtuel.<br/>                                                                                                                                                         |
| [**MSVM \_ VirtualHardDiskState**](msvm-virtualharddiskstate.md)<br/>                 | Fournit des informations d’État pour une image de disque dur virtuel existante.<br/>                                                                                                                                    |



 

 

 




