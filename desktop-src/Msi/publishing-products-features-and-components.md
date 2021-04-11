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
# <a name="publishing-products-features-and-components"></a>Publication de produits, de fonctionnalités et de composants

Pour [publier](components-and-features.md) un produit, un composant ou une fonctionnalité, utilisez l’une des actions de publication. L' [action PublishProduct](publishproduct-action.md) enregistre les informations sur le produit auprès du système. Après l’exécution de l’action PublishProduct, publiez les composants avec l' [action PublishComponents](publishcomponents-action.md), qui à son tour utilise la [table PublishComponent](publishcomponent-table.md) pour déterminer les composants définis comme étant publiés. Pour effectuer une publication par fonctionnalité, appelez l' [action PublishFeatures](publishfeatures-action.md). Cette action utilise la [table FeatureComponents](featurecomponents-table.md) comme données pour résoudre les fonctionnalités publiées.

Il existe également deux actions correspondantes qui annulent la publication d’une fonctionnalité ou d’un composant : l' [action UnpublishComponents](unpublishcomponents-action.md) et l' [action UnpublishFeatures](unpublishfeatures-action.md).

 

 



