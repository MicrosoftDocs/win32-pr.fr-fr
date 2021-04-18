---
description: Dans cette version de l’application, un envoi de bloc compressé de données est utilisé. Cette modification entraîne une amélioration significative des performances.
ms.assetid: 3f0a129b-5b67-4334-a0aa-cd80ee7018b9
title: 'Révision trois : envoi de bloc compressé'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657579406ed31fce08239c518a6910f525219fdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520503"
---
# <a name="revision-three-compressed-block-send"></a><span data-ttu-id="a971d-104">Révision trois : envoi de bloc compressé</span><span class="sxs-lookup"><span data-stu-id="a971d-104">Revision Three: Compressed Block Send</span></span>

<span data-ttu-id="a971d-105">Dans cette version de l’application, un envoi de bloc compressé de données est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a971d-105">In this version of the application, a compressed block send of the data is used.</span></span> <span data-ttu-id="a971d-106">Cette modification entraîne une amélioration significative des performances.</span><span class="sxs-lookup"><span data-stu-id="a971d-106">This change results in significant performance improvement.</span></span>


```C++
BYTE tmp[3*ROWS*COLS];
FIELD Old = Map;
ComputeNext( Map );
n=Compact(Map,Old,tmp);
bind( s, ... );
connect( s, ... );
send( s, tmp, 3*n );
//can't do recv(s,tmp,n)
for(int i=0; i < n; )
    recv( s, tmp+i, n-i );
closesocket( s );
```



## <a name="changes-in-this-version"></a><span data-ttu-id="a971d-107">Modifications de cette version</span><span class="sxs-lookup"><span data-stu-id="a971d-107">Changes in this Version</span></span>

<span data-ttu-id="a971d-108">Cette version reflète les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="a971d-108">This version reflects the following changes:</span></span>

-   <span data-ttu-id="a971d-109">Les mises à jour de cellules ne sont plus sérialisées.</span><span class="sxs-lookup"><span data-stu-id="a971d-109">Cell updates are no longer serialized.</span></span>
-   <span data-ttu-id="a971d-110">Étant donné qu’un bloc Send est utilisé, l’application n’est plus bavarde.</span><span class="sxs-lookup"><span data-stu-id="a971d-110">Since a block send is used, the application is no longer chatty.</span></span>
-   <span data-ttu-id="a971d-111">La compression des données est utilisée, ce qui se traduit par une application moins FAT.</span><span class="sxs-lookup"><span data-stu-id="a971d-111">Data compression is used, resulting in a less fat application.</span></span>

<span data-ttu-id="a971d-112">Il y a toujours un problème avec cette version de l’application ; le risque d’interblocage existe, car une grande transmission est utilisée sans réception.</span><span class="sxs-lookup"><span data-stu-id="a971d-112">There is still an issue with this version of the application; the risk of deadlock exists since a large send is used with no receives.</span></span> <span data-ttu-id="a971d-113">Le serveur envoie un octet pour tous les 3 octets reçus.</span><span class="sxs-lookup"><span data-stu-id="a971d-113">The server sends one byte for every 3 bytes received.</span></span> <span data-ttu-id="a971d-114">Cela peut provoquer un blocage si la taille de la mémoire tampon de réception est inférieure à 1000 octets pour cet exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="a971d-114">This could cause a deadlock if the receive buffer size is less than 1000 bytes for this sample application.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="a971d-115">Principales mesures de performance</span><span class="sxs-lookup"><span data-stu-id="a971d-115">Key Performance Metrics</span></span>

<span data-ttu-id="a971d-116">Les mesures de performances suivantes sont exprimées en temps de boucle (RTT), Goodput et surcharge de protocole.</span><span class="sxs-lookup"><span data-stu-id="a971d-116">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="a971d-117">Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="a971d-117">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="a971d-118">Cette version reflète les mesures de performances suivantes :</span><span class="sxs-lookup"><span data-stu-id="a971d-118">This version reflects the following performance metrics:</span></span>

-   <span data-ttu-id="a971d-119">Heure de la cellule —. 002 \* RTT</span><span class="sxs-lookup"><span data-stu-id="a971d-119">Cell Time — .002\*RTT</span></span>
-   <span data-ttu-id="a971d-120">Goodput : 2 kilo-octets/RTT</span><span class="sxs-lookup"><span data-stu-id="a971d-120">Goodput — 2 Kilobytes/RTT</span></span>
-   <span data-ttu-id="a971d-121">Surcharge de protocole : 14%</span><span class="sxs-lookup"><span data-stu-id="a971d-121">Protocol Overhead — 14%</span></span>

<span data-ttu-id="a971d-122">De la surcharge de 14%, 6% provient des en-têtes Ethernet et les 8 autres% proviennent du démarrage et de la destruction de la connexion.</span><span class="sxs-lookup"><span data-stu-id="a971d-122">Of the 14% overhead, 6% is from the Ethernet headers and the other 8% is from the connection startup and teardown.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a971d-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a971d-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a971d-124">Amélioration d’une application lente</span><span class="sxs-lookup"><span data-stu-id="a971d-124">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="a971d-125">Terminologie du réseau</span><span class="sxs-lookup"><span data-stu-id="a971d-125">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="a971d-126">Version de référence : une application très médiocre</span><span class="sxs-lookup"><span data-stu-id="a971d-126">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="a971d-127">Révision 1 : nettoyage évident</span><span class="sxs-lookup"><span data-stu-id="a971d-127">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="a971d-128">Révision 2 : reconception pour des connexions moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="a971d-128">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="a971d-129">Améliorations futures</span><span class="sxs-lookup"><span data-stu-id="a971d-129">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



