---
description: Déploiement pour une communication plus rapide
ms.assetid: 9099f9df-b620-4623-826e-c541202ebc4a
title: Déploiement pour une communication plus rapide
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2594a7dbd34813013257350e2deb9d93db6bae5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516801"
---
# <a name="deploying-for-faster-communication"></a><span data-ttu-id="80541-103">Déploiement pour une communication plus rapide</span><span class="sxs-lookup"><span data-stu-id="80541-103">Deploying for Faster Communication</span></span>

<span data-ttu-id="80541-104">Les performances sont un élément clé à prendre en compte lors du déploiement d’une application COM+, et l’emplacement des composants est la clé pour obtenir les meilleures performances d’une application bien conçue.</span><span class="sxs-lookup"><span data-stu-id="80541-104">Performance is a key consideration when deploying a COM+ application, and component location is the key to getting the best performance from a well-designed application.</span></span>

<span data-ttu-id="80541-105">Une fois largement détenues, avec les architectures d’applications évolutives, les performances peuvent être résolues en déplaçant simplement les composants principaux de l’application sur du matériel plus rapide.</span><span class="sxs-lookup"><span data-stu-id="80541-105">It was once widely held that with scalable application architectures, performance could be addressed by simply moving primary components of the application to faster hardware.</span></span> <span data-ttu-id="80541-106">Cela a prouvé que cela ne soit pas vrai.</span><span class="sxs-lookup"><span data-stu-id="80541-106">This has proven not to be true.</span></span> <span data-ttu-id="80541-107">Les problèmes de performances ne proviennent pas des performances des composants individuels, mais des liens reliant les composants.</span><span class="sxs-lookup"><span data-stu-id="80541-107">Performance problems arise not from individual component performance but from the links connecting components.</span></span>

<span data-ttu-id="80541-108">Le principal facteur de réussite est l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="80541-108">The primary factor for success is location.</span></span> <span data-ttu-id="80541-109">La proximité ou l’emplacement physique, le temps, la capacité et l’objectif sont des aspects distincts de l’emplacement qui s’appliquent au déploiement d’une application COM+, qui ont tous une incidence sur les performances.</span><span class="sxs-lookup"><span data-stu-id="80541-109">Proximity or physical location, time, capacity, and purpose are distinct aspects of location that apply to the deployment of a COM+ application, all of which affect performance.</span></span>

<span data-ttu-id="80541-110">Les meilleures performances sont fournies lorsque les composants et les ressources de l’application sont conçus et déployés pour répondre aux demandes qui leur sont passées par la charge de travail de l’application.</span><span class="sxs-lookup"><span data-stu-id="80541-110">The best performance comes when the application components and resources are designed and deployed to match the demands placed upon them by the application workload.</span></span>

<span data-ttu-id="80541-111">En général, vous devez déployer des composants pour réduire la communication entre les composants entre les processus et, en particulier, entre les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="80541-111">In general, you should deploy components to minimize cross-process, and especially cross-computer, communication between components.</span></span> <span data-ttu-id="80541-112">Si la conception de votre application est efficace, les classes d’un composant sont regroupées à l’aide de et de la fonction pour optimiser les communications au sein des composants.</span><span class="sxs-lookup"><span data-stu-id="80541-112">If your application design is efficient, classes within a component are grouped by use and function to maximize communications within components.</span></span> <span data-ttu-id="80541-113">Lors du déploiement de composants, vous devez vous assurer que les composants sont logiquement localisés pour utiliser les relations entre les composants et pour réduire la quantité de messagerie entre les composants.</span><span class="sxs-lookup"><span data-stu-id="80541-113">In deploying components, you need to ensure that the components are logically located to make use of the relationships between the components and to reduce the amount of messaging between components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="80541-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80541-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80541-115">Conception pour le déploiement</span><span class="sxs-lookup"><span data-stu-id="80541-115">Designing for Deployment</span></span>](designing-for-deployment.md)
</dt> </dl>

 

 



