---
title: Problèmes multithread
description: Problèmes multithread
ms.assetid: 17e74d2a-af4f-4188-89fa-b4f50abc424f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0910e1602d00d3429bb9e4c7a1667bf8113cd659
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380454"
---
# <a name="multi-threaded-issues"></a><span data-ttu-id="c9a29-103">Problèmes multithread</span><span class="sxs-lookup"><span data-stu-id="c9a29-103">Multi-Threaded Issues</span></span>

<span data-ttu-id="c9a29-104">OLE assure la prise en charge des applications multithread, ce qui permet aux applications d’effectuer des appels OLE à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="c9a29-104">OLE provides support for multithreaded applications, allowing applications to make OLE calls from multiple threads.</span></span> <span data-ttu-id="c9a29-105">Cette prise en charge multithread est appelée modèle cloisonné. il est important que tous les composants OLE qui utilisent plusieurs threads suivent ce modèle.</span><span class="sxs-lookup"><span data-stu-id="c9a29-105">This multithreaded support is called the apartment model, it is important that all OLE components using multiple threads follow this model.</span></span> <span data-ttu-id="c9a29-106">Le modèle cloisonné requiert que les pointeurs d’interface soient marshalés (à l’aide de [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface)et [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) lorsqu’ils sont transmis entre les threads.</span><span class="sxs-lookup"><span data-stu-id="c9a29-106">The apartment model requires that interface pointers are marshaled (using [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface), and [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface)) when passed between threads.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9a29-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c9a29-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9a29-108">Processus, threads et Apartments</span><span class="sxs-lookup"><span data-stu-id="c9a29-108">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> </dl>

 

 




