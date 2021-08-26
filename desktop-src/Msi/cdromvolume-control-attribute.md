---
description: Si le bit de contrôle CDROMVolume est défini, le contrôle affiche tous les volumes de l’installation actuelle, ainsi que tous les volumes CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Attribut de contrôle CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abd961ddfd710defea9b464ea861f731fcf84a0989062f0607fda8ced5b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078039"
---
# <a name="cdromvolume-control-attribute"></a>Attribut de contrôle CDROMVolume

Si le bit de contrôle CDROMVolume est défini, le contrôle affiche tous les volumes de l’installation actuelle, ainsi que tous les volumes CD-ROM.

Si ce bit n’est pas défini, le contrôle affiche tous les volumes de l’installation actuelle.

## <a name="valid-controls"></a>Contrôles valides

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                              |
|---------|-------------|---------------------------------------|
| 524 288  | 0x00080000  | **msidbControlAttributesCDROMVolume** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit CDROMVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



