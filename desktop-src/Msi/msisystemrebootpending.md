---
description: Le programme d’installation définit la valeur de la propriété MsiSystemRebootPending sur 1 s’il existe une opération en attente pour renommer un fichier.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propriété MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6cab600ca7c0f1bbc240f8fb1a9d93f3da62914e8250863333b75f8973d6c1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042649"
---
# <a name="msisystemrebootpending-property"></a>Propriété MsiSystemRebootPending

Le programme d’installation définit la valeur de la propriété **MsiSystemRebootPending** sur 1 s’il existe une opération en attente pour renommer un fichier.

Les auteurs de package peuvent baser une condition dans la [table LaunchCondition](launchcondition-table.md) sur cette propriété pour empêcher l’installation de leur package dans les cas où une opération est en attente pour renommer un fichier. Cela peut être fait pour empêcher un redémarrage du système d’exploitation provoqué par le changement de nom du fichier. Le programme d’installation ne définit pas la propriété **MsiSystemRebootPending** dans tous les cas qui requièrent un redémarrage du système.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Redémarrages du système](system-reboots.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




