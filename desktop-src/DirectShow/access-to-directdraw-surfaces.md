---
description: Accès aux surfaces DirectDraw
ms.assetid: 21002c9f-8b8b-49f3-9ea3-3703780e3412
title: Accès aux surfaces DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac1acdd122fa7d21fd49868c45f065f59b06ad8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846745"
---
# <a name="access-to-directdraw-surfaces"></a><span data-ttu-id="b9353-103">Accès aux surfaces DirectDraw</span><span class="sxs-lookup"><span data-stu-id="b9353-103">Access to DirectDraw Surfaces</span></span>

<span data-ttu-id="b9353-104">Les exemples d’objets multimédias fournis par VMR aux filtres en amont prennent en charge l’interface [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) .</span><span class="sxs-lookup"><span data-stu-id="b9353-104">The Media Sample objects provided by the VMR to upstream filters support the [**IVMRSurface**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurface) interface.</span></span> <span data-ttu-id="b9353-105">Pour obtenir l’interface, appelez QueryInterface sur l’interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) et spécifiez IID \_ IVMRSurface.</span><span class="sxs-lookup"><span data-stu-id="b9353-105">To obtain the interface, call QueryInterface on the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface and specify IID\_IVMRSurface.</span></span> <span data-ttu-id="b9353-106">Les filtres en amont peuvent ensuite utiliser les méthodes IVMRSurface pour accéder et manipuler la surface créée par VMR.</span><span class="sxs-lookup"><span data-stu-id="b9353-106">Upstream filters can then use the IVMRSurface methods to access and manipulate the surface that has been created by the VMR.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9353-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b9353-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9353-108">Utilisation de VMR pour les développeurs de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="b9353-108">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



