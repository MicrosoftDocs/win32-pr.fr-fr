---
description: Les fournisseurs de matériel implémentent les interfaces IVssProviderCreateSnapshotSet et IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Développement de fournisseurs de matériel VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210571"
---
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="febb4-103">Développement de fournisseurs de matériel VSS</span><span class="sxs-lookup"><span data-stu-id="febb4-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="febb4-104">Les fournisseurs de matériel implémentent les interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) et [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) .</span><span class="sxs-lookup"><span data-stu-id="febb4-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="febb4-105">**IVssProviderCreateSnapshotSet** implémente le séquencement d’état de cliché instantané.</span><span class="sxs-lookup"><span data-stu-id="febb4-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="febb4-106">**IVssHardwareSnapshotProvider** opère sur une abstraction de LUN.</span><span class="sxs-lookup"><span data-stu-id="febb4-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="febb4-107">Les fournisseurs doivent être implémentés en tant que serveur COM hors processus.</span><span class="sxs-lookup"><span data-stu-id="febb4-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="febb4-108">Les fournisseurs utilisent des mécanismes spécifiques au fournisseur (souvent des IOCTL privées) pour communiquer avec le sous-système de stockage qui instancie les numéros d’unités logiques de clichés instantanés.</span><span class="sxs-lookup"><span data-stu-id="febb4-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="febb4-109">Inscription et chargement du fournisseur de clichés instantanés</span><span class="sxs-lookup"><span data-stu-id="febb4-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="febb4-110">Création de clichés instantanés pour les fournisseurs</span><span class="sxs-lookup"><span data-stu-id="febb4-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="febb4-111">Interactions et comportements des fournisseurs de matériel</span><span class="sxs-lookup"><span data-stu-id="febb4-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



