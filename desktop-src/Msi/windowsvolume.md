---
description: Le programme d’installation définit la propriété WindowsVolume sur le volume du dossier Windows.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Propriété WindowsVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007303"
---
# <a name="windowsvolume-property"></a>Propriété WindowsVolume

Le programme d’installation définit la propriété **WindowsVolume** sur le volume du dossier Windows. La propriété se termine toujours par une barre oblique inverse. cela peut être utilisé pour définir l’emplacement par défaut sur le volume sur lequel se trouve le dossier Windows, car la propriété [**ROOTDRIVE**](rootdrive.md) n’est pas nécessairement égale à ce lecteur.

## <a name="remarks"></a>Notes

N’utilisez pas la propriété **WindowsVolume** dans la colonne Directory de la table [Directory](directory-table.md) . la propriété [**WindowsFolder**](windowsfolder.md) contient le chemin d’accès au dossier Windows.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows le programme d’installation sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Windows Service Pack minimale requise par une version Windows Installer, consultez la [configuration requise](windows-installer-portal.md) pour la Run-Time de Windows Installer.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




