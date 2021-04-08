---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8-chaîne de l’agent utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be481cf409468d9d182d37ae7636b167bc71d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865970"
---
# <a name="internet-explorer-8---user-agent-string"></a><span data-ttu-id="be515-103">Internet Explorer 8-chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="be515-103">Internet Explorer 8 - User Agent String</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="be515-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="be515-104">Affected Platforms</span></span>

 <span data-ttu-id="be515-105">**Clients** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="be515-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="be515-106">**Serveurs** -windows Server 2003 \| Windows Server 2008 Windows Server \| 2008 R2</span><span class="sxs-lookup"><span data-stu-id="be515-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  










## <a name="feature-impact"></a><span data-ttu-id="be515-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="be515-107">Feature Impact</span></span>

<span data-ttu-id="be515-108">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="be515-108">**Severity** - Medium</span></span>  
<span data-ttu-id="be515-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="be515-109">**Frequency** - High</span></span>  











## <a name="description"></a><span data-ttu-id="be515-110">Description</span><span class="sxs-lookup"><span data-stu-id="be515-110">Description</span></span>

<span data-ttu-id="be515-111">La chaîne de l’agent utilisateur est l’identificateur Internet Explorer qui fournit des données sur sa version et d’autres attributs aux serveurs Web.</span><span class="sxs-lookup"><span data-stu-id="be515-111">The User Agent String is the Internet Explorer identifier that provides data about its version and other attributes to web servers.</span></span> <span data-ttu-id="be515-112">De nombreuses applications Web s’appuient sur la chaîne de l’agent utilisateur d’IE.</span><span class="sxs-lookup"><span data-stu-id="be515-112">Many web applications rely on, and piggyback on, the IE User Agent String.</span></span> <span data-ttu-id="be515-113">Celles qui le font et dépendent d’un numéro de version antérieure seront affectées.</span><span class="sxs-lookup"><span data-stu-id="be515-113">Those that do so and depend on an earlier version number will be impacted.</span></span> <span data-ttu-id="be515-114">La chaîne de l’agent utilisateur comprend désormais la chaîne « Trident/4.0 » afin d’autoriser la différenciation entre la chaîne de l’agent utilisateur d’Internet Explorer 7 et la chaîne de l’agent utilisateur d’Internet Explorer 8 lors de l’exécution dans l’affichage de compatibilité d’Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="be515-114">The User Agent string now includes the string 'Trident/4.0' in order to allow differentiation between the Internet Explorer 7 User Agent String and the Internet Explorer 8 User Agent string when running in Internet Explorer 7 Compatibility View.</span></span> <span data-ttu-id="be515-115">Pour plus d’informations, consultez Description des chaînes de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be515-115">See Understanding User Agent Strings for details.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="be515-116">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="be515-116">Manifestation of Impact</span></span>

<span data-ttu-id="be515-117">Il y a deux zones affectées :</span><span class="sxs-lookup"><span data-stu-id="be515-117">There are two impacted areas:</span></span>

-   <span data-ttu-id="be515-118">Les pages Web qui vérifient explicitement la chaîne de l’agent utilisateur et ne prennent pas en charge la chaîne de l’agent utilisateur d’Internet Explorer 8 peuvent ne pas s’exécuter correctement.</span><span class="sxs-lookup"><span data-stu-id="be515-118">Webpages that explicitly check the User Agent String and do not support the Internet Explorer 8 User Agent String may not run properly.</span></span> <span data-ttu-id="be515-119">Dans la plupart des cas, cela signifie que les pages seront bloquées par les utilisateurs du contenu auquel ils tentent d’accéder ou affichent du contenu incorrect ou incorrect.</span><span class="sxs-lookup"><span data-stu-id="be515-119">In the majority of cases, this means the pages will be block users from the content they are attempting to access or display incorrect or malformed content.</span></span>
-   <span data-ttu-id="be515-120">Les applications qui hébergent Trident (voir hébergement et réutilisation) utilisent par défaut Internet Explorer 7 en utilisant le composant Web facultatif, mais n’ont pas accès aux fonctionnalités d’Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="be515-120">Applications that host Trident (see Hosting and Reuse) will default to Internet Explorer 7 using the Web Optional Component, but will not have access to Internet Explorer 8 features.</span></span>

## <a name="solution"></a><span data-ttu-id="be515-121">Solution</span><span class="sxs-lookup"><span data-stu-id="be515-121">Solution</span></span>

<span data-ttu-id="be515-122">Assurez-vous que vos applications gèrent correctement la nouvelle version « MSIE 8,0 » dans la chaîne de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be515-122">Ensure that your applications properly handle the new 'MSIE 8.0' version in the User Agent String.</span></span> <span data-ttu-id="be515-123">Vous pouvez également vous abonner à l’affichage de compatibilité d’Internet Explorer 7 pour ces applications basées sur Internet Explorer 7.</span><span class="sxs-lookup"><span data-stu-id="be515-123">You may also opt in to the Internet Explorer 7 Compatibility View for those applications based on Internet Explorer 7.</span></span> <span data-ttu-id="be515-124">Pour ce faire, vous pouvez utiliser des balises méta.</span><span class="sxs-lookup"><span data-stu-id="be515-124">This can be done with meta tags.</span></span> <span data-ttu-id="be515-125">Pour plus d’informations, consultez la rubrique Présentation des chaînes de l’agent utilisateur.</span><span class="sxs-lookup"><span data-stu-id="be515-125">See the discussion in Understanding User Agent Strings for details.</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="be515-126">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="be515-126">Compatibility, Performance, Reliability, and Usability Testing</span></span>

-   <span data-ttu-id="be515-127">Exécutez vos applications et pages Web dans un environnement Internet Explorer 8 sous Windows Vista ou Windows XP pour vous assurer qu’elles se comportent de la manière souhaitée.</span><span class="sxs-lookup"><span data-stu-id="be515-127">Run your applications and webpages in an Internet Explorer 8 environment on Windows Vista or Windows XP to ensure that they behave in the desired manner.</span></span>
-   <span data-ttu-id="be515-128">Vous pouvez également exécuter l’outil de test de compatibilité Internet Explorer (IECTT) fourni avec Application Compatibility Toolkit (ACT) pour localiser les problèmes potentiels liés aux mises à jour des fonctionnalités de sécurité.</span><span class="sxs-lookup"><span data-stu-id="be515-128">Alternatively, you can run the Internet Explorer Compatibility Test Tool (IECTT) provided with the Application Compatibility Toolkit (ACT) to locate any potential issues due to security feature updates.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="be515-129">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="be515-129">Links to Other Resources</span></span>

-   <span data-ttu-id="be515-130">[Fonctionnement des chaînes de l’agent utilisateur](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be515-130">[Understanding User Agent Strings](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))</span></span>
-   [<span data-ttu-id="be515-131">Chaîne de User-Agent d’Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="be515-131">Internet Explorer 8 User-Agent String</span></span>](/archive/blogs/ie/)
-   [<span data-ttu-id="be515-132">Vecteur de version et de chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="be515-132">User-Agent String and Version Vector</span></span>](https://archive.msdn.microsoft.com/ie8whitepapers)
-   <span data-ttu-id="be515-133">[Hébergement et réutilisation](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="be515-133">[Hosting and Reuse](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))</span></span>
-   [<span data-ttu-id="be515-134">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="be515-134">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="be515-135">[Problèmes connus liés aux fonctionnalités de sécurité d’Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="be515-135">[Known Internet Explorer Security Feature Issues](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))</span></span>

 

 
