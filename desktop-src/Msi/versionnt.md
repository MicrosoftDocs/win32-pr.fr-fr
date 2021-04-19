---
description: Le programme d’installation définit la propriété VersionNT sur le numéro de version du système d’exploitation, non défini si le système d’exploitation n’est pas Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 ou Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propriété VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61ce8d7d5c738be3b2fd51f2ca3054b8800d4c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535241"
---
# <a name="versionnt-property"></a>Propriété VersionNT

Le programme d’installation définit la propriété **VersionNT** sur le numéro de version du système d’exploitation, non défini si le système d’exploitation n’est pas Windows NT, Windows 2000, Windows XP, Windows Vista, windows Server 2008 ou Windows 7. La valeur est un entier : MajorVersion \* 100 + MinorVersion.

Les instructions conditionnelles qui dépendent du système d’exploitation peuvent utiliser cette propriété.

Voir aussi [valeurs de propriété du système d’exploitation](operating-system-property-values.md).

## <a name="remarks"></a>Notes

Les expressions de condition peuvent tester Windows NT, Windows 2000 ou Windows XP en utilisant le nom de propriété, ou peuvent vérifier la version à l’aide d’un opérateur de comparaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP, consultez la [Configuration requise de la Windows Installer Run-Time](windows-installer-portal.md) pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




