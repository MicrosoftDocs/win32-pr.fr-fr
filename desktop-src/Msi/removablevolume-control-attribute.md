---
description: Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes amovibles. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Attribut de contrôle RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9da559935a6f325c9f47fdbd902fe7b586870327b8107b14b6ae421f472a659
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912779"
---
# <a name="removablevolume-control-attribute"></a>Attribut de contrôle RemovableVolume

Si ce bit est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes amovibles. Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.

## <a name="valid-controls"></a>Contrôles valides

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                                  |
|---------|-------------|-------------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit RemovableVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez [contrôle des attributs](control-attributes.md) et des [contrôles](controls.md).

 

 



