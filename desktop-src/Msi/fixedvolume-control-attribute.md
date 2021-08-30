---
description: Si le bit de contrôle FixedVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les disques durs internes fixes.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Attribut de contrôle FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d872c4bf891aaa3d93a755058b0047598cb80b0e07629cca7f8f8fc981af8ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828849"
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



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit FixedVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



