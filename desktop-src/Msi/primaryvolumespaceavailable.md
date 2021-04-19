---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceAvailable sur une chaîne qui représente le nombre total d’octets disponibles, en unités de 512, sur le volume référencé par la propriété PrimaryVolumePath.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Propriété PrimaryVolumeSpaceAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525242"
---
# <a name="primaryvolumespaceavailable-property"></a>Propriété PrimaryVolumeSpaceAvailable

Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceAvailable** sur une chaîne qui représente le nombre total d’octets disponibles, en unités de 512, sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) .

## <a name="remarks"></a>Notes

Par exemple, si [**PrimaryVolumePath**](primaryvolumepath.md) est défini sur « D : » et que le volume D : a 446 134 272 octets libres, **PrimaryVolumeSpaceAvailable** est défini sur 871356.

Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




