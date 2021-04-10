---
description: Ce guide fournit les informations dont vous avez besoin pour permettre à votre application Microsoft Windows d’utiliser la nouvelle génération de protocole Internet version 6 (IPv6).
ms.assetid: 8e862eb0-2ba9-40b0-ac73-fcb0e625965e
title: Guide IPv6 pour les applications Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3c582ba8dc10c167d47aafe98b1e8742551f948
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113054"
---
# <a name="ipv6-guide-for-windows-sockets-applications"></a><span data-ttu-id="68ba1-103">Guide IPv6 pour les applications Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="68ba1-103">IPv6 Guide for Windows Sockets Applications</span></span>

<span data-ttu-id="68ba1-104">Ce guide fournit les informations dont vous avez besoin pour permettre à votre application Microsoft Windows d’utiliser la nouvelle génération de protocole Internet version 6 (IPv6).</span><span class="sxs-lookup"><span data-stu-id="68ba1-104">This guide provides the information you need to enable your Microsoft Windows application to use the next generation of Internet Protocol, version 6 (IPv6).</span></span> <span data-ttu-id="68ba1-105">L’ajout de la fonctionnalité IPv6 à votre application n’est pas nécessairement un processus de Portage.</span><span class="sxs-lookup"><span data-stu-id="68ba1-105">Adding IPv6 capability to your application is not necessarily a porting process.</span></span> <span data-ttu-id="68ba1-106">Le portage d’une application suggère de modifier le code pour fonctionner sur une plateforme différente, ce qui implique de laisser la plateforme précédente en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="68ba1-106">To port an application suggests modifying code to work on a different platform, which implies leaving the previous platform behind.</span></span> <span data-ttu-id="68ba1-107">Ce guide est spécifiquement structuré pour aider à ajouter des fonctionnalités IPv6 à une application tout en conservant la fonctionnalité IPv4.</span><span class="sxs-lookup"><span data-stu-id="68ba1-107">This guide is specifically structured to help add IPv6 capability to an application while retaining IPv4 functionality.</span></span>

<span data-ttu-id="68ba1-108">Ce guide décrit les problèmes liés à l’ajout de fonctionnalités IPv6, puis cible les zones de développement les plus affectées par la transition.</span><span class="sxs-lookup"><span data-stu-id="68ba1-108">This guide discusses the issues associated with adding IPv6 functionality, then targets the areas of development most affected by the transition.</span></span> <span data-ttu-id="68ba1-109">Chaque zone reçoit une explication complète des pièges à surveiller, des stratégies suggérées pour les éviter et des conseils sur la façon de tirer le meilleur parti des nouveaux éléments de programmation de [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) (fonctions et structures).</span><span class="sxs-lookup"><span data-stu-id="68ba1-109">Each area receives a thorough explanation of the pitfalls to watch out for, the strategies suggested to avoid them, and tips on how to make the best use of new [Windows Sockets 2](what-s-new-for-windows-sockets-2.md) programmatic elements (functions and structures).</span></span> <span data-ttu-id="68ba1-110">Pour plus d’informations sur IPv6, consultez [prise en charge d’IPv6](ipv6-support-2.md).</span><span class="sxs-lookup"><span data-stu-id="68ba1-110">For additional information on IPv6, see [IPv6 Support](ipv6-support-2.md).</span></span>

<span data-ttu-id="68ba1-111">Ce guide fournit également des exemples de code pour vous offrir une expérience pratique et des représentations visuelles des problèmes que vous pouvez rencontrer lors de la modification de vos applications.</span><span class="sxs-lookup"><span data-stu-id="68ba1-111">This guide also provides code examples to give you hands-on experience and visual representations of the issues you could encounter when modifying your applications.</span></span> <span data-ttu-id="68ba1-112">Les exemples proviennent d’exemples complets et fonctionnels d’une application Windows Sockets simple qui a été modifiée pour prendre en charge à la fois IPv4 et IPv6.</span><span class="sxs-lookup"><span data-stu-id="68ba1-112">The examples come from complete, working examples of a simple Windows Sockets application that has been modified to support both IPv4 and IPv6.</span></span> <span data-ttu-id="68ba1-113">Le code source de ces exemples fonctionnels est inclus dans son intégralité dans deux annexes à la fin de ce document : [annexe A : le code source IPv4 uniquement](appendix-a-ipv4-only-source-code-2.md) inclut le code source d’une application avant sa modification pour prendre en charge IPv6 ; [Annexe B : le code source agnostique de la version IP](appendix-b-ip-version-agnostic-source-code-2.md) fournit le code source une fois que l’application a été activée pour IPv6.</span><span class="sxs-lookup"><span data-stu-id="68ba1-113">Source code for these working examples is included in its entirety in two appendixes at the end of this document: [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) includes the source code for an application before it is modified to support IPv6; [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md) provides the source code after the application has been IPv6-enabled.</span></span>

<span data-ttu-id="68ba1-114">Microsoft propose un utilitaire appelé Checkv4.exe qui vous aide à trouver du code potentiellement sensible au portage dans le code de votre application et fournit également des recommandations pour les correctifs.</span><span class="sxs-lookup"><span data-stu-id="68ba1-114">Microsoft provides a utility called Checkv4.exe that helps you find potentially porting-sensitive code in your application code, and also makes recommendations for fixes.</span></span> <span data-ttu-id="68ba1-115">L’utilitaire Checkv4.exe est illustré dans ce document, à l’aide de l’exemple d’application inclus dans les annexes, avec des captures d’écran présentant la sortie générée par l’utilitaire Checkv4.exe.</span><span class="sxs-lookup"><span data-stu-id="68ba1-115">The Checkv4.exe utility is demonstrated in this document, using the sample application included in the appendixes, along with screen shots displaying the output that the Checkv4.exe utility produces.</span></span> <span data-ttu-id="68ba1-116">Pour plus d’informations, consultez [utilisation de l’utilitaire de Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="68ba1-116">For more information, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>

<span data-ttu-id="68ba1-117">Les domaines de programmation traités par ce guide sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="68ba1-117">The programming areas addressed by this guide are:</span></span>

-   [<span data-ttu-id="68ba1-118">Modification des structures de données pour IPv6 Winsock appications</span><span class="sxs-lookup"><span data-stu-id="68ba1-118">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
-   [<span data-ttu-id="68ba1-119">Appels de fonction pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="68ba1-119">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
-   [<span data-ttu-id="68ba1-120">Utilisation d’adresses IPv4 codées en dur</span><span class="sxs-lookup"><span data-stu-id="68ba1-120">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
-   [<span data-ttu-id="68ba1-121">Problèmes d’interface utilisateur pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="68ba1-121">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
-   [<span data-ttu-id="68ba1-122">Protocoles sous-jacents pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="68ba1-122">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
-   [<span data-ttu-id="68ba1-123">Sockets à double pile pour les applications Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="68ba1-123">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)

<span data-ttu-id="68ba1-124">Étant donné qu’il n’existe pas de séquence d’événements uniforme, les sections qui traitent des problèmes d’activation D’ipv6 ne sont pas organisées de façon séquentielle, de sorte que vous pouvez référencer n’importe quelle section à tout moment.</span><span class="sxs-lookup"><span data-stu-id="68ba1-124">Because there is no uniform sequence of events, the sections that address IPv6-enabling issues are not arranged in a sequentially significant manner, so you can reference any section at any time.</span></span> <span data-ttu-id="68ba1-125">Il est fortement recommandé d’examiner chaque section tout en ajoutant des fonctionnalités IPv6 à votre application.</span><span class="sxs-lookup"><span data-stu-id="68ba1-125">It is strongly recommended that you review each section while adding IPv6 capability to your application.</span></span> <span data-ttu-id="68ba1-126">Il est également recommandé de lire l’utilitaire Checkv4.exe, car il contient des conseils sur l’ordre dans lequel résoudre les problèmes d’activation d’IPv6.</span><span class="sxs-lookup"><span data-stu-id="68ba1-126">It is also advisable to read about the Checkv4.exe utility, as it includes tips on the order in which to address IPv6-enabling issues.</span></span>

<span data-ttu-id="68ba1-127">Pour examiner l’utilitaire de Checkv4.exe et pour examiner l’ordre dans lequel vous devez aborder le processus de Portage dans vos applications, consultez [utilisation de l’utilitaire de Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="68ba1-127">To look at the Checkv4.exe utility, and to review the order in which you should approach the porting process in your applications, see [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span> <span data-ttu-id="68ba1-128">Cette section contient des informations sur un indicateur de compilation qui vérifie rigoureusement les éléments de programmation incompatibles avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="68ba1-128">This section includes information on a compile-time flag that strictly checks for programming elements incompatible with IPv6.</span></span>

<span data-ttu-id="68ba1-129">Pour accéder directement à l’exemple d’application, consultez [annexe A : code source IPv4 uniquement](appendix-a-ipv4-only-source-code-2.md) et [annexe B : code source agnostique de la version IP](appendix-b-ip-version-agnostic-source-code-2.md).</span><span class="sxs-lookup"><span data-stu-id="68ba1-129">To go straight to the sample application, see [Appendix A: IPv4-only Source Code](appendix-a-ipv4-only-source-code-2.md) and [Appendix B: IP-version Agnostic Source Code](appendix-b-ip-version-agnostic-source-code-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="68ba1-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="68ba1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="68ba1-131">Protocole Internet version 6 (IPv6)</span><span class="sxs-lookup"><span data-stu-id="68ba1-131">Internet Protocol Version 6 (IPv6)</span></span>](internet-protocol-version-6-ipv6-2.md)
</dt> <dt>

[<span data-ttu-id="68ba1-132">Prise en charge D’ipv6</span><span class="sxs-lookup"><span data-stu-id="68ba1-132">IPv6 Support</span></span>](ipv6-support-2.md)
</dt> <dt>

[<span data-ttu-id="68ba1-133">Version préliminaire de la technologie IPv6 pour Windows 2000</span><span class="sxs-lookup"><span data-stu-id="68ba1-133">IPv6 Technology Preview for Windows 2000</span></span>](https://www.microsoft.com/downloads/details.aspx?FamilyID=27b1e6a6-bbdd-43c9-af57-dae19795a088)
</dt> <dt>

[<span data-ttu-id="68ba1-134">Utilisation de l’utilitaire Checkv4.exe</span><span class="sxs-lookup"><span data-stu-id="68ba1-134">Using the Checkv4.exe Utility</span></span>](using-the-checkv4-exe-utility-2.md)
</dt> <dt>

[<span data-ttu-id="68ba1-135">Annexe A : code source uniquement IPv4</span><span class="sxs-lookup"><span data-stu-id="68ba1-135">Appendix A: IPv4-only Source Code</span></span>](appendix-a-ipv4-only-source-code-2.md)
</dt> <dt>

[<span data-ttu-id="68ba1-136">Annexe B : code source agnostique de la version IP</span><span class="sxs-lookup"><span data-stu-id="68ba1-136">Appendix B: IP-version Agnostic Source Code</span></span>](appendix-b-ip-version-agnostic-source-code-2.md)
</dt> </dl>

 

 



