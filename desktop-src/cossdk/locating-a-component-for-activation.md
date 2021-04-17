---
description: Recherche d’un composant pour l’activation
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Recherche d’un composant pour l’activation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/05/2021
ms.locfileid: "104551801"
---
# <a name="locating-a-component-for-activation"></a><span data-ttu-id="ba1e4-103">Recherche d’un composant pour l’activation</span><span class="sxs-lookup"><span data-stu-id="ba1e4-103">Locating a Component for Activation</span></span>

<span data-ttu-id="ba1e4-104">Lorsque COM+ a localisé la partition correcte (par le biais de l’ensemble de partitions par défaut de l’identité de l’utilisateur, d’un moniker de partition ou de l’ID de partition dans le contexte de l’objet), COM + doit localiser le composant approprié dans cette partition.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-104">When COM+ has located the correct partition—through the user identity's default partition set, a partition moniker, or the partition ID in the object's context—COM+ must then locate the correct component within that partition.</span></span> <span data-ttu-id="ba1e4-105">L’illustration suivante montre comment un composant est trouvé et activé lorsque ce composant réside dans une partition.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-105">The following illustration shows how a component is found and activated when that component resides in a partition.</span></span>

> [!Note]  
> <span data-ttu-id="ba1e4-106">Avant toute activation de composant, COM+ effectue une validation pour vérifier que l’identité de l’utilisateur qui tente d’activer le composant dispose des droits d’accès à l’ensemble de partitions dans lequel le composant réside.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-106">Prior to any component activation, COM+ performs a validation to verify that the user identity attempting to activate the component has rights to access the partition set in which the component resides.</span></span>

 

![Diagramme qui montre une arborescence de résolution des problèmes pour localiser un composant en vue de son activation.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

<span data-ttu-id="ba1e4-108">L’illustration ci-dessus montre les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="ba1e4-108">The preceding illustration shows the following:</span></span>

-   <span data-ttu-id="ba1e4-109">Si le composant appelé réside dans une partition et qu’il se trouve dans la même application que le composant appelant, le composant est activé que le composant appelé soit marqué comme public ou privé.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-109">If the component being called resides in a partition and is in the same application as the calling component, the component is activated whether the component being called is marked as public or private.</span></span>
-   <span data-ttu-id="ba1e4-110">Si le composant appelé réside dans une partition mais n’existe pas dans la même application que le composant appelant, COM+ vérifie si le composant est marqué comme public.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-110">If the component being called resides in a partition but does not exist in the same application as the calling component, COM+ checks to see whether the component is marked as public.</span></span> <span data-ttu-id="ba1e4-111">Si aucune version publique n’est trouvée, COM+ recherche une version publique du composant dans la partition globale.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-111">If no public version is found, COM+ searches the Global Partition to find a public version of the component.</span></span> <span data-ttu-id="ba1e4-112">Si aucune version publique du composant n’est trouvée dans la partition globale ou si l’identité de l’utilisateur n’a pas de droits sur la partition, l’activation échoue.</span><span class="sxs-lookup"><span data-stu-id="ba1e4-112">If no public version of the component is found in the Global Partition or if the user identity has no rights to the partition, the activation fails.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ba1e4-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ba1e4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba1e4-114">Recherche de partitions pendant l’activation</span><span class="sxs-lookup"><span data-stu-id="ba1e4-114">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
</dt> </dl>

 

 



