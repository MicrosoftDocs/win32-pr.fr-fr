---
description: Le programme d’installation définit la valeur de la propriété MsiSystemRebootPending sur 1 s’il existe une opération en attente pour renommer un fichier.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Propriété MsiSystemRebootPending
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526362"
---
# <a name="msisystemrebootpending-property"></a>Propriété MsiSystemRebootPending

Le programme d’installation définit la valeur de la propriété **MsiSystemRebootPending** sur 1 s’il existe une opération en attente pour renommer un fichier.

Les auteurs de package peuvent baser une condition dans la [table LaunchCondition](launchcondition-table.md) sur cette propriété pour empêcher l’installation de leur package dans les cas où une opération est en attente pour renommer un fichier. Cela peut être fait pour empêcher un redémarrage du système d’exploitation provoqué par le changement de nom du fichier. Le programme d’installation ne définit pas la propriété **MsiSystemRebootPending** dans tous les cas qui requièrent un redémarrage du système.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[Redémarrages du système](system-reboots.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




