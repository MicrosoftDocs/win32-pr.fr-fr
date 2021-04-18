---
description: Le PRIMARYFOLDER est une propriété globale qui permet à l’auteur de désigner un dossier principal pour l’installation.
ms.assetid: 7ba776de-53e5-491a-917b-37778fe0c438
title: Propriété PRIMARYFOLDER
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 242b8adc9c753e3d1cb91c40798471852d9f2414
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532986"
---
# <a name="primaryfolder-property"></a>Propriété PRIMARYFOLDER

Le **PRIMARYFOLDER** est une propriété globale qui permet à l’auteur de désigner un dossier principal pour l’installation. La valeur de cette propriété doit être le nom de clé d’un répertoire qui existe dans la [table de répertoires](directory-table.md).

Le programme d’installation utilise le chemin d’accès résolu du dossier principal pour déterminer le volume à utiliser lors de la définition des valeurs de la propriété [**PrimaryVolumePath**](primaryvolumepath.md) , de la propriété [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) , de la propriété [**PrimaryVolumeSpaceRequired**](primaryvolumespacerequired.md) et de la propriété [**PrimaryVolumeSpaceRemaining**](primaryvolumespaceremaining.md) . Le programme d’installation fournit les valeurs de ces dernières propriétés aux utilisateurs dans l’interface utilisateur pour les aider à gérer l’espace disque. Les auteurs de package courants peuvent sélectionner le plus grand dossier comme dossier principal.

La valeur de cette propriété doit être le nom de clé d’un enregistrement de répertoire trouvé dans la [table de répertoires](directory-table.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> </dl>

 

 




