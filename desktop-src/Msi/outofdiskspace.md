---
description: Le programme d’installation définit la propriété OutOfDiskSpace sur TRUE si un volume qui est une cible de l’installation actuelle ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation.
ms.assetid: fb1e3be7-12dd-4036-b657-b91b480fca4a
title: Propriété OutOfDiskSpace
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3a438661e931547b0025f2bf85a2ccc03899f5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525243"
---
# <a name="outofdiskspace-property"></a>Propriété OutOfDiskSpace

Le programme d’installation définit la propriété **OutOfDiskSpace** sur true si un volume qui est une cible de l’installation actuelle ne dispose pas de suffisamment d’espace disque pour s’adapter à l’installation. Si tous les volumes disposent de suffisamment d’espace, la valeur est FALSe. Les actions de résolution de sélection utilisent cette valeur pour annuler une installation et générer une boîte de dialogue.

Cette propriété est valide à tout moment après l’exécution de l' [action CostFinalize](costfinalize-action.md) . L’état de la propriété [**OutOfNoRbDiskSpace**](outofnorbdiskspace.md) est mis à jour de manière dynamique chaque fois que le coût total d’installation est recalculé (par exemple, chaque fois que l’état d’installation d’une fonctionnalité est modifié via la boîte de dialogue de [sélection](selection-dialog.md) ).

## <a name="remarks"></a>Notes

Toute boîte de dialogue reposant sur la propriété **OutOfDiskSpace** pour déterminer s’il faut afficher une boîte de dialogue doit définir le [bit de style](trackdiskspace-dialog-style-bit.md) de la boîte de dialogue TrackDiskSpace pour la boîte de dialogue afin de mettre à jour dynamiquement l’espace sur les volumes cibles.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




