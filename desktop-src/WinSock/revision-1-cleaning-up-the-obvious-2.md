---
description: Dans cette version de l’exemple de programme, quelques changements évidents ont été apportés, qui prendront des Strides initiaux pour améliorer les performances.
ms.assetid: ef9d594c-31fe-44c0-b707-47c01e2c5bf0
title: 'Révision 1 : nettoyage évident'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 631bea7395000531cce542b41ace3b3aab9afff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524594"
---
# <a name="revision-one-cleaning-up-the-obvious"></a><span data-ttu-id="b3a76-103">Révision 1 : nettoyage évident</span><span class="sxs-lookup"><span data-stu-id="b3a76-103">Revision One: Cleaning up the Obvious</span></span>

<span data-ttu-id="b3a76-104">Dans cette version de l’exemple de programme, quelques changements évidents ont été apportés, qui prendront des Strides initiaux pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="b3a76-104">In this version of the example program, a few obvious changes have been made that will take initial strides at improving performance.</span></span> <span data-ttu-id="b3a76-105">Cette version du code est loin de l’optimisation des performances, mais il s’agit d’une bonne étape incrémentielle qui permet d’examiner les effets de meilleures approches de manière incrémentielle.</span><span class="sxs-lookup"><span data-stu-id="b3a76-105">This version of the code is far from performance-tuned, but it is a good incremental step that enables examination of the effects of incrementally better approaches.</span></span>

> [!WARNING]
> <span data-ttu-id="b3a76-106">Cet exemple de l’application fournit intentionnellement des performances médiocres, afin d’illustrer les améliorations de performances possibles avec les modifications apportées au code.</span><span class="sxs-lookup"><span data-stu-id="b3a76-106">This example of the application provides intentionally poor performance, in order to illustrate performance improvements possible with changes to code.</span></span> <span data-ttu-id="b3a76-107">N’utilisez pas cet exemple de code dans votre application. elle est fournie à titre d’illustration uniquement.</span><span class="sxs-lookup"><span data-stu-id="b3a76-107">Do not use this code sample in your application; it is for illustration purposes only.</span></span>

 


```C++
#include <windows.h>

BYTE Set(row, col, bAlive)
{
    SOCKET s = socket(...);
    BYTE byRet = 0;
    BYTE tmp[3];
    tmp[0] = (BYTE)row;
    tmp[1] = (BYTE)col;
    tmp[2] = (BYTE)bAlive;
    bind( s, ... );
    connect( s, ... );
    send( s, &tmp, 3 );
    recv( s, &byRet, 1 );
    closesocket( s );
    return byRet;
}
```



## <a name="changes-in-this-version"></a><span data-ttu-id="b3a76-108">Modifications de cette version</span><span class="sxs-lookup"><span data-stu-id="b3a76-108">Changes in this Version</span></span>

<span data-ttu-id="b3a76-109">Cette version reflète les modifications suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3a76-109">This version reflects the following changes:</span></span>

-   <span data-ttu-id="b3a76-110">Suppression de SNDBUF = 0.</span><span class="sxs-lookup"><span data-stu-id="b3a76-110">Removed SNDBUF=0.</span></span> <span data-ttu-id="b3a76-111">Les retards de 200 millisecondes dus aux envois non mis en mémoire tampon et aux accusés de réception différés sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="b3a76-111">The 200 millisecond delays due to unbuffered sends and delayed acknowledgments are removed.</span></span>
-   <span data-ttu-id="b3a76-112">Suppression du comportement Send-Send-Receive.</span><span class="sxs-lookup"><span data-stu-id="b3a76-112">Removed the Send-Send-Receive behavior.</span></span> <span data-ttu-id="b3a76-113">Cette modification élimine les retards de 200 millisecondes dus à Nagle et aux interactions ACK retardées.</span><span class="sxs-lookup"><span data-stu-id="b3a76-113">This change eliminates 200-millisecond delays due to Nagle and delayed ACK interactions.</span></span>
-   <span data-ttu-id="b3a76-114">Suppression de l’hypothèse Little-endian supprimée.</span><span class="sxs-lookup"><span data-stu-id="b3a76-114">Removed little-endian assumption.</span></span> <span data-ttu-id="b3a76-115">Les octets sont maintenant dans l’ordre.</span><span class="sxs-lookup"><span data-stu-id="b3a76-115">The bytes are now in order.</span></span>

## <a name="remaining-problems"></a><span data-ttu-id="b3a76-116">Problèmes restants</span><span class="sxs-lookup"><span data-stu-id="b3a76-116">Remaining Problems</span></span>

<span data-ttu-id="b3a76-117">Dans cette version, les problèmes suivants sont conservés :</span><span class="sxs-lookup"><span data-stu-id="b3a76-117">In this version, the following problems remain:</span></span>

-   <span data-ttu-id="b3a76-118">L’application se connecte toujours lourd.</span><span class="sxs-lookup"><span data-stu-id="b3a76-118">The application is still connect heavy.</span></span> <span data-ttu-id="b3a76-119">Étant donné que les retards de 600 millisecondes sont supprimés, l’application atteint maintenant le taux soutenu de 12 connexions par seconde.</span><span class="sxs-lookup"><span data-stu-id="b3a76-119">Since the 600+ millisecond delays are removed, the application now hits the 12 connects-per-second sustained rate.</span></span> <span data-ttu-id="b3a76-120">De nombreuses connexions simultanées deviennent maintenant un problème.</span><span class="sxs-lookup"><span data-stu-id="b3a76-120">Many concurrent connections now becomes an issue.</span></span>
-   <span data-ttu-id="b3a76-121">L’application est toujours FAT ; les cellules inchangées sont toujours propagées vers le serveur.</span><span class="sxs-lookup"><span data-stu-id="b3a76-121">The application is still fat; unchanged cells are still propagated to the server.</span></span>
-   <span data-ttu-id="b3a76-122">L’application présente toujours une mauvaise diffusion. les envois de 3 octets sont toujours des émissions de petite taille.</span><span class="sxs-lookup"><span data-stu-id="b3a76-122">The application still exhibits poor streaming; 3-byte sends are still small sends.</span></span>
-   <span data-ttu-id="b3a76-123">L’application envoie à présent 2 octets/RTT, soit 4 Ko/s sur une connexion Ethernet directement connectée.</span><span class="sxs-lookup"><span data-stu-id="b3a76-123">The application now sends 2 bytes/RTT, which equals 4 KB/s on directly connected Ethernet.</span></span> <span data-ttu-id="b3a76-124">Cela n’est pas trop rapide, mais TIME-WAIT entraînera probablement d’abord des problèmes.</span><span class="sxs-lookup"><span data-stu-id="b3a76-124">This is not too fast, but TIME-WAIT will likely cause problems first.</span></span>
-   <span data-ttu-id="b3a76-125">La surcharge est inférieure à 99,3%, ce qui n’est toujours pas un bon pourcentage de charge.</span><span class="sxs-lookup"><span data-stu-id="b3a76-125">The overhead is down to 99.3%, which is still not a good overhead percentage.</span></span>

## <a name="key-performance-metrics"></a><span data-ttu-id="b3a76-126">Principales mesures de performance</span><span class="sxs-lookup"><span data-stu-id="b3a76-126">Key Performance Metrics</span></span>

<span data-ttu-id="b3a76-127">Les métriques de performances clés suivantes sont exprimées en temps de trajet aller-retour (RTT), Goodput et surcharge de protocole.</span><span class="sxs-lookup"><span data-stu-id="b3a76-127">The following key performance metrics are expressed in Round Trip Time (RTT), Goodput, and Protocol Overhead.</span></span> <span data-ttu-id="b3a76-128">Pour obtenir une explication de ces termes, consultez la rubrique [terminologie réseau](network-terminology-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b3a76-128">See the [Network Terminology](network-terminology-2.md) topic for an explanation of these terms.</span></span>

<span data-ttu-id="b3a76-129">Cette version reflète les mesures de performances suivantes :</span><span class="sxs-lookup"><span data-stu-id="b3a76-129">This version reflect the following performance metrics:</span></span>

-   <span data-ttu-id="b3a76-130">Heure de la cellule — 2 × RTT</span><span class="sxs-lookup"><span data-stu-id="b3a76-130">Cell Time—2×RTT</span></span>
-   <span data-ttu-id="b3a76-131">Goodput : 2 octets/RTT</span><span class="sxs-lookup"><span data-stu-id="b3a76-131">Goodput—2 bytes/RTT</span></span>
-   <span data-ttu-id="b3a76-132">Surcharge de protocole — 99.3 pour cent</span><span class="sxs-lookup"><span data-stu-id="b3a76-132">Protocol Overhead—99.3 percent</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3a76-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b3a76-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3a76-134">Amélioration d’une application lente</span><span class="sxs-lookup"><span data-stu-id="b3a76-134">Improving a Slow Application</span></span>](improving-a-slow-application-2.md)
</dt> <dt>

[<span data-ttu-id="b3a76-135">Terminologie du réseau</span><span class="sxs-lookup"><span data-stu-id="b3a76-135">Network Terminology</span></span>](network-terminology-2.md)
</dt> <dt>

[<span data-ttu-id="b3a76-136">Version de référence : une application très médiocre</span><span class="sxs-lookup"><span data-stu-id="b3a76-136">The Baseline Version: A Very Poor Performing Application</span></span>](the-baseline-version-a-very-poor-performing-application-2.md)
</dt> <dt>

[<span data-ttu-id="b3a76-137">Révision 2 : reconception pour des connexions moins nombreuses</span><span class="sxs-lookup"><span data-stu-id="b3a76-137">Revision 2: Redesigning for Fewer Connects</span></span>](revision-2-redesigning-for-fewer-connects-2.md)
</dt> <dt>

[<span data-ttu-id="b3a76-138">Révision 3 : envoi de bloc compressé</span><span class="sxs-lookup"><span data-stu-id="b3a76-138">Revision 3: Compressed Block Send</span></span>](revision-3-compressed-block-send-2.md)
</dt> <dt>

[<span data-ttu-id="b3a76-139">Améliorations futures</span><span class="sxs-lookup"><span data-stu-id="b3a76-139">Future Improvements</span></span>](future-improvements-2.md)
</dt> </dl>

 

 



