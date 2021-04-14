---
title: Gadgets du Bureau supprimés
description: Gadgets du Bureau supprimés
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- Gadgets
- gadgets du Bureau
- Encadré Windows
- Barre latérale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c37c058a75aca82d7727566041af4c30f3bb474
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104383040"
---
# <a name="desktop-gadgets-removed"></a><span data-ttu-id="7c157-107">Gadgets du Bureau supprimés</span><span class="sxs-lookup"><span data-stu-id="7c157-107">Desktop gadgets removed</span></span>

## <a name="platforms"></a><span data-ttu-id="7c157-108">Plateformes</span><span class="sxs-lookup"><span data-stu-id="7c157-108">Platforms</span></span>

 <span data-ttu-id="7c157-109">**Clients** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="7c157-109">**Clients** - Windows 8</span></span>  
<span data-ttu-id="7c157-110">**Serveurs** -Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7c157-110">**Servers** - Windows Server 2012</span></span>  



## <a name="description"></a><span data-ttu-id="7c157-111">Description</span><span class="sxs-lookup"><span data-stu-id="7c157-111">Description</span></span>

<span data-ttu-id="7c157-112">Du point de vue des fonctionnalités, les gadgets ont déjà été dépréciés et sont déclassés par de nouvelles vignettes et applications dynamiques.</span><span class="sxs-lookup"><span data-stu-id="7c157-112">From a functionality standpoint, Gadgets have already been deprecated and are outclassed by new live tiles and apps.</span></span> <span data-ttu-id="7c157-113">Les gadgets présentent également un risque pour la sécurité pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="7c157-113">Gadgets also present a security risk to users.</span></span> <span data-ttu-id="7c157-114">En tant que plateforme, il existe des vulnérabilités telles que des gadgets sans gravité pourraient être exploités.</span><span class="sxs-lookup"><span data-stu-id="7c157-114">As a platform, vulnerabilities exist such that even benign Gadgets could be exploited.</span></span> <span data-ttu-id="7c157-115">Par conséquent, afin de respecter Windows 8 comme système d’exploitation le plus moderne et le plus sécurisé, nous avons choisi de supprimer entièrement les gadgets du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7c157-115">Therefore, in order to uphold Windows 8 as our most modern and secure operating system, we have chosen to remove Gadgets from the operating system entirely.</span></span> <span data-ttu-id="7c157-116">Les utilisateurs de Windows 7 avec des gadgets sur leur bureau seront avertis et les gadgets seront désinstallés.</span><span class="sxs-lookup"><span data-stu-id="7c157-116">Windows 7 users with Gadgets on their Desktop will be notified and Gadgets will be uninstalled.</span></span>

## <a name="manifestation"></a><span data-ttu-id="7c157-117">Manifestation</span><span class="sxs-lookup"><span data-stu-id="7c157-117">Manifestation</span></span>

<span data-ttu-id="7c157-118">Les gadgets du Bureau ne sont pas disponibles sur le bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="7c157-118">Desktop Gadgets will not be available on the Windows Desktop.</span></span>

## <a name="mitigation"></a><span data-ttu-id="7c157-119">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="7c157-119">Mitigation</span></span>

<span data-ttu-id="7c157-120">L’API et la structure des dossiers des gadgets Desktop resteront en place pour Windows 8.</span><span class="sxs-lookup"><span data-stu-id="7c157-120">The Desktop Gadgets API and folder structure will remain in place for Windows 8.</span></span> <span data-ttu-id="7c157-121">Les applications qui installent et exécutent par programme des gadgets à l’aide de cette API continuent de s’exécuter sans échec (même si les gadgets eux-mêmes ne le sont pas).</span><span class="sxs-lookup"><span data-stu-id="7c157-121">Applications which programmatically install and run Gadgets using this API will continue to run without fail (although the Gadgets themselves will not).</span></span>

## <a name="solution"></a><span data-ttu-id="7c157-122">Solution</span><span class="sxs-lookup"><span data-stu-id="7c157-122">Solution</span></span>

<span data-ttu-id="7c157-123">Les développeurs d’applications de bureau ne doivent pas empaqueter des gadgets dans leurs programmes d’installation.</span><span class="sxs-lookup"><span data-stu-id="7c157-123">Desktop app developers should not package Gadgets in their installers.</span></span> <span data-ttu-id="7c157-124">Ces gadgets occupent simplement de l’espace pour l’utilisateur et ne peuvent pas être exécutés dans le système.</span><span class="sxs-lookup"><span data-stu-id="7c157-124">These Gadgets will just take up space for the user and will not be able to be run in the system.</span></span>

## <a name="tests"></a><span data-ttu-id="7c157-125">Tests</span><span class="sxs-lookup"><span data-stu-id="7c157-125">Tests</span></span>

<span data-ttu-id="7c157-126">Les développeurs sont en mesure de tester la compatibilité de ce changement en désactivant le composant facultatif pour les gadgets de bureau dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7c157-126">Developers are able to test compatibility of this change by disabling the optional component for Desktop Gadgets in Windows 7.</span></span> <span data-ttu-id="7c157-127">Pour désactiver les gadgets sur un PC Windows 7, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="7c157-127">To disable Gadgets on a Windows 7 PC, follow the steps below:</span></span>

1.  <span data-ttu-id="7c157-128">Accédez à activer ou désactiver des fonctionnalités Windows dans le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="7c157-128">Navigate to Turn Windows Features on or off from the Control Panel.</span></span>
2.  <span data-ttu-id="7c157-129">Désactivez la case à cocher en regard de « plateforme Gadget Windows ».</span><span class="sxs-lookup"><span data-stu-id="7c157-129">Uncheck the box next to “Windows Gadget Platform”.</span></span>
3.  <span data-ttu-id="7c157-130">Cliquez sur OK et suivez les autres instructions à l’écran.</span><span class="sxs-lookup"><span data-stu-id="7c157-130">Click OK and follow any additional on-screen instructions.</span></span>

## <a name="resources"></a><span data-ttu-id="7c157-131">Ressources</span><span class="sxs-lookup"><span data-stu-id="7c157-131">Resources</span></span>

[<span data-ttu-id="7c157-132">Des vulnérabilités dans les gadgets pourraient permettre l’exécution de code à distance</span><span class="sxs-lookup"><span data-stu-id="7c157-132">Vulnerabilities in Gadgets Could Allow Remote Code Execution</span></span>](https://support.microsoft.com/kb/2719662)

 

 




