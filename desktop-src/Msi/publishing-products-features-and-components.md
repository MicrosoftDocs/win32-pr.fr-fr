---
description: Pour publier un produit, un composant ou une fonctionnalité, utilisez l’une des actions de publication.
ms.assetid: 2c395d81-4f46-444e-a275-7a5d806e473c
title: Publication de produits, de fonctionnalités et de composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cdd8c8445491646399c7d118a69ae497d27faff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202743"
---
# <a name="publishing-products-features-and-components"></a><span data-ttu-id="7c460-103">Publication de produits, de fonctionnalités et de composants</span><span class="sxs-lookup"><span data-stu-id="7c460-103">Publishing Products, Features, and Components</span></span>

<span data-ttu-id="7c460-104">Pour [publier](components-and-features.md) un produit, un composant ou une fonctionnalité, utilisez l’une des actions de publication.</span><span class="sxs-lookup"><span data-stu-id="7c460-104">To [publish](components-and-features.md) a product, component, or feature, use one of the publishing actions.</span></span> <span data-ttu-id="7c460-105">L' [action PublishProduct](publishproduct-action.md) enregistre les informations sur le produit auprès du système.</span><span class="sxs-lookup"><span data-stu-id="7c460-105">The [PublishProduct action](publishproduct-action.md) registers the product information with the system.</span></span> <span data-ttu-id="7c460-106">Après l’exécution de l’action PublishProduct, publiez les composants avec l' [action PublishComponents](publishcomponents-action.md), qui à son tour utilise la [table PublishComponent](publishcomponent-table.md) pour déterminer les composants définis comme étant publiés.</span><span class="sxs-lookup"><span data-stu-id="7c460-106">After executing the PublishProduct action, publish the components with the [PublishComponents action](publishcomponents-action.md), which in turn uses the [PublishComponent table](publishcomponent-table.md) to determine the components that are set as advertised.</span></span> <span data-ttu-id="7c460-107">Pour effectuer une publication par fonctionnalité, appelez l' [action PublishFeatures](publishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="7c460-107">To publish on a per-feature basis, invoke the [PublishFeatures action](publishfeatures-action.md).</span></span> <span data-ttu-id="7c460-108">Cette action utilise la [table FeatureComponents](featurecomponents-table.md) comme données pour résoudre les fonctionnalités publiées.</span><span class="sxs-lookup"><span data-stu-id="7c460-108">This action uses the [FeatureComponents table](featurecomponents-table.md) as data to resolve which features are advertised.</span></span>

<span data-ttu-id="7c460-109">Il existe également deux actions correspondantes qui annulent la publication d’une fonctionnalité ou d’un composant : l' [action UnpublishComponents](unpublishcomponents-action.md) et l' [action UnpublishFeatures](unpublishfeatures-action.md).</span><span class="sxs-lookup"><span data-stu-id="7c460-109">There are also two corresponding actions that unpublish a feature or a component: the [UnpublishComponents action](unpublishcomponents-action.md) and the [UnpublishFeatures action](unpublishfeatures-action.md).</span></span>

 

 



