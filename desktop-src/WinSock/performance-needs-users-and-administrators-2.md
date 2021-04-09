---
description: Besoins en performances des utilisateurs et administrateurs avec les applications Windows Sockets (Winsock).
ms.assetid: 6c4365c6-a406-497b-a313-1faeb3e3b7f5
title: 'Besoins en matière de performances : utilisateurs et administrateurs'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a8178cf1d7516e9c16493916f8cf911752b9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033974"
---
# <a name="performance-needs-users-and-administrators"></a><span data-ttu-id="56542-103">Besoins en matière de performances : utilisateurs et administrateurs</span><span class="sxs-lookup"><span data-stu-id="56542-103">Performance Needs: Users and Administrators</span></span>

<span data-ttu-id="56542-104">Les utilisateurs jugent les performances des applications en fonction de leur expérience :</span><span class="sxs-lookup"><span data-stu-id="56542-104">Users judge application performance by their experience:</span></span>

-   <span data-ttu-id="56542-105">L’application est-elle rapide à répondre ?</span><span class="sxs-lookup"><span data-stu-id="56542-105">Is the application quick to respond?</span></span>
-   <span data-ttu-id="56542-106">Une icône de sablier s’affiche-t-elle pendant les opérations d’arrière-plan ?</span><span class="sxs-lookup"><span data-stu-id="56542-106">Is an hourglass icon displayed while background operations are carried out?</span></span>
-   <span data-ttu-id="56542-107">L’application démarre-t-elle et se ferme rapidement ?</span><span class="sxs-lookup"><span data-stu-id="56542-107">Does the application launch and close quickly?</span></span>
-   <span data-ttu-id="56542-108">Les erreurs sont-elles gérées de façon compréhensible ?</span><span class="sxs-lookup"><span data-stu-id="56542-108">Are errors handled in an understandable way?</span></span>

<span data-ttu-id="56542-109">Pour résumer, les utilisateurs veulent que les applications soient rapides et prévisibles.</span><span class="sxs-lookup"><span data-stu-id="56542-109">To summarize, users want applications to be fast and predictable.</span></span>

<span data-ttu-id="56542-110">En revanche, les administrateurs jugent souvent les performances d’une application sur la manière dont elle utilise les ressources réseau.</span><span class="sxs-lookup"><span data-stu-id="56542-110">In contrast, administrators often judge an application's performance on how efficiently it uses network resources.</span></span> <span data-ttu-id="56542-111">Les administrateurs peuvent poser les questions suivantes :</span><span class="sxs-lookup"><span data-stu-id="56542-111">Administrators may ask:</span></span>

-   <span data-ttu-id="56542-112">L’application a-t-elle une faible surcharge et une utilisation efficace du réseau ?</span><span class="sxs-lookup"><span data-stu-id="56542-112">Does the application have low overhead and efficient network usage?</span></span>
-   <span data-ttu-id="56542-113">Le nombre minimal de connexions est-il utilisé pour que mon serveur puisse traiter autant d’utilisateurs à la fois que possible ?</span><span class="sxs-lookup"><span data-stu-id="56542-113">Are the minimum number of connections used, so my server can service as many users at once as possible?</span></span>
-   <span data-ttu-id="56542-114">Suis-je constamment appelant le support technique ?</span><span class="sxs-lookup"><span data-stu-id="56542-114">Am I constantly calling helpdesk?</span></span>

<span data-ttu-id="56542-115">En bref, les administrateurs veulent que les applications soient mises à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="56542-115">In short, administrators want applications to scale.</span></span>

## <a name="best-practices-for-performance-needs"></a><span data-ttu-id="56542-116">Meilleures pratiques en matière de besoins en matière de performances</span><span class="sxs-lookup"><span data-stu-id="56542-116">Best Practices for Performance Needs</span></span>

<span data-ttu-id="56542-117">Lors du développement d’une application Windows Sockets, ces exigences en matière de performances traduisent en règles utiles.</span><span class="sxs-lookup"><span data-stu-id="56542-117">When developing a Windows Sockets application, these performance requirements translate into useful rules.</span></span>

-   <span data-ttu-id="56542-118">Les applications réseau s’initialisent rapidement.</span><span class="sxs-lookup"><span data-stu-id="56542-118">Have network applications initialize quickly.</span></span>

    <span data-ttu-id="56542-119">L’interface utilisateur ne doit pas avoir à attendre les réponses réseau.</span><span class="sxs-lookup"><span data-stu-id="56542-119">The user interface should not have to wait for network responses.</span></span> <span data-ttu-id="56542-120">Certaines tâches peuvent être effectuées avant que le réseau soit disponible ou sans réseau.</span><span class="sxs-lookup"><span data-stu-id="56542-120">Some tasks can be performed before the network is available, or without the network.</span></span> <span data-ttu-id="56542-121">Si le réseau ne répond pas, l’utilisateur peut avoir besoin de l’interface utilisateur pour des opérations simples, telles que la fermeture de l’application.</span><span class="sxs-lookup"><span data-stu-id="56542-121">If the network is not responding, the user may need the user interface for simple operations, such as closing the application.</span></span>

-   <span data-ttu-id="56542-122">N’attendez pas que le réseau soit arrêté.</span><span class="sxs-lookup"><span data-stu-id="56542-122">Do not wait for the network for shutdown.</span></span>

    <span data-ttu-id="56542-123">Les applications client-serveur écrites correctement gèrent les déconnexions abandonnées de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="56542-123">Properly written client-server applications handle abortive disconnects gracefully.</span></span> <span data-ttu-id="56542-124">N’initialisez pas une opération potentiellement longue, telle que la synchronisation de fichiers ou de dossiers avec un serveur, qui ne peut pas être interrompue lors de l’arrêt.</span><span class="sxs-lookup"><span data-stu-id="56542-124">Do not initiate a potentially lengthy operation, such as synchronizing files or folders with a server, that cannot be interrupted on shutdown.</span></span> <span data-ttu-id="56542-125">Les réseaux ne sont pas constamment réactifs, de sorte que même les petites opérations peuvent prendre du temps.</span><span class="sxs-lookup"><span data-stu-id="56542-125">Networks are not consistently responsive, so even small operations could prove time consuming.</span></span> <span data-ttu-id="56542-126">Fournir des commentaires positifs aux utilisateurs, y compris des indications de progression et des temps d’achèvement estimés.</span><span class="sxs-lookup"><span data-stu-id="56542-126">Provide positive feedback for users, including indications of progress and estimated completion times.</span></span>

-   <span data-ttu-id="56542-127">Garantir une interface utilisateur réactive.</span><span class="sxs-lookup"><span data-stu-id="56542-127">Ensure a responsive user interface.</span></span>

    <span data-ttu-id="56542-128">La réactivité des applications permet d’éliminer les appels au support technique inutiles.</span><span class="sxs-lookup"><span data-stu-id="56542-128">Application responsiveness helps eliminate unnecessary helpdesk calls.</span></span> <span data-ttu-id="56542-129">Une bonne indication pour une réponse interactive est de 500 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="56542-129">A good guideline for interactive response is 500 milliseconds.</span></span> <span data-ttu-id="56542-130">Les utilisateurs perçoivent des pauses de plus de 500 millisecondes comme un décalage des performances.</span><span class="sxs-lookup"><span data-stu-id="56542-130">Users perceive pauses longer than 500 milliseconds as a lag in performance.</span></span> <span data-ttu-id="56542-131">Les applications doivent être suffisamment réactives pour fournir l’utilisateur en toute confiance à l’application.</span><span class="sxs-lookup"><span data-stu-id="56542-131">Applications should be responsive enough to provide the user with confidence about the application.</span></span>

-   <span data-ttu-id="56542-132">Examinez les erreurs réseau.</span><span class="sxs-lookup"><span data-stu-id="56542-132">Scrutinize network errors.</span></span>

    <span data-ttu-id="56542-133">Toutes les erreurs réseau ne sont pas critiques.</span><span class="sxs-lookup"><span data-stu-id="56542-133">Not all network errors are critical.</span></span> <span data-ttu-id="56542-134">Par exemple, une application qui a reçu ou publié toutes ses données peut ignorer des erreurs lors de la fermeture de la connexion.</span><span class="sxs-lookup"><span data-stu-id="56542-134">For example, an application that has received or posted all of its data can likely ignore errors when closing the connection.</span></span> <span data-ttu-id="56542-135">Ne supposez pas que le réseau ou l’utilisateur est disponible. Gérez les erreurs sans intervention de l’utilisateur ou ignorez-les si les erreurs ne sont pas critiques.</span><span class="sxs-lookup"><span data-stu-id="56542-135">Do not assume the network or the user is available; either handle errors without user intervention, or ignore them if errors are noncritical.</span></span>

-   <span data-ttu-id="56542-136">Une application doit définir ses propres délais d’expiration raisonnables.</span><span class="sxs-lookup"><span data-stu-id="56542-136">An application should define its own reasonable time outs.</span></span>

    <span data-ttu-id="56542-137">Par exemple, une demande Windows Sockets Connect () peut être bloquée dans certaines conditions jusqu’à 21 secondes.</span><span class="sxs-lookup"><span data-stu-id="56542-137">For example, a Windows Sockets connect() request may block under some conditions for as much as 21 seconds.</span></span> <span data-ttu-id="56542-138">Les applications peuvent avoir besoin d’introduire leur propre délai d’expiration en fonction de leurs utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="56542-138">Applications may need to introduce their own time outs as appropriate for their users.</span></span>

-   <span data-ttu-id="56542-139">Réduire la charge de protocole.</span><span class="sxs-lookup"><span data-stu-id="56542-139">Minimize protocol overhead.</span></span>

    <span data-ttu-id="56542-140">La préservation de la bande passante réseau est partiellement liée à la réduction de la charge de protocole générée par votre application.</span><span class="sxs-lookup"><span data-stu-id="56542-140">Conserving network bandwidth is partially about minimizing the protocol overhead incurred by your application.</span></span> <span data-ttu-id="56542-141">Il s’agit également d’éliminer le trafic réseau inutile.</span><span class="sxs-lookup"><span data-stu-id="56542-141">It is also about eliminating unnecessary network traffic.</span></span> <span data-ttu-id="56542-142">Les protocoles avec une surcharge d’en-tête inférieure peuvent être utilisés pour transférer des données d’application.</span><span class="sxs-lookup"><span data-stu-id="56542-142">Protocols with a lower header overhead can be used to transfer application data.</span></span> <span data-ttu-id="56542-143">Par exemple, lors de l’envoi de petites quantités de données non critiques ou reproductibles, utilisez UDP au lieu de TCP pour réduire la surcharge associée à l’établissement et à la maintenance de la connexion.</span><span class="sxs-lookup"><span data-stu-id="56542-143">For example, when sending smaller amounts of noncritical or repeatable data, use UDP as opposed to TCP to reduce the overhead associated with connection establishment and maintenance.</span></span> <span data-ttu-id="56542-144">Si les mêmes données doivent être envoyées à plusieurs destinataires, envisagez la multidiffusion.</span><span class="sxs-lookup"><span data-stu-id="56542-144">If the same data must be sent to multiple recipients, consider multicast.</span></span> <span data-ttu-id="56542-145">Sachez que les applications UDP ne sont pas contrôlées par le biais de la bande passante, ce qui peut entraîner une défaillance catastrophique du réseau.</span><span class="sxs-lookup"><span data-stu-id="56542-145">Be aware that UDP applications are not flow-controlled—pushing beyond the available bandwidth can cause catastrophic network failure.</span></span> <span data-ttu-id="56542-146">L’utilitaire Netstat peut être utilisé avec ses options **-e** et **-s** pour afficher les statistiques de différents protocoles.</span><span class="sxs-lookup"><span data-stu-id="56542-146">The Netstat utility can be used with its **-e** and **-s** options to display statistics for various protocols.</span></span>

-   <span data-ttu-id="56542-147">Conserver les ressources système.</span><span class="sxs-lookup"><span data-stu-id="56542-147">Conserve system resources.</span></span>

    <span data-ttu-id="56542-148">Les ressources système peuvent être utilisées rapidement si une contrainte appropriée n’est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="56542-148">System resources can be consumed quickly if proper restraint is not used.</span></span> <span data-ttu-id="56542-149">Par exemple, les sockets et les connexions TCP consomment des ressources.</span><span class="sxs-lookup"><span data-stu-id="56542-149">For example, sockets and TCP connections consume resources.</span></span> <span data-ttu-id="56542-150">N’utilisez pas plusieurs connexions TCP par client où l’une d’elles servira à l’application.</span><span class="sxs-lookup"><span data-stu-id="56542-150">Do not use several TCP connections per client where one will serve the application's purpose.</span></span>

<span data-ttu-id="56542-151">Pour les applications transactionnelles, une expérience utilisateur correcte et une faible utilisation du réseau ne sont pas des objectifs conflictuels.</span><span class="sxs-lookup"><span data-stu-id="56542-151">For transactional applications, good user experience and low network utilization are not conflicting goals.</span></span> <span data-ttu-id="56542-152">Le réseau est un goulot d’étranglement.</span><span class="sxs-lookup"><span data-stu-id="56542-152">The network is a bottleneck.</span></span> <span data-ttu-id="56542-153">Les applications nécessitant beaucoup de ressources réseau consacrent plus de temps à attendre, et les applications réseau bien écrites sont conçues pour réduire le temps d’attente inutile, à la fois pour l’interface utilisateur et pour la transmission réseau.</span><span class="sxs-lookup"><span data-stu-id="56542-153">Network-intensive applications spend more time waiting, and well written network applications are designed to minimize unnecessary wait time, both for the user interface and for network transmissions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56542-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="56542-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56542-155">Applications Windows Sockets hautes performances</span><span class="sxs-lookup"><span data-stu-id="56542-155">High-performance Windows Sockets Applications</span></span>](high-performance-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="56542-156">Dimensions de performances</span><span class="sxs-lookup"><span data-stu-id="56542-156">Performance Dimensions</span></span>](performance-dimensions-2.md)
</dt> </dl>

 

 



