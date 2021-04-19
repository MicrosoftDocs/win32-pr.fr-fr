---
description: Version de référence d’une application très médiocre dans Windows Sockets (Winsock).
ms.assetid: 923884c4-f1bd-4f72-983e-6158f368e0dd
title: 'Version de référence : une application très médiocre'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c094be5fd5cf6e3b9eaeb07c7ff38880e651dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518728"
---
# <a name="the-baseline-version-a-very-poor-performing-application"></a><span data-ttu-id="f8415-103">Version de référence : une application très médiocre</span><span class="sxs-lookup"><span data-stu-id="f8415-103">The Baseline Version: A Very Poor Performing Application</span></span>

<span data-ttu-id="f8415-104">L’exemple de code initial le plus médiocre utilisé pour calculer les mises à jour est le suivant :</span><span class="sxs-lookup"><span data-stu-id="f8415-104">The initial, poor performing code sample used to calculate the updates is as follows:</span></span>

> [!Note]  
> <span data-ttu-id="f8415-105">Par souci de simplicité, il n’y a pas de gestion des erreurs dans les exemples suivants.</span><span class="sxs-lookup"><span data-stu-id="f8415-105">For simplicity, there is no error handling in the following examples.</span></span> <span data-ttu-id="f8415-106">Toutes les applications de production vérifient toujours les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="f8415-106">Any production application always checks return values.</span></span>

 

> [!WARNING]
> <span data-ttu-id="f8415-107">Les premiers exemples de l’application offrent des performances intentionnellement médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code.</span><span class="sxs-lookup"><span data-stu-id="f8415-107">The first few examples of the application provide intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="f8415-108">N’utilisez pas ces exemples de code dans votre application. ils sont fournis à titre d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="f8415-108">Do not use these code samples in your application; they are for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BOOL Map[ROWS][COLS];

void LifeUpdate()
{
    ComputeNext( Map );
    for( int i = 0 ; i < ROWS ; ++i )     //serialized
        for( int j = 0 ; j < COLS ; ++j )
            Set( i, j, Map[i][j] );    //chatty
}

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    setsockopt( s, SO_SNDBUF, &Zero, sizeof(int) );
    bind( s, ... );
    connect( s, ... );
    send( s, &row, 1 );
    send( s, &col, 1 );
    send( s, &bAlive, 1 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



<span data-ttu-id="f8415-109">Dans cet État, l’application présente les pires performances réseau possibles.</span><span class="sxs-lookup"><span data-stu-id="f8415-109">In this state, the application has the worst possible network performance.</span></span> <span data-ttu-id="f8415-110">Les problèmes liés à cette version de l’exemple d’application sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="f8415-110">The problems with this version of the sample application include:</span></span>

-   <span data-ttu-id="f8415-111">L’application est bavarde.</span><span class="sxs-lookup"><span data-stu-id="f8415-111">The application is chatty.</span></span> <span data-ttu-id="f8415-112">Chaque transaction est trop petite : il n’est pas nécessaire de mettre à jour les cellules une par une.</span><span class="sxs-lookup"><span data-stu-id="f8415-112">Each transaction is too small — cells do not need to be updated one by one.</span></span>
-   <span data-ttu-id="f8415-113">Les transactions sont strictement sérialisées, même si les cellules peuvent être mises à jour simultanément.</span><span class="sxs-lookup"><span data-stu-id="f8415-113">The transactions are strictly serialized, even though the cells could be updated concurrently.</span></span>
-   <span data-ttu-id="f8415-114">La mémoire tampon d’envoi est définie sur zéro, et l’application entraîne un délai de 200 millisecondes pour chaque envoi, soit trois fois par cellule.</span><span class="sxs-lookup"><span data-stu-id="f8415-114">The send buffer is set to zero, and the application incurs a 200-millisecond delay for each send — three times per cell.</span></span>
-   <span data-ttu-id="f8415-115">L’application est très connectée et se connecte une seule fois pour chaque cellule.</span><span class="sxs-lookup"><span data-stu-id="f8415-115">The application is very connect heavy, connecting once for each cell.</span></span> <span data-ttu-id="f8415-116">Les applications sont limitées en nombre de connexions par seconde pour une destination donnée en raison de l’état d’attente, mais ce n’est pas un problème dans la mesure où chaque transaction prend plus de 600 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="f8415-116">Applications are limited in the number of connections per second for a given destination because of TIME-WAIT state, but that is not an issue here, since each transaction takes over 600 milliseconds.</span></span>
-   <span data-ttu-id="f8415-117">L’application est FAT ; de nombreuses transactions n’ont aucun effet sur l’état du serveur, car de nombreuses cellules ne changent pas de la mise à jour à la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="f8415-117">The application is fat; many transactions have no effect on the server state, because many cells do not change from update to update.</span></span>
-   <span data-ttu-id="f8415-118">L’application présente une mauvaise diffusion. les petits envois consomment beaucoup d’UC et de RAM.</span><span class="sxs-lookup"><span data-stu-id="f8415-118">The application exhibits poor streaming; small sends consume a lot of CPU and RAM.</span></span>
-   <span data-ttu-id="f8415-119">L’application suppose une représentation Little endian pour ses envois.</span><span class="sxs-lookup"><span data-stu-id="f8415-119">The application assumes little-endian representation for its sends.</span></span> <span data-ttu-id="f8415-120">Il s’agit d’une hypothèse naturelle pour la plate-forme Windows actuelle, mais elle peut être dangereuse pour le code à long terme.</span><span class="sxs-lookup"><span data-stu-id="f8415-120">This is a natural assumption for the current Windows platform, but can be dangerous for long-lived code.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="f8415-121">Principales mesures de performance</span><span class="sxs-lookup"><span data-stu-id="f8415-121">Key Performance Metrics</span></span>

<span data-ttu-id="f8415-122">Les mesures de performances suivantes sont exprimées en temps de boucle (RTT), Goodput et surcharge de protocole.</span><span class="sxs-lookup"><span data-stu-id="f8415-122">The following performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="f8415-123">Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="f8415-123">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

-   <span data-ttu-id="f8415-124">L’heure de la cellule, l’heure réseau pour une mise à jour de cellule unique, requiert 4 temps \* RTT + 600 millisecondes pour Nagle et les interactions ACK différées.</span><span class="sxs-lookup"><span data-stu-id="f8415-124">Cell time, network time for a single cell update, requires 4\*RTT + 600 milliseconds for Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="f8415-125">Goodput est inférieur à 6 octets.</span><span class="sxs-lookup"><span data-stu-id="f8415-125">Goodput is less than 6 bytes.</span></span>
-   <span data-ttu-id="f8415-126">La surcharge de protocole est de 99,6%.</span><span class="sxs-lookup"><span data-stu-id="f8415-126">Protocol Overhead is 99.6%.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8415-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f8415-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8415-128">Amélioration d’une application lente</span><span class="sxs-lookup"><span data-stu-id="f8415-128">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="f8415-129">Terminologie du réseau</span><span class="sxs-lookup"><span data-stu-id="f8415-129">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="f8415-130">Révision 1 : nettoyage évident</span><span class="sxs-lookup"><span data-stu-id="f8415-130">Revision 1: Cleaning up the Obvious</span></span>](revision-1-cleaning-up-the-obvious-2.md)
</dt> <dt>

[<span data-ttu-id="f8415-131">Révision 2 : reconception pour des connexions moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="f8415-131">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="f8415-132">Révision 3 : envoi de bloc compressé</span><span class="sxs-lookup"><span data-stu-id="f8415-132">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="f8415-133">Améliorations futures</span><span class="sxs-lookup"><span data-stu-id="f8415-133">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



