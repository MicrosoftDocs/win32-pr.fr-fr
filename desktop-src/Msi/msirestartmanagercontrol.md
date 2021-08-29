---
description: la propriété MSIRESTARTMANAGERCONTROL spécifie si le package Windows Installer utilise les fonctionnalités du gestionnaire de redémarrage ou de la boîte de dialogue FilesInUse.
ms.assetid: fefff18b-892a-440e-9f57-d23aeb99af74
title: Propriété MSIRESTARTMANAGERCONTROL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912f529187560aa5fffff90407573e5438139d2b2d26345645752c8d30416f60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065959"
---
# <a name="msirestartmanagercontrol-property"></a>Propriété MSIRESTARTMANAGERCONTROL

la propriété **MSIRESTARTMANAGERCONTROL** spécifie si le package Windows Installer utilise les fonctionnalités du [gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) ou de la [boîte de dialogue FilesInUse](filesinuse-dialog.md) .

## <a name="value"></a>Valeur



| Valeur                                                                                        | Signification                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl>                 | Il s’agit de la valeur par défaut si la propriété n’est pas définie. Windows le programme d’installation tente toujours d’utiliser le [gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) sur Windows Vista.<br/>                                                                                                                                                                                                       |
| <dl> <dt>Désactive</dt> </dl>         | Désactive l’interaction du package avec le gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md). Windows Le programme d’installation utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md). <br/>                                                                                                                                                                                                      |
| <dl> <dt>"DisableShutdown"</dt> </dl> | Windows Le programme d’installation utilise la [boîte de dialogue FilesInUse](filesinuse-dialog.md). ce paramètre désactive les tentatives du gestionnaire de [redémarrage](../rstmgr/restart-manager-portal.md) afin d’atténuer les redémarrages lors de l’installation d’un Windows Installer package qui n’a pas été créé pour utiliser le gestionnaire de redémarrage. Le programme d’installation utilise toujours le gestionnaire de redémarrage pour détecter les fichiers utilisés par les applications. <br/> |



 

## <a name="remarks"></a>Remarques

La propriété **MSIRESTARTMANAGERCONTROL** est ignorée si le [Gestionnaire de redémarrage](../rstmgr/restart-manager-portal.md) n’est pas disponible ou est désactivé.

La valeur de cette propriété peut être modifiée à l’aide de transformations ou de mises à niveau de personnalisation. La modification de la valeur de cette propriété à partir d’actions personnalisées n’a aucun effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. pour plus d’informations sur la Service Pack minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[DisableAutomaticApplicationShutdown](disableautomaticapplicationshutdown.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
