---
description: Interactions et comportements des fournisseurs de matériel
ms.assetid: 059968cf-43e5-4442-b757-80afdd66799f
title: Interactions et comportements des fournisseurs de matériel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa30add6b34a7f3a0c45c88346c32c43e99398e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202385"
---
# <a name="hardware-provider-interactions-and-behaviors"></a><span data-ttu-id="22b75-103">Interactions et comportements des fournisseurs de matériel</span><span class="sxs-lookup"><span data-stu-id="22b75-103">Hardware Provider Interactions and Behaviors</span></span>

<span data-ttu-id="22b75-104">Les fournisseurs de matériel peuvent prendre en charge les clichés instantanés de copie en écriture et/ou de copie complète (différentielle et/ou Plex).</span><span class="sxs-lookup"><span data-stu-id="22b75-104">Hardware providers may support copy-on-write and/or full copy mirror (differential and/or plex) shadow copies.</span></span> <span data-ttu-id="22b75-105">L’allocation de ressources pour les clichés instantanés doit suivre le contexte spécifié par le demandeur dans [**IVssBackupComponents :: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), énuméré par le [**\_ \_ \_ contexte de capture instantanée VSS**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), pour le jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="22b75-105">Resource allocation for shadow copies should follow the context specified by the requester in [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext), enumerated by [**\_VSS\_SNAPSHOT\_CONTEXT**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context), for the shadow copy set.</span></span>

-   <span data-ttu-id="22b75-106">Si le demandeur spécifie un contexte de cliché instantané qui est pris en charge par le fournisseur, le fournisseur doit créer un cliché instantané à l’aide de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="22b75-106">If the requester specifies a shadow copy context that is supported by the provider, the provider should create a shadow copy using that method.</span></span>
-   <span data-ttu-id="22b75-107">Si le demandeur spécifie un contexte de cliché instantané qui n’est pas pris en charge par le fournisseur, le fournisseur ne doit pas tenter de créer le cliché instantané et retourner la **valeur false** par le biais du paramètre *pbIsSupported* dans [**IVssHardwareSnapshotProvider :: AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span><span class="sxs-lookup"><span data-stu-id="22b75-107">If the requester specifies a shadow copy context that is not supported by the provider, then the provider should not attempt to create the shadow copy and return **FALSE** through the *pbIsSupported* parameter in [**IVssHardwareSnapshotProvider::AreLunsSupported**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-arelunssupported).</span></span>
-   <span data-ttu-id="22b75-108">Si le demandeur ne spécifie pas explicitement un contexte de cliché instantané, le fournisseur doit utiliser un comportement par défaut raisonnable pour la création de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="22b75-108">If the requester does not explicitly specify a shadow copy context, then the provider should use reasonable default behavior for shadow copy creation.</span></span>

<span data-ttu-id="22b75-109">Les fournisseurs de matériel associés aux sous-systèmes RAID SAN doivent prendre en charge les clichés instantanés transportables pour permettre le déplacement entre les ordinateurs hôtes d’un réseau SAN.</span><span class="sxs-lookup"><span data-stu-id="22b75-109">Hardware providers associated with SAN RAID subsystems should support transportable shadow copies to allow movement between hosts on a SAN.</span></span>

<span data-ttu-id="22b75-110">Les fournisseurs de matériel exécutés sur plusieurs ordinateurs sur un réseau SAN qui gèrent le même sous-système RAID n’ont pas besoin de coordonner les fournisseurs sur un réseau SAN.</span><span class="sxs-lookup"><span data-stu-id="22b75-110">Hardware providers running on multiple machines on a SAN yet managing the same RAID subsystem do not need to coordinate between providers on a SAN.</span></span> <span data-ttu-id="22b75-111">Le coordinateur gère tout état nécessaire.</span><span class="sxs-lookup"><span data-stu-id="22b75-111">The coordinator maintains any necessary state.</span></span> <span data-ttu-id="22b75-112">Deux types d’État sont reconnus :</span><span class="sxs-lookup"><span data-stu-id="22b75-112">Two kinds of state are recognized:</span></span>

-   <span data-ttu-id="22b75-113">État nécessaire pour prendre en charge l’accès aux données sur les volumes contenus dans un cliché instantané matériel.</span><span class="sxs-lookup"><span data-stu-id="22b75-113">State necessary to support data access to the volumes contained on a hardware shadow copy.</span></span> <span data-ttu-id="22b75-114">Cela comprend le marquage d’un volume en lecture seule ou masqué.</span><span class="sxs-lookup"><span data-stu-id="22b75-114">This includes any tagging of a volume as read-only or hidden.</span></span> <span data-ttu-id="22b75-115">Cet État doit être sur le numéro d’unité logique matériel et se déplacer avec le numéro d’unité logique.</span><span class="sxs-lookup"><span data-stu-id="22b75-115">This state must be on the hardware LUN and travel with the LUN.</span></span> <span data-ttu-id="22b75-116">Cet État est conservé entre les époques de démarrage et/ou la découverte des appareils.</span><span class="sxs-lookup"><span data-stu-id="22b75-116">This state is preserved across boot epochs and/or device discovery.</span></span> <span data-ttu-id="22b75-117">VSS gère cet État pendant la durée de vie du cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="22b75-117">VSS manages this state for the lifetime of the shadow copy.</span></span>
-   <span data-ttu-id="22b75-118">État nécessaire pour reconnaître un volume spécifique dans le cadre d’un jeu de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="22b75-118">State necessary to recognize a specific volume as part of a shadow copy set.</span></span> <span data-ttu-id="22b75-119">Cet État est conservé par VSS conjointement avec le demandeur qui a créé le jeu de clichés instantanés à l’origine.</span><span class="sxs-lookup"><span data-stu-id="22b75-119">This state is persisted by VSS in conjunction with the requester that originally created the shadow copy set.</span></span>

<span data-ttu-id="22b75-120">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="22b75-120">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="22b75-121">Processus de création de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="22b75-121">The Shadow Copy Creation Process</span></span>](the-shadow-copy-creation-process.md)
-   [<span data-ttu-id="22b75-122">Comportements requis pour les fournisseurs de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="22b75-122">Required Behaviors for Shadow Copy Providers</span></span>](required-behaviors-for-shadow-copy-providers.md)
-   [<span data-ttu-id="22b75-123">Transitions d’État dans les fournisseurs de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="22b75-123">State Transitions in shadow copy providers</span></span>](state-transitions-in-shadow-copy-providers.md)
-   [<span data-ttu-id="22b75-124">Gestion des erreurs dans les fournisseurs de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="22b75-124">Error Handling in shadow copy providers</span></span>](error-handling-in-shadow-copy-providers.md)

 

 



