---
description: L’action ForceReboot invite l’utilisateur à redémarrer le système pendant l’installation.
ms.assetid: e1bcdd59-8cbc-46f7-b908-c8cbc2ea0539
title: Action ForceReboot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807bab474f1faacfbc7684797b7a0b7b74f354d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520012"
---
# <a name="forcereboot-action"></a>Action ForceReboot

L’action ForceReboot invite l’utilisateur à redémarrer le système pendant l’installation. L’action ForceReboot est différente de l' [action ScheduleReboot](schedulereboot-action.md) , car l’action ScheduleReboot est utilisée pour planifier une invite de redémarrage à la fin de l’installation.

Si l’installation a une interface utilisateur, le programme d’installation affiche une boîte de dialogue à chaque action ForceReboot qui invite l’utilisateur à redémarrer le système. L’utilisateur doit répondre à cette invite avant de poursuivre l’installation. Si l’installation n’a pas d’interface utilisateur, le système redémarre automatiquement à l’action ForceReboot.

Si le programme d’installation détermine qu’un redémarrage est nécessaire, il invite automatiquement l’utilisateur à redémarrer à la fin de l’installation, qu’il y ait ou non des actions ForceReboot ou ScheduleReboot dans la séquence. Par exemple, le programme d’installation demande automatiquement un redémarrage s’il doit remplacer les fichiers utilisés lors de l’installation.

Supprimez certaines invites de redémarrage en définissant la propriété [**reboot**](reboot.md) .

Si le Windows Installer rencontre l’action ForceReboot ou [ScheduleReboot](schedulereboot-action.md) lors d’une [installation de plusieurs packages](multiple-package-installations.md), le programme d’installation s’arrête et annule l’installation. D’autres packages appartenant à l’installation de plusieurs packages, qui ne contiennent pas d’action ForceReboot ou ScheduleReboot, peuvent être installés.

## <a name="sequence-restrictions"></a>Restrictions de séquence

Les actions suivantes se produisent généralement ensemble en tant que groupe dans la séquence d’action. Il est recommandé que l’action ForceReboot soit planifiée pour venir après ce groupe. Si l’action ForceReboot est planifiée avant l' [action RegisterProduct](registerproduct-action.md), le programme d’installation requiert à nouveau la source du package d’installation après le redémarrage. Par conséquent, la séquence par défaut pour ForceReboot suit immédiatement cette séquence d’action.

-   [RegisterProduct](registerproduct-action.md)
-   [RegisterUser](registeruser-action.md)
-   [PublishProduct](publishproduct-action.md)
-   [PublishFeatures](publishfeatures-action.md)
-   [CreateShortcuts](createshortcuts-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)

L’action ForceReboot doit être comprise entre [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md) dans la séquence d’action de la [table InstallExecuteSequence](installexecutesequence-table.md).

## <a name="actiondata-messages"></a>Messages ActionData

Il n’y a aucun message ActionData.

## <a name="remarks"></a>Notes

L’action ForceReboot doit toujours être utilisée avec une instruction conditionnelle de sorte que le programme d’installation déclenche un redémarrage uniquement lorsque cela est nécessaire. Par exemple, un redémarrage peut être nécessaire uniquement si un fichier particulier est remplacé ou si un composant particulier est installé. Chaque installation de produit est unique et une action personnalisée peut être nécessaire pour déterminer si un redémarrage est nécessaire. La condition sur l’action ForceReboot utilise généralement la propriété [**AFTERREBOOT**](afterreboot.md) .

ForceReboot exécute les opérations système générées par les actions précédentes avant de demander un redémarrage ou un redémarrage. Par exemple, les opérations système générées par [InstallFiles](installfiles-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) sont exécutées avant un redémarrage.

L’action ForceReboot écrit une clé de Registre qui entraîne le démarrage du programme d’installation après le redémarrage. L’emplacement de cette clé est **HKEY \_ local \_ machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Redémarrages du système](system-reboots.md)
</dt> </dl>

 

 



