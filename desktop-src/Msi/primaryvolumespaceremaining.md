---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceRemaining sur une chaîne représentant le nombre total d’octets restants sur le volume référencé par la propriété PrimaryVolumePath, si toutes les fonctionnalités actuellement sélectionnées ont été installées.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Propriété PrimaryVolumeSpaceRemaining
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16107af105de0684bd917177050017a3c14e40aff32c658881342a90e877c973
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580489"
---
# <a name="primaryvolumespaceremaining-property"></a>Propriété PrimaryVolumeSpaceRemaining

Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceRemaining** sur une chaîne représentant le nombre total d’octets restants sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) , si toutes les fonctionnalités actuellement sélectionnées ont été installées. Comme avec la propriété [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , ce nombre est exprimé en unités de 512 octets.

## <a name="remarks"></a>Remarques

Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




