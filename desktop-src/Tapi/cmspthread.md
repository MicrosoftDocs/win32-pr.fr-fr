---
description: La classe CMSPThread implémente le thread de travail MSP.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520738"
---
# <a name="cmspthread"></a><span data-ttu-id="e17fd-103">CMSPThread</span><span class="sxs-lookup"><span data-stu-id="e17fd-103">CMSPThread</span></span>

<span data-ttu-id="e17fd-104">La classe **CMSPThread** implémente le thread de travail du MSP.</span><span class="sxs-lookup"><span data-stu-id="e17fd-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="e17fd-105">Les classes de base utilisent ce thread de travail à différentes fins.</span><span class="sxs-lookup"><span data-stu-id="e17fd-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="e17fd-106">Un mécanisme d’élément de travail générique et léger est fourni pour permettre au MSP dérivé d’utiliser ce thread pour ses propres éléments de travail synchrones ou asynchrones, quel que soit le cas.</span><span class="sxs-lookup"><span data-stu-id="e17fd-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="e17fd-107">Le thread pompe également les messages et prend en charge la gestion des APC (bien que les APC ne soient pas utilisés dans les classes de base).</span><span class="sxs-lookup"><span data-stu-id="e17fd-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="e17fd-108">Lorsque plusieurs adresses similaires sont présentes (autrement dit, lorsque la même implémentation MSP de la même DLL est instanciée plusieurs fois), la classe thread garantit l’évolutivité en utilisant automatiquement un thread unique pour toutes les adresses.</span><span class="sxs-lookup"><span data-stu-id="e17fd-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="e17fd-109">L’interface à la classe thread est telle que l’implémentation MSP peut considérer la classe thread comme un thread privé et n’a pas besoin de se soucier des autres adresses qui peuvent la partager.</span><span class="sxs-lookup"><span data-stu-id="e17fd-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="e17fd-110">Défini dans MSPthrd. h.</span><span class="sxs-lookup"><span data-stu-id="e17fd-110">Defined in MSPthrd.h.</span></span>

 

 



