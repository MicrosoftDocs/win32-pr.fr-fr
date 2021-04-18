---
description: Un fournisseur de clichés instantanés doit se conformer aux indications pour garantir la compatibilité du demandeur.
ms.assetid: 49baeb89-1dc9-45c2-a532-071085a8e52f
title: Comportements requis pour les fournisseurs de clichés instantanés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f451dea7154a313cd64a3a46fbcc3b5fe663ec12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519855"
---
# <a name="required-behaviors-for-shadow-copy-providers"></a>Comportements requis pour les fournisseurs de clichés instantanés

Un fournisseur de clichés instantanés doit se conformer aux indications pour garantir la compatibilité du demandeur. Lors de l’exécution, une application de sauvegarde ou tout autre demandeur qui utilise des clichés instantanés doit fonctionner correctement sans aucune connaissance des détails spécifiques de l’implémentation du fournisseur.

## <a name="automagic-resource-management"></a>Gestion des ressources automagic

Le demandeur doit être en mesure d’ajouter simplement un volume à un jeu de clichés instantanés. Le demandeur peut spécifier des attributs de cliché instantané tels **que VSS \_ Volsnap \_ attr \_ transportable**, **VSS \_ Volsnap \_ attr \_ Differential** et/ou **VSS \_ Volsnap \_ attr \_ Plex** dans le contexte de l' [**\_ \_ instantané \_ VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context). Le fournisseur doit respecter ces attributs. S’il ne peut pas honorer ces attributs, il doit indiquer que le jeu de clichés instantanés n’est pas pris en charge en affectant \* à *PbIsSupported* dans [**IVssHardwareSnapshotProvider :: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported) la **valeur false**.

Le fournisseur ne doit jamais accepter de prendre en charge un cliché instantané qu’il ne peut pas créer. Si le demandeur ne spécifie pas d’attribut Plex ou Differential, le fournisseur doit inclure la logique automagic pour allouer l’espace du sous-système pour le cliché instantané et créer le cliché instantané à l’aide de la méthode la plus appropriée. Le fournisseur de matériel ne doit pas inclure d’API spécifique au fournisseur pour la gestion des propriétés de clichés instantanés requises.

## <a name="created-shadow-copy-volumes-are-read-only-and-hidden"></a>Les volumes de clichés instantanés créés sont Read-Only et masqués

VSS définit les indicateurs sur chaque numéro d’unité logique affecté de telle sorte que les volumes de clichés instantanés résultants soient masqués et en lecture seule lorsqu’ils sont détectés par un ordinateur exécutant Windows Server 2003. Les lettres de lecteur et les dossiers montés ne sont pas attribués automatiquement. VSS gère ces indicateurs tout au long du cycle de vie d’un cliché instantané.

## <a name="hardware-shadow-copy-luns-must-be-readwrite"></a>Les numéros d’unité logique de cliché instantané matériel doivent être en lecture/écriture

VSS prend en charge les clichés instantanés matériels uniquement lorsque le numéro d’unité logique sous-jacent est mappé en lecture/écriture. Cette opération doit être effectuée avant la création du cliché instantané. elle ne peut pas être effectuée après le fait. Les fournisseurs de matériel ne doivent pas modifier ces indicateurs. Pour plus d’informations sur la façon dont VSS utilise ces indicateurs, consultez [le processus de création](the-shadow-copy-creation-process.md)de clichés instantanés.

## <a name="auto-import-hardware-shadow-copies-are-not-supported-on-windows-cluster-service"></a>Les clichés instantanés matériels à importation automatique ne sont pas pris en charge sur le service de cluster Windows

Windows service de cluster ne peut pas prendre en charge les numéros d’unité logique avec des signatures et une disposition de partition dupliquées Les numéros d’unités logiques des clichés instantanés doivent être transportés vers un ordinateur hôte situé en dehors du cluster. Pour plus d’informations, consultez [récupération rapide à l’aide de volumes de clichés instantanés transportables](fast-recovery-using-transportable-shadow-copied-volumes.md).

## <a name="shadow-copies-that-contain-dynamic-disks-must-be-transported-to-a-different-host"></a>Les clichés instantanés qui contiennent des disques dynamiques doivent être transportés vers un autre hôte

**Avant Windows Server 2008 :** La prise en charge native des disques dynamiques ne peut pas prendre en charge les numéros d’unités logiques avec des signatures et des contenus de base de données Les numéros d’unités logiques des clichés instantanés doivent être acheminés vers un autre hôte. VSS applique cela en n’autorisant pas l’importation automatique des clichés instantanés de disques dynamiques. Un demandeur ne doit pas importer un cliché instantané transportable sur le même hôte.

**À partir de Windows Server 2008 :** Cette limitation est supprimée.

## <a name="providers-are-out-of-process"></a>Les fournisseurs sont hors processus

Tous les fournisseurs doivent être implémentés en tant que composants COM hors processus.

## <a name="time-critical-operations"></a>Opérations de Time-Critical

Les opérations longues, telles que la synchronisation des plex, doivent être lancées dans [**IVssHardwareSnapshotProvider :: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot). Cette fonction doit démarrer le travail de préparation asynchrone et retourner rapidement. [**IVssProviderCreateSnapshotSet :: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) sert de fonction « Rendezvous » : le fournisseur peut attendre de façon synchrone dans cette méthode pour terminer le travail de préparation qui a été démarré par **BeginPrepareSnapshot**.

Les fournisseurs ne doivent pas ajouter de retards dans [**IVssProviderCreateSnapshotSet ::P recommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-precommitsnapshots), [**IVssProviderCreateSnapshotSet :: CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots)ou [**IVssProviderCreateSnapshotSet ::P ostcommitsnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) , car les applications sont figées pendant ces appels. **CommitSnapshots** doit retourner en quelques secondes, car cette opération est appelée pendant la fenêtre de vidage et de suspension, et la prise en charge du noyau VSS annule le vidage et le blocage si la mise en service n’est pas reçue dans les 10 secondes, ce qui entraîne l’échec du processus de création de clichés instantanés par VSS. Si le fournisseur prend plus de quelques secondes pour effectuer cet appel, il est fort probable que la création du cliché instantané échoue.

## <a name="careful-io-during-commitsnapshots"></a>E/s avec prudence lors de la CommitSnapshots

Les fournisseurs de matériel ne doivent pas avoir besoin d’effectuer des e/s sur les volumes impliqués dans le cliché instantané pendant [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots). Si des e/s sont requises, les fournisseurs ne doivent pas initialiser les e/s sur un volume d’origine lors de la gestion de la méthode **CommitSnapshots** .

Pendant la [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots), les pilotes de prise en charge du noyau VSS bloquent les e/s des volumes d’origine qui sont des clichés instantanés. Si le fournisseur utilise des e/s synchrones sur un volume qui se trouve dans le jeu de clichés instantanés, ces e/s seront bloquées et le processus de validation de cliché instantané sera bloqué. Le fournisseur ne doit pas appeler d’API Win32 pendant **CommitSnapshots** , car il aura une probabilité élevée de provoquer des e/s et un blocage. Le délai d’attente de la prise en charge du noyau VSS interrompt ce blocage au bout de 10 secondes, mais cela entraîne l’échec de la création de clichés instantanés.

Si des e/s doivent être tentées, elles doivent être exécutées de façon asynchrone. L’e/s ne se termine pas tant que tous les fournisseurs n’ont pas retourné leurs méthodes [**CommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-commitsnapshots) . En général, il est préférable d’effectuer ces opérations dans l’appel [**PostCommitSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-postcommitsnapshots) .

## <a name="readwrite-shadow-copy-luns"></a>LUN de clichés instantanés en lecture/écriture

Dans cette version, VSS prend en charge uniquement les numéros d’unités logiques de clichés instantanés en lecture/écriture même si les volumes sont exposés en lecture seule. La raison en est que le système doit modifier les structures de données sur disque, telles que :

-   Signature de disque, qui change pendant le processus de cliché instantané
-   Les structures de données liées aux partitions, y compris celles indiquant que la partition est en lecture seule, masquée, un cliché instantané, et ne doivent pas recevoir de lettre de lecteur.

## <a name="unique-page-83-information"></a>Page unique 83 informations

Le numéro d’unité logique d’origine et le numéro d’unité logique de cliché instantané nouvellement créé doivent avoir au moins un identificateur de stockage unique dans les données de la page 83. Au moins un identificateur de stockage de \_ type 1, 2, 3 ou 8, et une association de 0 doit être unique sur le numéro d’unité logique d’origine et le numéro d’unité logique de cliché instantané nouvellement créé.

 

 



