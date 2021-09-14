---
description: Insérez l’action ScheduleReboot dans la séquence d’action pour inviter l’utilisateur à redémarrer le système à la fin de l’installation. Utilisez l’action ForceReboot pour demander un redémarrage lors de l’installation.
ms.assetid: 36f24f57-f1f0-4eca-9b6d-1b25fb73fa96
title: Action ScheduleReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460e3f25283c233fac80b25edd91d4bd102de435
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021253"
---
# <a name="schedulereboot-action"></a>Action ScheduleReboot

Insérez l’action ScheduleReboot dans la séquence d’action pour inviter l’utilisateur à redémarrer le système à la fin de l’installation. Utilisez l' [action ForceReboot](forcereboot-action.md) pour demander un redémarrage lors de l’installation.

Si l’installation a une interface utilisateur, le programme d’installation affiche une boîte de message et un bouton à la fin de l’installation, en demandant si l’utilisateur souhaite redémarrer le système. L’utilisateur doit répondre à cette invite avant de terminer l’installation. Si l’installation n’a pas d’interface utilisateur, le système redémarre automatiquement à la fin.

Si le programme d’installation détermine qu’un redémarrage est nécessaire, il invite automatiquement l’utilisateur à redémarrer à la fin de l’installation, qu’il y ait ou non des actions ForceReboot ou ScheduleReboot dans la séquence. Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers en cours d’utilisation pendant l’installation.

Vous pouvez supprimer certaines invites pour les redémarrages en définissant la propriété [**reboot**](reboot.md) .

si le Windows Installer rencontre l’action [ForceReboot](forcereboot-action.md) ou ScheduleReboot lors d’une [installation de plusieurs packages](multiple-package-installations.md), le programme d’installation s’arrête et annule l’installation. D’autres packages appartenant à l’installation de plusieurs packages, qui ne contiennent pas d’action ForceReboot ou ScheduleReboot, peuvent être installés.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Il n’existe aucune restriction de séquence.

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

Par exemple, cette action peut être utilisée pour forcer le programme d’installation à demander un redémarrage après l’installation des pilotes qui nécessitent un redémarrage. Si le programme d’installation tente de remplacer des fichiers qui sont en cours d’utilisation, il invite automatiquement l’utilisateur à redémarrer même si ScheduleReboot n’a pas été utilisé.

L’action ScheduleReboot est généralement placée à la fin de la séquence, mais elle peut être insérée à n’importe quel point de la séquence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Redémarrages du système](system-reboots.md)
</dt> </dl>

 

 



