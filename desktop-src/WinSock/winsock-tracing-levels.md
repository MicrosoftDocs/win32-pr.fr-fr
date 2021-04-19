---
description: 'En savoir plus sur : niveaux de suivi Winsock'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Niveaux de suivi Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531728"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="0b0f0-103">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="0b0f0-104">Niveaux de suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="0b0f0-105">Il existe deux niveaux de journalisation possibles dans le suivi Winsock :</span><span class="sxs-lookup"><span data-stu-id="0b0f0-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="0b0f0-106">Information</span><span class="sxs-lookup"><span data-stu-id="0b0f0-106">Information</span></span>
-   <span data-ttu-id="0b0f0-107">Commentaires</span><span class="sxs-lookup"><span data-stu-id="0b0f0-107">Verbose</span></span>

<span data-ttu-id="0b0f0-108">Le niveau d’information effectue le suivi des événements de création et de fermeture de socket, ainsi que toutes les erreurs qui se produisent sur le Socket.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="0b0f0-109">Le niveau détaillé inclut les événements de niveau informations et ajoute un suivi supplémentaire pour les événements d’envoi et de réception.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="0b0f0-110">La journalisation documentée est utilisée pour intercepter les problèmes d’endommagement de la mémoire tampon, ainsi que les applications mal écrites.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="0b0f0-111">Les informations ou le niveau de détail peuvent être utilisés avec le suivi d’événements réseau Winsock.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="0b0f0-112">Le suivi des modifications du catalogue Winsock ne prend en charge que le niveau d’information.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="0b0f0-113">Suivi des événements d’informations</span><span class="sxs-lookup"><span data-stu-id="0b0f0-113">Information Event Tracing</span></span>

<span data-ttu-id="0b0f0-114">La liste suivante détaille les opérations de socket d’événements réseau Winsock qui sont suivies au niveau des informations :</span><span class="sxs-lookup"><span data-stu-id="0b0f0-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="0b0f0-115">Création de socket</span><span class="sxs-lookup"><span data-stu-id="0b0f0-115">Socket creation</span></span>

    <span data-ttu-id="0b0f0-116">Un événement est enregistré dans une session de création de socket qui peut être utilisé pour suivre la durée de vie d’un Socket.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="0b0f0-117">Ces événements incluent également les sockets créés en acceptant des connexions sur un socket d’écoute.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="0b0f0-118">Lier</span><span class="sxs-lookup"><span data-stu-id="0b0f0-118">Bind</span></span>

    <span data-ttu-id="0b0f0-119">L’adresse IP locale est journalisée pour aider à mettre en corrélation les informations de suivi Winsock avec les appels de socket d’une application.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="0b0f0-120">Se connecter</span><span class="sxs-lookup"><span data-stu-id="0b0f0-120">Connect</span></span>

    <span data-ttu-id="0b0f0-121">L’adresse IP distante du socket connecté est journalisée pour aider à mettre en corrélation les informations de suivi Winsock avec les appels de socket d’une application.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="0b0f0-122">Abandons et annulations initiés par Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="0b0f0-123">À chaque fois que Winsock abandonne ou annule activement une demande, l’événement est consigné.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="0b0f0-124">Réinitialisations initiées par le transport</span><span class="sxs-lookup"><span data-stu-id="0b0f0-124">Transport initiated resets</span></span>

    <span data-ttu-id="0b0f0-125">Chaque fois que le transport sous-jacent indique qu’une connexion a été réinitialisée, l’événement est consigné.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="0b0f0-126">Erreurs d’envoi et de réception</span><span class="sxs-lookup"><span data-stu-id="0b0f0-126">Send and receive errors</span></span>

    <span data-ttu-id="0b0f0-127">Chaque fois qu’un appel d’envoi ou de réception vers le transport sous-jacent échoue, l’événement est consigné.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="0b0f0-128">Déconnexion et fermeture du socket</span><span class="sxs-lookup"><span data-stu-id="0b0f0-128">Socket disconnect and close</span></span>

    <span data-ttu-id="0b0f0-129">Un événement est consigné lorsqu’un handle de socket est fermé.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="0b0f0-130">Suivi des événements détaillés</span><span class="sxs-lookup"><span data-stu-id="0b0f0-130">Verbose Event Tracing</span></span>

<span data-ttu-id="0b0f0-131">Tous les événements d’information sont suivis au niveau détaillé.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="0b0f0-132">La liste suivante détaille les opérations de socket d’événements réseau Winsock supplémentaires qui sont suivies au niveau de détail :</span><span class="sxs-lookup"><span data-stu-id="0b0f0-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="0b0f0-133">Mémoires tampons d’envoi et de réception</span><span class="sxs-lookup"><span data-stu-id="0b0f0-133">Send and receive buffers</span></span>

    <span data-ttu-id="0b0f0-134">Les événements sont consignés dans les longueurs et les adresses de tampon d’utilisateur lorsque les appels d’envoi et de réception sont publiés dans Winsock, ainsi qu’à la fin de ces appels.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="0b0f0-135">Cela est utile pour diagnostiquer les problèmes de réutilisation de la mémoire tampon et pour une utilisation inefficace des mémoires tampons.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="0b0f0-136">Options de socket</span><span class="sxs-lookup"><span data-stu-id="0b0f0-136">Socket options</span></span>

    <span data-ttu-id="0b0f0-137">Un événement est consigné lorsqu’une application modifie certaines valeurs d’option de Socket.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="0b0f0-138">Certaines des options journalisées incluent SO \_ SNDBUF, donc \_ RCVBUF, SIO active la mise en \_ \_ \_ file d’attente circulaire et FIONBIO.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="0b0f0-139">WSAPoll et sélectionnez</span><span class="sxs-lookup"><span data-stu-id="0b0f0-139">WSAPoll and select</span></span>

    <span data-ttu-id="0b0f0-140">Un événement est consigné dans le journal de l’utilisation d’une application de [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) et des appels [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) qui peuvent être utilisés pour rechercher des goulots d’étranglement de performances.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="0b0f0-141">Abandons et annulations initiés par Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="0b0f0-142">À chaque fois que Winsock abandonne ou annule activement une demande, l’événement est consigné.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="0b0f0-143">Masque d’événement</span><span class="sxs-lookup"><span data-stu-id="0b0f0-143">Event mask</span></span>

    <span data-ttu-id="0b0f0-144">Un événement est consigné dans le journal du masque d’événement qu’une application inscrit pour l’utilisation de la fonction [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) .</span><span class="sxs-lookup"><span data-stu-id="0b0f0-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="0b0f0-145">Datagramme</span><span class="sxs-lookup"><span data-stu-id="0b0f0-145">Datagram</span></span>

    <span data-ttu-id="0b0f0-146">Un événement est consigné chaque fois qu’un datagramme arrive et qu’il n’y a pas d’espace de mémoire tampon dans lequel le copier.</span><span class="sxs-lookup"><span data-stu-id="0b0f0-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b0f0-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0b0f0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b0f0-148">Contrôle du suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="0b0f0-149">Suivi Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="0b0f0-150">Détails du suivi de modification du catalogue Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="0b0f0-151">Détails du suivi d’événements réseau Winsock</span><span class="sxs-lookup"><span data-stu-id="0b0f0-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
