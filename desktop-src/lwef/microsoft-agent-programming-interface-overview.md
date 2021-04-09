---
title: Vue d’ensemble de l’interface de programmation Microsoft Agent
description: Vue d’ensemble de l’interface de programmation Microsoft Agent
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840098"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="54180-103">Vue d’ensemble de l’interface de programmation Microsoft Agent</span><span class="sxs-lookup"><span data-stu-id="54180-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="54180-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="54180-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="54180-105">L’API Microsoft Agent fournit des services qui prennent en charge l’affichage et l’animation de caractères animés.</span><span class="sxs-lookup"><span data-stu-id="54180-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="54180-106">Implémenté comme un serveur com OLE Automation (Component Object Model \[ \] ), Microsoft Agent permet à plusieurs applications, appelées clients ou applications clientes, d’héberger et d’accéder en même temps à ses services d’animation, d’entrée et de sortie.</span><span class="sxs-lookup"><span data-stu-id="54180-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="54180-107">Un client peut être n’importe quelle application qui se connecte aux interfaces COM de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="54180-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="54180-108">En tant que serveur COM, Microsoft Agent démarre automatiquement uniquement lorsqu’une application cliente utilise les interfaces COM et les demandes pour s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="54180-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="54180-109">Il reste en cours d’exécution jusqu’à ce que tous les clients ferment leurs connexions.</span><span class="sxs-lookup"><span data-stu-id="54180-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="54180-110">Quand aucun client connecté n’est conservé, Microsoft Agent se ferme automatiquement.</span><span class="sxs-lookup"><span data-stu-id="54180-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="54180-111">Bien que vous puissiez appeler les interfaces COM de Microsoft agent directement, Microsoft Agent comprend également un contrôle Microsoft ActiveX.</span><span class="sxs-lookup"><span data-stu-id="54180-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="54180-112">Ce contrôle facilite l’accès aux services de Microsoft Agent à partir de langages de programmation qui prennent en charge l’interface de contrôle ActiveX.</span><span class="sxs-lookup"><span data-stu-id="54180-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="54180-113">Outre la prise en charge des programmes autonomes écrits pour Windows, l’agent peut être écrit pour prendre en charge les pages Web, à condition que le navigateur prenne en charge l’interface ActiveX.</span><span class="sxs-lookup"><span data-stu-id="54180-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="54180-114">Microsoft Internet Explorer prend en charge ActiveX ainsi que les langages de script que vous pouvez utiliser pour programmer l’agent.</span><span class="sxs-lookup"><span data-stu-id="54180-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="54180-115">Si vous n’utilisez pas Internet Explorer, contactez votre fournisseur ou fournisseur à propos de la prise en charge d’ActiveX par le navigateur.</span><span class="sxs-lookup"><span data-stu-id="54180-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="54180-116">Les informations suivantes fournissent une brève vue d’ensemble des interfaces de programmation pour le logiciel Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="54180-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="54180-117">Services d’animation</span><span class="sxs-lookup"><span data-stu-id="54180-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="54180-118">Services d’entrée</span><span class="sxs-lookup"><span data-stu-id="54180-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="54180-119">Fenêtre commandes vocales</span><span class="sxs-lookup"><span data-stu-id="54180-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="54180-120">Services de sortie</span><span class="sxs-lookup"><span data-stu-id="54180-120">Output Services</span></span>](output-services.md)

 

 




