---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protection des ressources Windows supplémentaires sur les clés de Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542990"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="95f87-103">Protection des ressources Windows supplémentaires sur les clés de Registre</span><span class="sxs-lookup"><span data-stu-id="95f87-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="95f87-104">Plateforme</span><span class="sxs-lookup"><span data-stu-id="95f87-104">Platform</span></span>

<span data-ttu-id="95f87-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="95f87-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="95f87-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="95f87-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="95f87-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="95f87-107">Feature Impact</span></span>

<span data-ttu-id="95f87-108">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="95f87-108">**Severity** - Medium</span></span>  
<span data-ttu-id="95f87-109">**Fréquence** -faible</span><span class="sxs-lookup"><span data-stu-id="95f87-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="95f87-110">Description</span><span class="sxs-lookup"><span data-stu-id="95f87-110">Description</span></span>

<span data-ttu-id="95f87-111">Des ressources système supplémentaires ont ajouté des paramètres Protection des ressources Windows (WRP) dans Windows 7, ce qui les rend accessibles en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="95f87-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="95f87-112">La grande majorité des ressources qui ont reçu une protection supplémentaire sont des clés de serveur COM système, bien que certaines fonctionnalités aient ajouté une protection des ressources ciblée.</span><span class="sxs-lookup"><span data-stu-id="95f87-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="95f87-113">Microsoft a modifié ces ressources afin de protéger le système et d’autres applications contre les interruptions et de fournir une plateforme cohérente et stable sur laquelle les applications peuvent s’exécuter de manière fiable.</span><span class="sxs-lookup"><span data-stu-id="95f87-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="95f87-114">Dans le passé, les applications pouvaient fournir des fichiers personnalisés et utiliser l’inscription COM non protégée pour modifier le système.</span><span class="sxs-lookup"><span data-stu-id="95f87-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="95f87-115">Dans le cas d’applications plus anciennes, cela peut rétrograder les runtimes du système ou modifier l’interface sur laquelle les autres applications devaient fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="95f87-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="95f87-116">Dans le pire des cas, ces installations peuvent entraîner des défaillances ou une dégradation du système au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="95f87-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="95f87-117">Pour offrir une meilleure expérience et une plate-forme d’application plus stable, nous avons verrouillé ces inscriptions afin que seules les mises à jour Microsoft puissent modifier les composants système.</span><span class="sxs-lookup"><span data-stu-id="95f87-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="95f87-118">Étant donné que la plupart des ressources modifiées sont des clés COM utilisées par le système, cette modification n’affecte pas la majorité des applications.</span><span class="sxs-lookup"><span data-stu-id="95f87-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="95f87-119">Bien que nous pensons que la plupart des applications ont une meilleure expérience sur Windows 7 suite à ces modifications, un petit sous-ensemble d’applications peut être affecté.</span><span class="sxs-lookup"><span data-stu-id="95f87-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="95f87-120">Les couches de compatibilité des applications du système résolvent automatiquement les problèmes d’installation en indiquant toujours à l’application qu’elle a réussi à modifier un paramètre, même si elle a échoué en raison d’une ressource protégée.</span><span class="sxs-lookup"><span data-stu-id="95f87-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="95f87-121">Cela empêche les configurations d’applications de s’arrêter, mais peut entraîner des problèmes si le paramètre devait être modifié pour que l’application fonctionne correctement.</span><span class="sxs-lookup"><span data-stu-id="95f87-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="95f87-122">Manifestation</span><span class="sxs-lookup"><span data-stu-id="95f87-122">Manifestation</span></span>

<span data-ttu-id="95f87-123">Les applications ont peut-être modifié ces paramètres avant Windows 7.</span><span class="sxs-lookup"><span data-stu-id="95f87-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="95f87-124">Lors de l’installation de sur Windows 7, certaines fonctionnalités de peuvent ne plus fonctionner, car les paramètres ne reflètent pas ce que l’application attendait.</span><span class="sxs-lookup"><span data-stu-id="95f87-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="95f87-125">Il existe deux scénarios dans lesquels les applications peuvent rencontrer des problèmes liés à cette protection supplémentaire :</span><span class="sxs-lookup"><span data-stu-id="95f87-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="95f87-126">Applications qui utilisaient peut-être des paramètres protégés en tant que magasin de données ou comme un point d’extensibilité rare ou non ATTENDU</span><span class="sxs-lookup"><span data-stu-id="95f87-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="95f87-127">Dans de rares cas, le mécanisme de détection utilisé pour identifier les configurations d’applications peut ne pas reconnaître une configuration particulière et la couche d’atténuation de la compatibilité des applications ne peut donc pas être appliquée.</span><span class="sxs-lookup"><span data-stu-id="95f87-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="95f87-128">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="95f87-128">Mitigation</span></span>

<span data-ttu-id="95f87-129">Le principal moyen d’atténuation est la couche de compatibilité des applications du système, qui est appliquée automatiquement aux configurations d’applications lorsqu’elles sont détectées.</span><span class="sxs-lookup"><span data-stu-id="95f87-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="95f87-130">Vous pouvez également l’appliquer manuellement à n’importe quelle application à l’aide de l’onglet compatibilité dans les propriétés de l’application.</span><span class="sxs-lookup"><span data-stu-id="95f87-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="95f87-131">Cette couche résout le problème en interceptant les opérations du Registre.</span><span class="sxs-lookup"><span data-stu-id="95f87-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="95f87-132">Dans le cas où l’application essayait de modifier un paramètre en lecture seule (WRP), la couche retourne toujours Success, même si le paramètre n’a pas été vraiment modifié.</span><span class="sxs-lookup"><span data-stu-id="95f87-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="95f87-133">Pour la plupart des applications, cela ne pose aucun problème.</span><span class="sxs-lookup"><span data-stu-id="95f87-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="95f87-134">Toutefois, il est possible que l’application ait besoin de ce paramètre modifié pour fonctionner correctement, qui est le premier scénario décrit ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="95f87-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="95f87-135">Solution</span><span class="sxs-lookup"><span data-stu-id="95f87-135">Solution</span></span>

<span data-ttu-id="95f87-136">Pour les deux scénarios identifiés ci-dessus :</span><span class="sxs-lookup"><span data-stu-id="95f87-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="95f87-137">Si l’application requiert que la clé soit accessible en écriture pour fonctionner ou utiliser le magasin de données, il n’existe aucune solution autre que la modification de l’application afin qu’elle n’écrit plus à cet emplacement.</span><span class="sxs-lookup"><span data-stu-id="95f87-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="95f87-138">Si la couche de compatibilité n’a pas été appliquée à une installation, l’échec du programme d’installation doit être détecté et proposé pour être appliqué et réexécuté.</span><span class="sxs-lookup"><span data-stu-id="95f87-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="95f87-139">Les applications peuvent également s’exécuter en mode de compatibilité, auquel cas la couche d’atténuation est toujours appliquée.</span><span class="sxs-lookup"><span data-stu-id="95f87-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="95f87-140">Tests de compatibilité</span><span class="sxs-lookup"><span data-stu-id="95f87-140">Compatibility Tests</span></span>

<span data-ttu-id="95f87-141">Comment détecter si un programme d’atténuation de WRP est appliqué à une application :</span><span class="sxs-lookup"><span data-stu-id="95f87-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="95f87-142">Windows Installer est conscient de WRP ; elle ignore automatiquement et silencieusement les tentatives d’écriture ou de modification d’une ressource protégée.</span><span class="sxs-lookup"><span data-stu-id="95f87-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="95f87-143">Si l’application a été installée avec Windows Installer et que la journalisation a été activée, un avertissement est consigné pour chaque opération d’écriture de clé de Registre ignorée en raison de sa ressource protégée par WRP.</span><span class="sxs-lookup"><span data-stu-id="95f87-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="95f87-144">L’API WRP intègre SfCIsKeyProtected, qui peut demander si une clé de Registre est protégée par WRP sur le système actuel.</span><span class="sxs-lookup"><span data-stu-id="95f87-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="95f87-145">Pour plus d’informations sur l’utilisation de cette API, consultez l’entrée WRP sur MSDN dans les liens ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="95f87-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="95f87-146">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="95f87-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="95f87-147">Protection des ressources Windows</span><span class="sxs-lookup"><span data-stu-id="95f87-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
