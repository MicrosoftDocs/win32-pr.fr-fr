---
description: le programme d’installation définit la propriété VersionNT sur le numéro de version du système d’exploitation, non défini si le système d’exploitation n’est pas Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 ou Windows 7.
ms.assetid: 49005783-0bcb-458e-8266-56e6ea6afb43
title: Propriété VersionNT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73f2787f7b4914495bc257629e7b50765d7e93ec221cf1aa44d9c1f7e706d127
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995639"
---
# <a name="versionnt-property"></a>Propriété VersionNT

le programme d’installation définit la propriété **VersionNT** sur le numéro de version du système d’exploitation, non défini si le système d’exploitation n’est pas Windows NT, Windows 2000, Windows XP, Windows Vista, Windows Server 2008 ou Windows 7. La valeur est un entier : MajorVersion \* 100 + MinorVersion.

Les instructions conditionnelles qui dépendent du système d’exploitation peuvent utiliser cette propriété.

Voir aussi [valeurs de propriété du système d’exploitation](operating-system-property-values.md).

## <a name="remarks"></a>Remarques

les expressions de Condition peuvent tester Windows NT, Windows 2000 ou Windows XP en utilisant le nom de propriété, ou peuvent vérifier la version à l’aide d’un opérateur de comparaison.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows le programme d’installation sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Windows Service Pack minimale requise par une version Windows Installer, consultez la [configuration requise](windows-installer-portal.md) pour la Run-Time de Windows Installer.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




