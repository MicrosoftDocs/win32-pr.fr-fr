---
description: Le programme d’installation définit la valeur de la propriété PrimaryVolumeSpaceRequired sur une chaîne représentant le nombre total d’octets requis par toutes les fonctionnalités sélectionnées sur le volume référencé par la propriété PrimaryVolumePath.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Propriété PrimaryVolumeSpaceRequired
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127110950"
---
# <a name="primaryvolumespacerequired-property"></a>Propriété PrimaryVolumeSpaceRequired

Le programme d’installation définit la valeur de la propriété **PrimaryVolumeSpaceRequired** sur une chaîne représentant le nombre total d’octets requis par toutes les fonctionnalités sélectionnées sur le volume référencé par la propriété [**PrimaryVolumePath**](primaryvolumepath.md) . Comme avec la propriété [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , ce nombre est exprimé en unités de 512 octets.

## <a name="remarks"></a>Notes

Remarque Si cette valeur doit être affichée dans un contrôle de [texte](text-control.md)statique, le bit de mise [en forme peut](formatsize-control-attribute.md) être utilisé pour mettre automatiquement en forme et étiqueter ce nombre en unités de kilo-octets ou mégaoctets selon le cas.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




