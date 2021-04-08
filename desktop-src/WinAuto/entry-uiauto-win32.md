---
title: Automatisation de l’interface utilisateur
description: Microsoft UI Automation est une infrastructure d’accessibilité qui permet aux applications Windows de fournir et d’utiliser des informations de programmation sur les interfaces utilisateur.
ms.assetid: 700ca38d-ff40-472b-a95a-11fa94c3bc1d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8006c79299cc1f736dc43555968443f634d4a51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842541"
---
# <a name="ui-automation"></a><span data-ttu-id="e08b2-103">Automatisation de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="e08b2-103">UI Automation</span></span>

<span data-ttu-id="e08b2-104">Microsoft UI Automation est une infrastructure d’accessibilité qui permet aux applications Windows de fournir et d’utiliser des informations de programmation sur les interfaces utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e08b2-104">Microsoft UI Automation is an accessibility framework that enables Windows applications to provide and consume programmatic information about user interfaces (UIs).</span></span> <span data-ttu-id="e08b2-105">Il fournit un accès par programme à la plupart des éléments d’interface utilisateur sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="e08b2-105">It provides programmatic access to most UI elements on the desktop.</span></span> <span data-ttu-id="e08b2-106">Il permet aux produits de technologie d’assistance, tels que les lecteurs d’écran, de fournir des informations sur l’interface utilisateur aux utilisateurs finaux et de manipuler l’interface utilisateur par d’autres moyens que l’entrée standard.</span><span class="sxs-lookup"><span data-stu-id="e08b2-106">It enables assistive technology products, such as screen readers, to provide information about the UI to end users and to manipulate the UI by means other than standard input.</span></span> <span data-ttu-id="e08b2-107">UI Automation permet également aux scripts de test automatisés d’interagir avec l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e08b2-107">UI Automation also allows automated test scripts to interact with the UI.</span></span>

-   [<span data-ttu-id="e08b2-108">Le cas échéant</span><span class="sxs-lookup"><span data-stu-id="e08b2-108">Where Applicable</span></span>](#where-applicable)
-   [<span data-ttu-id="e08b2-109">Public destiné aux développeurs</span><span class="sxs-lookup"><span data-stu-id="e08b2-109">Developer Audience</span></span>](#developer-audience)
-   [<span data-ttu-id="e08b2-110">Spécifications d’exécution</span><span class="sxs-lookup"><span data-stu-id="e08b2-110">Run-Time Requirements</span></span>](#run-time-requirements)
-   [<span data-ttu-id="e08b2-111">Prise en charge des systèmes d’exploitation de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="e08b2-111">Support for Down-level Operating Systems</span></span>](#support-for-down-level-operating-systems)

## <a name="where-applicable"></a><span data-ttu-id="e08b2-112">Cas d'emploi</span><span class="sxs-lookup"><span data-stu-id="e08b2-112">Where Applicable</span></span>

<span data-ttu-id="e08b2-113">À l’aide d’UI Automation et des pratiques de conception accessibles suivantes, les développeurs peuvent rendre les applications s’exécutant sur Windows plus accessibles à de nombreuses personnes avec une vision, une audition ou un handicap moteur.</span><span class="sxs-lookup"><span data-stu-id="e08b2-113">By using UI Automation and following accessible design practices, developers can make applications running on Windows more accessible to many people with vision, hearing, or motion disabilities.</span></span> <span data-ttu-id="e08b2-114">En outre, UI Automation est spécifiquement conçu pour fournir des fonctionnalités robustes pour les scénarios de test automatisé.</span><span class="sxs-lookup"><span data-stu-id="e08b2-114">Also, UI Automation is specifically designed to provide robust functionality for automated testing scenarios.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="e08b2-115">Public de développeurs</span><span class="sxs-lookup"><span data-stu-id="e08b2-115">Developer Audience</span></span>

<span data-ttu-id="e08b2-116">UI Automation est conçu pour les développeurs C/C++ expérimentés.</span><span class="sxs-lookup"><span data-stu-id="e08b2-116">UI Automation is designed for experienced C/C++ developers.</span></span> <span data-ttu-id="e08b2-117">En général, les développeurs ont besoin d’un niveau modéré de compréhension des objets COM (Component Object Model) et des interfaces, d’Unicode et de la programmation des API Windows.</span><span class="sxs-lookup"><span data-stu-id="e08b2-117">In general, developers need a moderate level of understanding about Component Object Model (COM) objects and interfaces, Unicode, and Windows API programming.</span></span>

<span data-ttu-id="e08b2-118">Pour plus d’informations sur UI Automation pour le code managé, consultez [accessibilité](/dotnet/framework/ui-automation/) dans la section Guide du développeur .NET Framework de MSDN.</span><span class="sxs-lookup"><span data-stu-id="e08b2-118">For information about UI Automation for managed code, please see [Accessibility](/dotnet/framework/ui-automation/) in the .NET Framework Developer's Guide section of MSDN.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="e08b2-119">Exigences d'exécution</span><span class="sxs-lookup"><span data-stu-id="e08b2-119">Run-Time Requirements</span></span>

<span data-ttu-id="e08b2-120">UI Automation est pris en charge sur les systèmes d’exploitation suivants : Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016 et Windows Server 2019.</span><span class="sxs-lookup"><span data-stu-id="e08b2-120">UI Automation is supported on the following operating systems: Windows XP, Windows Server 2003, Windows Server 2003 R2, Windows Vista, Windows 7, Windows 10, Windows Server 2008, Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2, Windows Server 2016, and Windows Server 2019.</span></span>

> [!Note]  
> <span data-ttu-id="e08b2-121">Windows XP et Windows Server 2003 nécessitent également Microsoft .NET Framework 3,0.</span><span class="sxs-lookup"><span data-stu-id="e08b2-121">Windows XP and Windows Server 2003 also require Microsoft .NET Framework 3.0.</span></span>

 

## <a name="support-for-down-level-operating-systems"></a><span data-ttu-id="e08b2-122">Prise en charge des systèmes d’exploitation de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="e08b2-122">Support for Down-level Operating Systems</span></span>

<span data-ttu-id="e08b2-123">La mise à jour de plateforme pour Windows Vista est un ensemble de bibliothèques d’exécution qui permet aux développeurs de cibler des applications sur des systèmes d’exploitation Windows 7 et de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="e08b2-123">The Platform Update for Windows Vista is a set of run-time libraries that enables developers to target applications to both Windows 7 and down-level operating systems.</span></span> <span data-ttu-id="e08b2-124">La mise à jour de plateforme pour Windows Server 2008 est un ensemble de bibliothèques d’exécution qui permet aux développeurs de cibler des applications à la fois vers Windows Server 2008 R2 et pour les versions antérieures de Windows Server.</span><span class="sxs-lookup"><span data-stu-id="e08b2-124">The Platform Update for Windows Server 2008 is a set of run-time libraries that enables developers to target applications to both Windows Server 2008 R2 and previous versions of Windows Server.</span></span> <span data-ttu-id="e08b2-125">La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update.</span><span class="sxs-lookup"><span data-stu-id="e08b2-125">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 will be available to all Windows Vista and Windows Server 2008 customers through Windows Update.</span></span> <span data-ttu-id="e08b2-126">Les applications tierces qui requièrent une mise à jour de plateforme pour Windows Vista ou une mise à jour de plateforme pour Windows Server 2008 peuvent avoir Windows Update détecter si elles sont installées ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="e08b2-126">Third-party applications that require Platform Update for Windows Vista or Platform Update for Windows Server 2008 can have Windows Update detect whether it is installed; if it is not, Windows Update will download and install it in the background.</span></span>

<span data-ttu-id="e08b2-127">La mise à jour de la plateforme pour Windows Vista et la mise à jour de la plateforme pour Windows Server 2008 prennent en charge l’ensemble des fonctionnalités de l’API Windows Automation 3,0 sur les systèmes d’exploitation suivants.</span><span class="sxs-lookup"><span data-stu-id="e08b2-127">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 both support the entire Windows Automation API 3.0 feature set on the following operating systems.</span></span>

-   <span data-ttu-id="e08b2-128">Windows XP (anglais)</span><span class="sxs-lookup"><span data-stu-id="e08b2-128">Windows XP (English)</span></span> <dl> <span data-ttu-id="e08b2-129">Windows XP famille SP3 x86</span><span class="sxs-lookup"><span data-stu-id="e08b2-129">Windows XP Home SP3 x86</span></span>  
    <span data-ttu-id="e08b2-130">Windows XP Professionnel SP3 x86</span><span class="sxs-lookup"><span data-stu-id="e08b2-130">Windows XP Professional SP3 x86</span></span>  
    </dl>
-   Windows Server 2003 (English) <dl> <span data-ttu-id="e08b2-131">Windows Server 2003 SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-131">Windows Server 2003 SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="e08b2-132">Windows Vista (anglais)</span><span class="sxs-lookup"><span data-stu-id="e08b2-132">Windows Vista (English)</span></span> <dl> <span data-ttu-id="e08b2-133">Starter SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-133">Starter SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="e08b2-134">Édition familiale Premium SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-134">Home Premium SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="e08b2-135">Business Pack SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-135">Business SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="e08b2-136">Enterprise SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-136">Enterprise SP2 (x86 and x64)</span></span>  
    <span data-ttu-id="e08b2-137">Ultimate SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-137">Ultimate SP2 (x86 and x64)</span></span>  
    </dl>
-   <span data-ttu-id="e08b2-138">Windows Server 2008 (anglais)</span><span class="sxs-lookup"><span data-stu-id="e08b2-138">Windows Server 2008 (English)</span></span> <dl> <span data-ttu-id="e08b2-139">Windows Server 2008 SP2 (x86 et x64)</span><span class="sxs-lookup"><span data-stu-id="e08b2-139">Windows Server 2008 SP2 (x86 and x64)</span></span>  
    </dl>

<span data-ttu-id="e08b2-140">Pour plus d’informations sur les deux mises à jour, consultez [mise à jour de la plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span><span class="sxs-lookup"><span data-stu-id="e08b2-140">For more information about both updates, see [Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e08b2-141">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="e08b2-141">In this section</span></span>

-   [<span data-ttu-id="e08b2-142">Notions de base d’UI Automation</span><span class="sxs-lookup"><span data-stu-id="e08b2-142">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
-   [<span data-ttu-id="e08b2-143">Guide du programmeur du fournisseur UI Automation</span><span class="sxs-lookup"><span data-stu-id="e08b2-143">UI Automation Provider Programmer's Guide</span></span>](uiauto-providerportal.md)
-   [<span data-ttu-id="e08b2-144">Guide du programmeur du client UI Automation</span><span class="sxs-lookup"><span data-stu-id="e08b2-144">UI Automation Client Programmer's Guide</span></span>](uiauto-clientportal.md)
-   [<span data-ttu-id="e08b2-145">Référence</span><span class="sxs-lookup"><span data-stu-id="e08b2-145">Reference</span></span>](entry-uiautocore-ref.md)
-   [<span data-ttu-id="e08b2-146">Exemples</span><span class="sxs-lookup"><span data-stu-id="e08b2-146">Samples</span></span>](samples-entry.md)
-   [<span data-ttu-id="e08b2-147">Annexes</span><span class="sxs-lookup"><span data-stu-id="e08b2-147">Appendixes</span></span>](appendix-entry.md)

 

 