---
description: Partitions par défaut
ms.assetid: ce6ad7c1-d4a1-4573-860e-f7859c588773
title: Partitions par défaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5115b6b2480958c78a53c264804eb1f292808545
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201124"
---
# <a name="default-partitions"></a><span data-ttu-id="8c3f2-103">Partitions par défaut</span><span class="sxs-lookup"><span data-stu-id="8c3f2-103">Default Partitions</span></span>

<span data-ttu-id="8c3f2-104">Lorsqu’une partition par défaut est affectée à un utilisateur, COM+ tente d’abord d’activer les composants de cette partition.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-104">When a default partition is assigned to a user, COM+ attempts to activate components in that partition first.</span></span> <span data-ttu-id="8c3f2-105">Si l’activation échoue, COM+ recherche le composant à activer dans la partition globale.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-105">If the activation fails, COM+ searches the global partition for the component to activate.</span></span> <span data-ttu-id="8c3f2-106">L’exception à ce processus se produit lorsque le composant COM+ comprend un moniker de partition qui spécifie explicitement la partition dans laquelle le composant se trouve.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-106">The exception to this process occurs when the COM+ component includes a partition moniker, which explicitly specifies the partition in which the component is located.</span></span> <span data-ttu-id="8c3f2-107">Dans ce cas, le moniker de la partition a la priorité sur toute configuration de partition par défaut.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-107">In this case, the partition moniker takes precedence over any default partition configuration.</span></span>

<span data-ttu-id="8c3f2-108">Lorsque vous utilisez des partitions locales, la partition par défaut est affectée aux utilisateurs à l’aide du dossier **com+ partition Users** dans l’outil d’administration Services de composants sur le serveur d’applications.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-108">When using local partitions, the default partition is assigned to users using the **COM+ Partition Users** folder in the Component Services administrative tool on the application server.</span></span> <span data-ttu-id="8c3f2-109">Lorsque vous utilisez des jeux de partitions dans le Active Directory, la partition par défaut de l’utilisateur est déterminée par le jeu de partitions de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8c3f2-109">When using partition sets in the Active Directory, the user's default partition is determined by the user's partition set.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c3f2-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c3f2-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c3f2-111">Partitions locales</span><span class="sxs-lookup"><span data-stu-id="8c3f2-111">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="8c3f2-112">Propriétés de partition</span><span class="sxs-lookup"><span data-stu-id="8c3f2-112">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="8c3f2-113">Partitions et Active Directory</span><span class="sxs-lookup"><span data-stu-id="8c3f2-113">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> <dt>

[<span data-ttu-id="8c3f2-114">Partition globale</span><span class="sxs-lookup"><span data-stu-id="8c3f2-114">The Global Partition</span></span>](the-global-partition.md)
</dt> </dl>

 

 



