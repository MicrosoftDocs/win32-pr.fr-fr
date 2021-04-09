---
description: Dans cette révision, l’exemple d’application est repensé pour éliminer les connexions inutiles.
ms.assetid: 0db6ded4-0a59-454e-824e-8cd7f0dc9fec
title: 'Révision deux : reconception pour des connexions moins nombreuses'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d5a8c8648f43f9ddac93c9d17f667b4b97011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114911"
---
# <a name="revision-two-redesigning-for-fewer-connects"></a><span data-ttu-id="5e01d-103">Révision deux : reconception pour des connexions moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="5e01d-103">Revision Two: Redesigning for Fewer Connects</span></span>

<span data-ttu-id="5e01d-104">Dans cette révision, l’exemple d’application est repensé pour éliminer les connexions inutiles.</span><span class="sxs-lookup"><span data-stu-id="5e01d-104">In this revision, the sample application is redesigned to eliminate unnecessary connects.</span></span>

> [!WARNING]
> <span data-ttu-id="5e01d-105">Cet exemple d’application fournit également des performances intentionnellement médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code.</span><span class="sxs-lookup"><span data-stu-id="5e01d-105">This examples of the application also provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="5e01d-106">N’utilisez pas cet exemple de code dans votre application. elle est fournie à titre d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="5e01d-106">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
ComputeNext( Map );
bind( s, ... );
connect( s, ... );
for(int i=0 ; i < ROWS ; ++i)
  for(int j=0 ; j < COLS ; ++j)
  {
    BYTE tmp[3];
    tmp[0] = i;
    tmp[1] = j;
    tmp[2] = Map[i][j];
    send( s, tmp, 3 );
    recv( s, &byRet, 1 );
  }
closesocket( s );
```



## <a name="remaining-problems"></a><span data-ttu-id="5e01d-107">Problèmes restants</span><span class="sxs-lookup"><span data-stu-id="5e01d-107">Remaining Problems</span></span>

<span data-ttu-id="5e01d-108">Les modifications apportées à la révision deux ont remanié l’application pour n’effectuer qu’une seule connexion par mise à jour.</span><span class="sxs-lookup"><span data-stu-id="5e01d-108">The changes in Revision Two redesigned the application to make only one connect per update.</span></span> <span data-ttu-id="5e01d-109">L’application comprend toujours les problèmes de performances suivants :</span><span class="sxs-lookup"><span data-stu-id="5e01d-109">The application still includes the following performance issues:</span></span>

-   <span data-ttu-id="5e01d-110">L’application est toujours sérialisée et bavarde.</span><span class="sxs-lookup"><span data-stu-id="5e01d-110">The application is still serialized and chatty.</span></span>
-   <span data-ttu-id="5e01d-111">L’application a toujours une conception FAT ; Il existe de nombreux envois qui ne nécessitent aucune opération dans cette conception.</span><span class="sxs-lookup"><span data-stu-id="5e01d-111">The application still has a fat design; there are many sends that require no operation in this design.</span></span>
-   <span data-ttu-id="5e01d-112">Les envois sont toujours uniquement de 3 octets, ce qui correspond à une mauvaise diffusion.</span><span class="sxs-lookup"><span data-stu-id="5e01d-112">The sends are still only 3 bytes, which is poor streaming.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="5e01d-113">Principales mesures de performance</span><span class="sxs-lookup"><span data-stu-id="5e01d-113">Key Performance Metrics</span></span>

<span data-ttu-id="5e01d-114">Les mesures de performances suivantes sont exprimées en temps de boucle (RTT), Goodput et surcharge de protocole.</span><span class="sxs-lookup"><span data-stu-id="5e01d-114">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="5e01d-115">Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="5e01d-115">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="5e01d-116">Cette version reflète les mesures de performances suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e01d-116">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="5e01d-117">Heure de la cellule — 1 \* RTT</span><span class="sxs-lookup"><span data-stu-id="5e01d-117">Cell Time — 1\*RTT</span></span>
-   <span data-ttu-id="5e01d-118">Goodput — 4 octets/RTT</span><span class="sxs-lookup"><span data-stu-id="5e01d-118">Goodput — 4 bytes/RTT</span></span>
-   <span data-ttu-id="5e01d-119">Surcharge de protocole : 96,8%</span><span class="sxs-lookup"><span data-stu-id="5e01d-119">Protocol Overhead — 96.8%</span></span>

## <a name="related-topics"></a><span data-ttu-id="5e01d-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5e01d-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e01d-121">Amélioration d’une application lente</span><span class="sxs-lookup"><span data-stu-id="5e01d-121">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="5e01d-122">Terminologie du réseau</span><span class="sxs-lookup"><span data-stu-id="5e01d-122">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="5e01d-123">Version de référence : une application très médiocre</span><span class="sxs-lookup"><span data-stu-id="5e01d-123">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="5e01d-124">Révision 1 : nettoyage évident</span><span class="sxs-lookup"><span data-stu-id="5e01d-124">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="5e01d-125">Révision 3 : envoi de bloc compressé</span><span class="sxs-lookup"><span data-stu-id="5e01d-125">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="5e01d-126">Améliorations futures</span><span class="sxs-lookup"><span data-stu-id="5e01d-126">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



