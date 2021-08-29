---
description: La propriété reboot supprime certaines invites pour un redémarrage du système.
ms.assetid: d88752cd-f59d-4214-b5b5-ce126500aa4e
title: Reboot, propriété
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de2dbba173d40d59be4ece4578267aa1f2829d62f6583c0ce05ef94598fa491
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913039"
---
# <a name="reboot-property"></a>Reboot, propriété

La propriété **reboot** supprime certaines invites pour un redémarrage du système. Un administrateur utilise généralement cette propriété avec une série d’installations pour installer plusieurs produits en même temps avec un seul redémarrage à la fin. Pour plus d’informations, consultez [redémarrages du système](system-reboots.md).

Les actions [ForceReboot](forcereboot-action.md) et [ScheduleReboot](schedulereboot-action.md) indiquent au programme d’installation d’inviter l’utilisateur à redémarrer le système. Le programme d’installation peut également déterminer qu’un redémarrage est nécessaire, qu’il y ait des actions ForceReboot ou ScheduleReboot dans la séquence. Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers en cours d’utilisation pendant l’installation.

Vous pouvez supprimer certaines invites pour les redémarrages en définissant la propriété **reboot** comme suit.



| Valeur de redémarrage   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Force          | Toujours demander un redémarrage à la fin de l’installation. L’interface utilisateur invite toujours l’utilisateur à redémarrer à la fin. S’il n’existe pas d’interface utilisateur et qu’il ne s’agit pas d’une [installation de plusieurs packages](multiple-package-installations.md), le système redémarre automatiquement à la fin de l’installation. S’il s’agit d’une installation de plusieurs packages, il n’y a pas de redémarrage automatique du système et le programme d’installation retourne l’erreur \_ redémarrage de la réussite \_ \_ obligatoire. |
| Suppress       | Supprimer les invites de redémarrage à la fin de l’installation. Le programme d’installation invite toujours l’utilisateur à redémarrer au cours de l’installation chaque fois qu’il rencontre l' [action ForceReboot](forcereboot-action.md). S’il n’existe pas d’interface utilisateur, le système redémarre automatiquement à chaque ForceReboot. Le redémarrage à la fin de l’installation (par exemple, dû à une tentative d’installation d’un fichier en cours d’utilisation) est supprimé.                                    |
| ReallySuppress | Supprimez tous les redémarrages et redémarrez les invites lancées par ForceReboot lors de l’installation. À la fin de l’installation, supprimez tous les redémarrages et redémarrez les invites. L’invite de redémarrage et le redémarrage proprement dit sont supprimés. Par exemple, le redémarrage à la fin de l’installation, provoqué par une tentative d’installation d’un fichier en cours d’utilisation, est supprimé.                                                                                                                    |



 

## <a name="remarks"></a>Remarques

Le programme d’installation évalue uniquement le premier caractère de la propriété **reboot** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP. pour plus d’informations sur la Service Pack de Windows minimale requise par une version de Windows Installer, consultez la [configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés](properties.md)
</dt> <dt>

[**Propriété REBOOTPROMPT**](rebootprompt.md)
</dt> <dt>

[Redémarrages du système](system-reboots.md)
</dt> </dl>

 

 




