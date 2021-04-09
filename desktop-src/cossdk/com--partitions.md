---
description: Vous pouvez utiliser le service partitions COM+ pour installer différentes versions d’une application COM+ sur un ordinateur et les exécuter simultanément.
ms.assetid: fd22a64c-f2d8-48af-86e1-985e21b0f8fa
title: Partitions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdd4e1efdd42ac407d8937c4090c59e65472ed69
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860861"
---
# <a name="com-partitions"></a><span data-ttu-id="9c31e-103">Partitions COM+</span><span class="sxs-lookup"><span data-stu-id="9c31e-103">COM+ Partitions</span></span>

<span data-ttu-id="9c31e-104">Vous pouvez utiliser le service partitions COM+ pour installer différentes versions d’une application COM+ sur un ordinateur et les exécuter simultanément.</span><span class="sxs-lookup"><span data-stu-id="9c31e-104">You can use the COM+ partitions service to install different versions of a COM+ application on a computer and run them simultaneously.</span></span>

<span data-ttu-id="9c31e-105">**Windows XP :** La possibilité de créer, de configurer ou de déléguer des partitions COM+ n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="9c31e-105">**Windows XP:** The ability to create, configure, or delegate COM+ partitions is not available.</span></span> <span data-ttu-id="9c31e-106">La partition globale est la seule partition COM+ disponible.</span><span class="sxs-lookup"><span data-stu-id="9c31e-106">The global partition is the only COM+ partition available.</span></span>

<span data-ttu-id="9c31e-107">\* \* Windows 2000 : \* \* le service partitions COM+ n’est pas disponible dans Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="9c31e-107">\*\*Windows 2000:  \*\* The COM+ partitions service is not available in Windows 2000.</span></span>

<span data-ttu-id="9c31e-108">Les rubriques suivantes fournissent des informations sur le service partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="9c31e-108">The following topics provide information about the COM+ partitions service.</span></span>



| <span data-ttu-id="9c31e-109">Rubrique</span><span class="sxs-lookup"><span data-stu-id="9c31e-109">Topic</span></span>                                                               | <span data-ttu-id="9c31e-110">Description</span><span class="sxs-lookup"><span data-stu-id="9c31e-110">Description</span></span>                                                                 |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="9c31e-111">Concepts des partitions COM+</span><span class="sxs-lookup"><span data-stu-id="9c31e-111">COM+ Partitions Concepts</span></span>](com--partitions-concepts.md)<br/> | <span data-ttu-id="9c31e-112">Fournit une vue d’ensemble de l’utilisation des partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="9c31e-112">Provides an overview of using COM+ partitions.</span></span><br/>                   |
| [<span data-ttu-id="9c31e-113">Tâches des partitions COM+</span><span class="sxs-lookup"><span data-stu-id="9c31e-113">COM+ Partitions Tasks</span></span>](com--partitions-tasks.md)<br/>       | <span data-ttu-id="9c31e-114">Fournit des instructions pour la création et la gestion des partitions COM+.</span><span class="sxs-lookup"><span data-stu-id="9c31e-114">Provides instructions for creating and managing COM+ partitions.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="9c31e-115">Le service partitions COM+ n’est pas activé par défaut.</span><span class="sxs-lookup"><span data-stu-id="9c31e-115">The COM+ partitions service is not enabled by default.</span></span> <span data-ttu-id="9c31e-116">Pour utiliser le service partitions COM+, vous devez l’activer par le biais de l’outil d’administration Services de composants ou en modifiant la propriété PartitionsEnabled de la collection [**LocalComputer**](localcomputer.md) sur true.</span><span class="sxs-lookup"><span data-stu-id="9c31e-116">To use the COM+ partitions service, you must enable it through the Component Services administration tool or by changing the PartitionsEnabled property on the [**LocalComputer**](localcomputer.md) collection to True.</span></span>

 

 

 




