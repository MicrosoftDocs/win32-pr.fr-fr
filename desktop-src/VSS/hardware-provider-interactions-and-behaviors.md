---
description: Interactions et comportements des fournisseurs de matériel
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interactions et comportements des fournisseurs de matériel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7c8029b32ee3387b86519da8630d995820bf3dab5da79769ca26f618ef32660
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118122058"
---
# <a name="hardware-provider-interactions-and-behaviors"></a>Interactions et comportements des fournisseurs de matériel

Les fournisseurs de matériel peuvent prendre en charge les clichés instantanés de copie en écriture et/ou de copie complète (différentielle et/ou Plex). L’allocation de ressources pour les clichés instantanés doit suivre le contexte spécifié par le demandeur dans [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), énuméré par le [**\_ \_ \_ contexte de capture instantanée VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), pour le jeu de clichés instantanés.

-   Si le demandeur spécifie un contexte de cliché instantané qui est pris en charge par le fournisseur, le fournisseur doit créer un cliché instantané à l’aide de cette méthode.
-   Si le demandeur spécifie un contexte de cliché instantané qui n’est pas pris en charge par le fournisseur, le fournisseur ne doit pas tenter de créer le cliché instantané et retourner la **valeur false** par le biais du paramètre *pbIsSupported* dans [**IVssHardwareSnapshotProvider :: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).
-   Si le demandeur ne spécifie pas explicitement un contexte de cliché instantané, le fournisseur doit utiliser un comportement par défaut raisonnable pour la création de clichés instantanés.

Les fournisseurs de matériel associés aux sous-systèmes RAID SAN doivent prendre en charge les clichés instantanés transportables pour permettre le déplacement entre les ordinateurs hôtes d’un réseau SAN.

Les fournisseurs de matériel exécutés sur plusieurs ordinateurs sur un réseau SAN qui gèrent le même sous-système RAID n’ont pas besoin de coordonner les fournisseurs sur un réseau SAN. Le coordinateur gère tout état nécessaire. Deux types d’État sont reconnus :

-   État nécessaire pour prendre en charge l’accès aux données sur les volumes contenus dans un cliché instantané matériel. Cela comprend le marquage d’un volume en lecture seule ou masqué. Cet État doit être sur le numéro d’unité logique matériel et se déplacer avec le numéro d’unité logique. Cet État est conservé entre les époques de démarrage et/ou la découverte des appareils. VSS gère cet État pendant la durée de vie du cliché instantané.
-   État nécessaire pour reconnaître un volume spécifique dans le cadre d’un jeu de clichés instantanés. Cet État est conservé par VSS conjointement avec le demandeur qui a créé le jeu de clichés instantanés à l’origine.

Pour plus d'informations, voir les rubriques suivantes :

-   [Processus de création de clichés instantanés](the-shadow-copy-creation-process.md)
-   [Comportements requis pour les fournisseurs de clichés instantanés](required-behaviors-for-shadow-copy-providers.md)
-   [Transitions d’État dans les fournisseurs de clichés instantanés](state-transitions-in-shadow-copy-providers.md)
-   [Gestion des erreurs dans les fournisseurs de clichés instantanés](error-handling-in-shadow-copy-providers.md)

 

 



