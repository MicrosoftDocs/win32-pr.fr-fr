---
description: Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disque RAM. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Attribut de contrôle RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312274"
---
# <a name="ramdiskvolume-control-attribute"></a>Attribut de contrôle RAMDiskVolume

Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disque RAM. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.

## <a name="valid-controls"></a>Contrôles valides

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit RAMDiskVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



