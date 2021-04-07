---
description: Si le bit de contrôle FixedVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les disques durs internes fixes.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Attribut de contrôle FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863550"
---
# <a name="fixedvolume-control-attribute"></a>Attribut de contrôle FixedVolume

Si le bit de contrôle FixedVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les disques durs internes fixes.

Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.

## <a name="valid-controls"></a>Contrôles valides

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)



| Decimal | Valeur hexadécimale | Constante                              |
|---------|-------------|---------------------------------------|
| 131 072  | 0x00020000  | **msidbControlAttributesFixedVolume** |



 

## <a name="remarks"></a>Notes

Pour définir cet attribut sur un contrôle, incluez le bit FixedVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



