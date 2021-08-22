---
description: Si le bit de contrôle FloppyVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disquette.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Attribut de contrôle FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4639960fee79336048082c91088e19c1b360f857216f2cf0ad9ed07c64b52b8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947010"
---
# <a name="floppyvolume-control-attribute"></a>Attribut de contrôle FloppyVolume

Si le bit de contrôle FloppyVolume est défini, le contrôle affiche tous les volumes impliqués dans l’installation actuelle, ainsi que tous les volumes de disquette.

Si ce bit n’est pas défini, le contrôle répertorie les volumes dans l’installation actuelle.

## <a name="valid-controls"></a>Contrôles valides

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Valeur



| Decimal | Valeur hexadécimale | Constante                               |
|---------|-------------|----------------------------------------|
| 2 097 152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Remarques

Pour définir cet attribut sur un contrôle, incluez le bit FloppyVolume dans la colonne attributs de l’enregistrement du contrôle dans la [table de contrôle](control-table.md).

Consultez les [attributs de contrôle](control-attributes.md) et le contrôle que vous devez créer sous [contrôles](controls.md).

 

 



