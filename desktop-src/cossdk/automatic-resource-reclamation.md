---
description: Récupération automatique des ressources
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Récupération automatique des ressources
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f76721df1a3858c9ad97d2f696115fff2eb6d3d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104317893"
---
# <a name="automatic-resource-reclamation"></a><span data-ttu-id="47a5b-103">Récupération automatique des ressources</span><span class="sxs-lookup"><span data-stu-id="47a5b-103">Automatic Resource Reclamation</span></span>

<span data-ttu-id="47a5b-104">COM+ notifie le gestionnaire de distribution à chaque expiration de la durée de vie d’un objet.</span><span class="sxs-lookup"><span data-stu-id="47a5b-104">COM+ notifies the dispenser manager each time an object's lifetime ends.</span></span> <span data-ttu-id="47a5b-105">Le gestionnaire de distribution avertit ensuite le détenteur de chaque distributeur de ressources inscrit pour voir s’il possède des ressources encore détenues par cet objet.</span><span class="sxs-lookup"><span data-stu-id="47a5b-105">The dispenser manager then notifies each registered resource dispenser's Holder to see whether it has any resources still held by this object.</span></span> <span data-ttu-id="47a5b-106">Si c’est le cas, ces ressources sont libérées, empêchant les fuites de ressources par les composants qui obtiennent des ressources via un distributeur de ressources.</span><span class="sxs-lookup"><span data-stu-id="47a5b-106">If so, those resources are freed, preventing the possibility of resource leaks by components that get resources through a resource dispenser.</span></span>

<span data-ttu-id="47a5b-107">La fonctionnalité de récupération automatique est une option qui est désactivée par défaut.</span><span class="sxs-lookup"><span data-stu-id="47a5b-107">The auto-reclamation feature is an option that is turned off by default.</span></span> <span data-ttu-id="47a5b-108">Un distributeur de ressources peut choisir d’activer cette option et, à cette fin, garantit qu’une référence à une ressource distribuée à un objet n’est jamais retournée par les méthodes d’objet.</span><span class="sxs-lookup"><span data-stu-id="47a5b-108">A resource dispenser can choose to enable this option and, in doing so, guarantees that a reference to any resource dispensed to an object is never returned by the object methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47a5b-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47a5b-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a5b-110">Concepts du distributeur de ressources COM+</span><span class="sxs-lookup"><span data-stu-id="47a5b-110">COM+ Resource Dispenser Concepts</span></span>](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



