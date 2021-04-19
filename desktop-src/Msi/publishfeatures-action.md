---
description: L’action PublishFeatures écrit l’état de chaque fonctionnalité dans le registre système.
ms.assetid: 8205e865-e625-43b9-8ce9-cff8026b2717
title: Action PublishFeatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5356ef89aa2651c470917a9b8d81b79ee83d01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544838"
---
# <a name="publishfeatures-action"></a><span data-ttu-id="90f1e-103">Action PublishFeatures</span><span class="sxs-lookup"><span data-stu-id="90f1e-103">PublishFeatures Action</span></span>

<span data-ttu-id="90f1e-104">L’action PublishFeatures écrit l’état de chaque fonctionnalité dans le registre système.</span><span class="sxs-lookup"><span data-stu-id="90f1e-104">The PublishFeatures action writes each feature's state into the system registry.</span></span> <span data-ttu-id="90f1e-105">L’état de la fonctionnalité peut être absent, publié ou installé.</span><span class="sxs-lookup"><span data-stu-id="90f1e-105">The feature state may be either absent, advertised, or installed.</span></span> <span data-ttu-id="90f1e-106">L’action PublishFeatures écrit également le mappage du composant de fonctionnalité dans le registre système pour chaque fonctionnalité installée.</span><span class="sxs-lookup"><span data-stu-id="90f1e-106">The PublishFeatures action also writes the feature-component mapping into the system registry for each installed feature.</span></span>

<span data-ttu-id="90f1e-107">L’action PublishFeatures interroge la table [FeatureComponents](featurecomponents-table.md), la table des [fonctionnalités](feature-table.md)et la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="90f1e-107">The PublishFeatures action queries the [FeatureComponents table](featurecomponents-table.md), [Feature table](feature-table.md), and [Component table](component-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="90f1e-108">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="90f1e-108">Sequence Restrictions</span></span>

<span data-ttu-id="90f1e-109">L’action PublishFeatures doit précéder [PublishProduct](publishproduct-action.md).</span><span class="sxs-lookup"><span data-stu-id="90f1e-109">The PublishFeatures action must come before [PublishProduct](publishproduct-action.md).</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="90f1e-110">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="90f1e-110">ActionData Messages</span></span>



| <span data-ttu-id="90f1e-111">Champ</span><span class="sxs-lookup"><span data-stu-id="90f1e-111">Field</span></span> | <span data-ttu-id="90f1e-112">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="90f1e-112">Description of action data</span></span>        |
|-------|-----------------------------------|
| <span data-ttu-id="90f1e-113">\[1\]</span><span class="sxs-lookup"><span data-stu-id="90f1e-113">\[1\]</span></span> | <span data-ttu-id="90f1e-114">Identificateur de la fonctionnalité publiée.</span><span class="sxs-lookup"><span data-stu-id="90f1e-114">Identifier of advertised feature.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="90f1e-115">Notes</span><span class="sxs-lookup"><span data-stu-id="90f1e-115">Remarks</span></span>

<span data-ttu-id="90f1e-116">L’action PublishFeatures publie la composition de toutes les fonctionnalités sélectionnées pour être publiées ou installées.</span><span class="sxs-lookup"><span data-stu-id="90f1e-116">The PublishFeatures action publishes the composition of all features that are selected to be advertised or installed.</span></span>

 

 



