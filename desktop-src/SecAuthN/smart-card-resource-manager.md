---
description: Gestionnaire des ressources de carte à puce
ms.assetid: 96434996-88fa-47d3-bb44-3ebb23610b27
title: Gestionnaire des ressources de carte à puce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c3ee8e0bf311539863502d3e789544717e6dff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536555"
---
# <a name="smart-card-resource-manager"></a><span data-ttu-id="a4c61-103">Gestionnaire des ressources de carte à puce</span><span class="sxs-lookup"><span data-stu-id="a4c61-103">Smart Card Resource Manager</span></span>

<span data-ttu-id="a4c61-104">Le [*Gestionnaire de ressources*](../secgloss/r-gly.md) de [*carte à puce*](../secgloss/s-gly.md) gère l’accès aux [*lecteurs*](../secgloss/r-gly.md) et aux *cartes à puce*.</span><span class="sxs-lookup"><span data-stu-id="a4c61-104">The [*smart card*](../secgloss/s-gly.md) [*resource manager*](../secgloss/r-gly.md) manages access to [*readers*](../secgloss/r-gly.md) and to *smart cards*.</span></span> <span data-ttu-id="a4c61-105">Pour gérer ces ressources, il exécute les fonctions suivantes.</span><span class="sxs-lookup"><span data-stu-id="a4c61-105">To manage these resources, it performs the following functions.</span></span>

-   <span data-ttu-id="a4c61-106">Identifie et effectue le suivi des ressources.</span><span class="sxs-lookup"><span data-stu-id="a4c61-106">Identifies and tracks resources.</span></span>
-   <span data-ttu-id="a4c61-107">Alloue des lecteurs et des ressources sur plusieurs applications.</span><span class="sxs-lookup"><span data-stu-id="a4c61-107">Allocates readers and resources across multiple applications.</span></span>
-   <span data-ttu-id="a4c61-108">Prend en charge les primitives de [*transaction*](../secgloss/t-gly.md) pour accéder aux services disponibles sur une carte donnée.</span><span class="sxs-lookup"><span data-stu-id="a4c61-108">Supports [*transaction*](../secgloss/t-gly.md) primitives for accessing services available on a given card.</span></span>
    > [!Note]  
    > <span data-ttu-id="a4c61-109">Il s’agit d’un point important, car les cartes actuelles sont des appareils à thread unique qui nécessitent souvent l’exécution de plusieurs commandes pour effectuer une seule fonction.</span><span class="sxs-lookup"><span data-stu-id="a4c61-109">This is an important point because current cards are single-threaded devices that often require the execution of multiple commands to complete a single function.</span></span> <span data-ttu-id="a4c61-110">Les [*transactions*](../secgloss/t-gly.md) permettent l’exécution de plusieurs commandes sans interruption, garantissant ainsi que les informations d' [*État*](../secgloss/s-gly.md) intermédiaires ne sont pas endommagées.</span><span class="sxs-lookup"><span data-stu-id="a4c61-110">[*Transactions*](../secgloss/t-gly.md) allow multiple commands to be executed without interruption, ensuring that intermediate [*state*](../secgloss/s-gly.md) information is not corrupted.</span></span>

     

<span data-ttu-id="a4c61-111">Le gestionnaire de ressources est accessible directement par le biais de l’API Resource Manager ou indirectement par le biais de n’importe quel [*fournisseur de services*](../secgloss/s-gly.md)de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="a4c61-111">The resource manager can be accessed directly by way of the resource manager API or indirectly through any smart card [*service provider*](../secgloss/s-gly.md).</span></span>

<span data-ttu-id="a4c61-112">L’API Resource Manager est un ensemble de fonctions Windows qui fournissent un accès direct aux services de Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a4c61-112">The resource manager API is a set of Windows functions that provide direct access to the resource manager's services.</span></span> <span data-ttu-id="a4c61-113">Pour obtenir une vue d’ensemble des fonctions Windows fournies par l’API, consultez [api gestionnaire des ressources de carte à puce](smart-card-resource-manager-api.md).</span><span class="sxs-lookup"><span data-stu-id="a4c61-113">For an overview of the Windows functions provided by the API, see [Smart Card Resource Manager API](smart-card-resource-manager-api.md).</span></span> <span data-ttu-id="a4c61-114">En comparaison, les fournisseurs de services de carte à puce utilisent des interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="a4c61-114">In comparison, smart card service providers use COM interfaces.</span></span>

<span data-ttu-id="a4c61-115">La plupart des fonctions Windows de l’API Resource Manager ont des équivalents dans les propriétés et les méthodes des interfaces COM des fournisseurs de services de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="a4c61-115">Many of the Windows functions in the resource manager API have equivalents in the properties and methods of the smart card service providers' COM interfaces.</span></span> <span data-ttu-id="a4c61-116">Et même si la plupart des développeurs d’applications trouveront COM plus facile à utiliser, certaines applications devront toujours utiliser les fonctions Windows pour effectuer certaines tâches.</span><span class="sxs-lookup"><span data-stu-id="a4c61-116">And although most application developers will find COM easier to work with, some applications will still need to use the Windows functions to perform certain tasks.</span></span> <span data-ttu-id="a4c61-117">Par exemple, les applications qui doivent manipuler la liste des lecteurs ou des groupes de lecteurs dans la [*base de données des cartes à puce*](../secgloss/s-gly.md), et celles qui ont besoin d’un contrôle direct d’un lecteur, doivent utiliser l’API Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="a4c61-117">For example, applications that need to manipulate the list of readers or reader groups in the [*smart card database*](../secgloss/s-gly.md), and those that need direct control of a reader, must use the resource manager API.</span></span> <span data-ttu-id="a4c61-118">Les services qui offrent ces fonctionnalités sont disponibles uniquement dans les fonctions Windows, et non dans le COM fourni par les fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="a4c61-118">The services that provide these capabilities are available only in the Windows functions, not in the COM provided by the service providers.</span></span>

<span data-ttu-id="a4c61-119">Pour plus d’informations sur l’implémentation de [*Resource Manager*](../secgloss/r-gly.md) dans Windows, consultez [Gestionnaire des ressources Implementation](resource-manager-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="a4c61-119">For information about how the [*resource manager*](../secgloss/r-gly.md) is implemented in Windows, see [Resource Manager Implementation](resource-manager-implementation.md).</span></span>

 

 
