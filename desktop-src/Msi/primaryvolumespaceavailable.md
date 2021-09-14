---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceAvailable sur une chaîne qui représente le nombre total d’octets disponibles, en unités de 512, sur le volume référencé par la propriété PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propriété PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110973"
---
# <a name="primaryvolumespaceavailable-property"></a>Propriété PrimaryVolumeSpaceAvailable

Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceAvailable** sur une chaîne qui représente le nombre total d’octets disponibles, en unités de 512, sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) .

## <a name="remarks"></a>Notes

Par exemple, si [**PrimaryVolumePath**](primaryvolumepath.md) est défini sur « D : » et que le volume D : a 446 134 272 octets libres, **PrimaryVolumeSpaceAvailable** est défini sur 871356.

Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




