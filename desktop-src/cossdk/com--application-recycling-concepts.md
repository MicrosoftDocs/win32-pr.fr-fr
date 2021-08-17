---
description: Le recyclage des applications peut augmenter considérablement la stabilité globale de vos applications COM+ en proposant un correctif rapide pour les problèmes connus et en vous aidant à vous protéger contre les problèmes inattendus.
ms.assetid: bf98318b-4d87-44cc-85a1-68faf5547e06
title: Concepts de recyclage des applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6a635487427fce3f17203f11426261996348a5e4057ab8bceebcae552d51bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129261"
---
# <a name="com-application-recycling-concepts"></a>Concepts de recyclage des applications COM+

Le recyclage des applications peut augmenter considérablement la stabilité globale de vos applications COM+ en proposant un correctif rapide pour les problèmes connus et en vous aidant à vous protéger contre les problèmes inattendus. Par exemple, les performances de l’application peuvent se dégrader au fil du temps en raison de problèmes tels que les fuites de mémoire, l’utilisation des ressources non évolutives et l’échec du processus. COM+ fournit le recyclage des applications comme solution à ces problèmes. Vous pouvez utiliser le recyclage d’applications pour arrêter automatiquement un processus et le redémarrer, ce qui a pour conséquence la réinitialisation d’un processus défaillant et la réallocation de mémoire qu’il utilise.

Le recyclage d’applications s’effectue en créant un doublon du processus Dllhost associé à une application. Ce processus Dllhost duplique toutes les futures demandes d’objets, ce qui laisse l’ancien Dllhost terminer la maintenance des demandes d’objets restantes. L’ancien processus Dllhost est arrêté lorsqu’il détecte la publication de toutes les références externes aux objets du processus ou lorsque la valeur du délai d’expiration est atteinte. Grâce à ce comportement, le recyclage d’applications garantit qu’une application cliente ne rencontre pas d’interruption de service.

> [!Note]  
> vous ne pouvez pas recycler une application COM+ qui a été configurée pour s’exécuter en tant que service Windows. En outre, les applications de bibliothèque disposent des propriétés de recyclage et de regroupement de leur processus hôte.

 

Vous pouvez configurer le recyclage d’applications de manière administrative, à l’aide de l’outil d’administration Services de composants, ou par programme, via le kit de développement logiciel (SDK) d’administration COM+. Vous pouvez recycler les processus en fonction de plusieurs critères, déterminés par les propriétés suivantes d’un objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection d' [**applications**](applications.md) :

-   **RecycleLifetimeLimit.** Nombre maximal de minutes pendant lesquelles un processus peut s’exécuter avant son recyclage. La plage valide est comprise entre 0 et 30 240 minutes (21 jours). Le nombre de minutes par défaut est 0, ce qui indique que le processus ne se recyclera pas pour atteindre une limite de durée de vie.
-   **RecycleMemoryLimit.** Quantité maximale d’utilisation de la mémoire de processus (en kilo-octets) avant le recyclage du processus. Si l’utilisation de la mémoire de processus dépasse le nombre spécifié pendant plus d’une minute, le processus est recyclé. La plage valide est comprise entre 0 et 1 048 576 Ko. La quantité d’utilisation de la mémoire par défaut est de 0 Ko, ce qui indique que le processus ne recyclera pas d’atteindre une limite de mémoire.
-   **RecycleCallLimit.** Nombre maximal d’appels que les objets d’application peuvent accepter avant de recycler le processus. La plage valide est comprise entre 0 et 1 048 576 appels. Le nombre d’appels par défaut est 0, ce qui indique que le processus ne sera pas recyclé pour atteindre une limite d’appel.
-   **RecycleActivationLimit.** Nombre maximal d’activations d’objets d’application à accepter avant de recycler le processus. La plage valide est comprise entre 0 et 1 048 576. Le nombre d’activations par défaut est 0, ce qui indique que le processus ne sera pas recyclé pour atteindre une limite d’activation.

En outre, la propriété RecycleExpirationTimeout de l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) est utilisée pour forcer l’arrêt d’un processus recyclé. Elle indique le nombre de minutes d’attente pour la libération de toutes les références externes aux objets dans le processus recyclé avant de forcer l’arrêt du processus. La plage valide est comprise entre 1 et 1440 minutes (24 heures) et le délai d’expiration par défaut est de 15 minutes. Cette valeur est utilisée uniquement lorsqu’il est déjà déterminé qu’un processus sera recyclé selon les autres critères.

Vous pouvez sélectionner plusieurs critères pour le recyclage d’une application. COM+ recycle l’application une fois que le premier du jeu de critères est satisfait. Vous pouvez définir la valeur du délai d’expiration pour déterminer la durée pendant laquelle un ancien processus Dllhost peut consacrer des demandes de service restantes avant d’être arrêté de force.

La collection [**ApplicationInstances**](applicationinstances.md) fournit la propriété HasRecycled, qui permet de déterminer si l’application a déjà été recyclée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de recyclage des applications COM+](com--application-recycling-tasks.md)
</dt> <dt>

[**RecycleSurrogate**](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)
</dt> </dl>

 

 



