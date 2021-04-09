---
description: Le regroupement d’applications COM+ permet la mise à l’échelle des processus à thread unique, à l’instar de la façon dont le regroupement de threads permet la mise à l’échelle des objets à thread unique.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Concepts de regroupement d’applications COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87a72f5681896e8ac0e6a50b3bddfc16cf4303f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860874"
---
# <a name="com-application-pooling-concepts"></a><span data-ttu-id="a058b-103">Concepts de regroupement d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="a058b-103">COM+ Application Pooling Concepts</span></span>

<span data-ttu-id="a058b-104">Le regroupement d’applications COM+ permet la mise à l’échelle des processus à thread unique, à l’instar de la façon dont le regroupement de threads permet la mise à l’échelle des objets à thread unique.</span><span class="sxs-lookup"><span data-stu-id="a058b-104">COM+ application pooling allows single-threaded processes to scale, similar to the way that thread pooling allows single-threaded objects to scale.</span></span> <span data-ttu-id="a058b-105">Le regroupement d’applications peut également aider à récupérer suite à des défaillances dans des processus uniques en fournissant d’autres processus en cours d’exécution capables de gérer les activations.</span><span class="sxs-lookup"><span data-stu-id="a058b-105">Application pooling can also help recover from failures in single processes by providing other running processes able to handle activations.</span></span>

> [!Note]  
> <span data-ttu-id="a058b-106">Les applications de bibliothèque disposent des propriétés de recyclage et de regroupement de leur processus hôte.</span><span class="sxs-lookup"><span data-stu-id="a058b-106">Library applications have the recycling and pooling properties of their host process.</span></span>

 

<span data-ttu-id="a058b-107">Toutes les méthodes de l’interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) prennent en charge le regroupement d’applications.</span><span class="sxs-lookup"><span data-stu-id="a058b-107">All methods of the [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) interface support application pooling.</span></span>

<span data-ttu-id="a058b-108">Le regroupement d’applications COM+ est configurable par application à l’aide de la propriété ConcurrentApps de l’objet [**COMAdminCatalogObject**](comadmincatalogobject.md) dans la collection d' [**applications**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="a058b-108">COM+ application pooling is configurable per application by using the ConcurrentApps property of the [**COMAdminCatalogObject**](comadmincatalogobject.md) object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="a058b-109">ConcurrentApps est une valeur entière qui spécifie le nombre maximal de processus Dllhost simultanés qui doivent être démarrés pour traiter des activations pour une application.</span><span class="sxs-lookup"><span data-stu-id="a058b-109">ConcurrentApps is an integer value that specifies the maximum number of simultaneous Dllhost processes that should be started to service activations for an application.</span></span> <span data-ttu-id="a058b-110">Cette propriété peut être définie à l’aide de l’outil d’administration Services de composants ou par programme.</span><span class="sxs-lookup"><span data-stu-id="a058b-110">This property can be set by using the Component Services administration tool or programmatically.</span></span>

<span data-ttu-id="a058b-111">Si la propriété ConcurrentApps est définie sur 1, qui est la valeur par défaut, le service de mise en pool d’applications COM+ est désactivé.</span><span class="sxs-lookup"><span data-stu-id="a058b-111">If the ConcurrentApps property is set to 1, which is the default value, the COM+ Application Pooling service is disabled.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a058b-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a058b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a058b-113">Tâches de regroupement d’applications COM+</span><span class="sxs-lookup"><span data-stu-id="a058b-113">COM+ Application Pooling Tasks</span></span>](com--application-pooling-tasks.md)
</dt> <dt>

[<span data-ttu-id="a058b-114">Concepts de recyclage des applications COM+</span><span class="sxs-lookup"><span data-stu-id="a058b-114">COM+ Application Recycling Concepts</span></span>](com--application-recycling-concepts.md)
</dt> </dl>

 

 



