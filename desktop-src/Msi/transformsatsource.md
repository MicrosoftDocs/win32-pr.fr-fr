---
description: La définition de cette propriété est semblable à la définition de la stratégie de stratégie TransformsAtSource, à ceci près que l’étendue est différente.
ms.assetid: b78c3757-d969-4684-84b9-b2acfd9f5c82
title: Propriété TRANSFORMSATSOURCE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e8b0acf2e64976d66f04fbd16ec67a5bb38b7fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526673"
---
# <a name="transformsatsource-property"></a>Propriété TRANSFORMSATSOURCE

La définition de cette propriété est semblable à la définition de la stratégie de [stratégie TransformsAtSource](transformsatsource-policy.md) , à ceci près que l’étendue est différente. La définition de la stratégie TransformsAtSource s’applique à tous les packages installés par un utilisateur donné. La définition de la propriété **TRANSFORMSATSOURCE** s’applique au package, quels que soient les utilisateurs.

## <a name="remarks"></a>Notes

Windows Installer interprète la propriété **TRANSFORMSATSOURCE** comme s’il s’agissait de la propriété [**TRANSFORMSSECURE**](transformssecure.md) . Si l’indicateur @ est passé dans la propriété [**TRANSformations**](transforms.md) , Windows Installer traite les transformations de la liste comme des [transformations sécurisées à la source](secure-at-source-transforms.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




