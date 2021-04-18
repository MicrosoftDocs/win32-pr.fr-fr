---
description: .
ms.assetid: 974650d9-504a-4f19-bc71-90fbc92672d9
title: Contrôle de version du système d’exploitation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e71cb671e19463ca6137c9b0ce7af04c2793e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519558"
---
# <a name="operating-system-versioning"></a><span data-ttu-id="d7143-103">Contrôle de version du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="d7143-103">Operating System Versioning</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="d7143-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="d7143-104">Affected Platforms</span></span>

<span data-ttu-id="d7143-105">**Clients** -Windows 7</span><span class="sxs-lookup"><span data-stu-id="d7143-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="d7143-106">**Serveurs** -Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="d7143-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="d7143-107">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="d7143-107">Feature Impact</span></span>

<span data-ttu-id="d7143-108">**Gravité** -haute</span><span class="sxs-lookup"><span data-stu-id="d7143-108">**Severity** - High</span></span>  
<span data-ttu-id="d7143-109">**Fréquence** -élevée</span><span class="sxs-lookup"><span data-stu-id="d7143-109">**Frequency** - High</span></span>  









## <a name="description"></a><span data-ttu-id="d7143-110">Description</span><span class="sxs-lookup"><span data-stu-id="d7143-110">Description</span></span>

<span data-ttu-id="d7143-111">Le numéro de version interne de Windows 7 et de Windows Server 2008 R2 est 6,1.</span><span class="sxs-lookup"><span data-stu-id="d7143-111">The internal version number for Windows 7 and Windows Server 2008 R2 is 6.1.</span></span> <span data-ttu-id="d7143-112">La fonction GetVersion retourne maintenant ce numéro de version aux applications lorsqu’elles sont interrogées.</span><span class="sxs-lookup"><span data-stu-id="d7143-112">The GetVersion function will now return this version number to applications when queried.</span></span> <span data-ttu-id="d7143-113">Ceci est particulièrement important pour les AntiVirus, les sauvegardes, les applications utilitaires et la protection contre la copie.</span><span class="sxs-lookup"><span data-stu-id="d7143-113">This is especially important for AntiVirus, backup, utility applications, and copy protection.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="d7143-114">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="d7143-114">Manifestation of Impact</span></span>

<span data-ttu-id="d7143-115">La description de cette modification est spécifique à l’application.</span><span class="sxs-lookup"><span data-stu-id="d7143-115">The manifestation of this change is application-specific.</span></span> <span data-ttu-id="d7143-116">Cela signifie que toute application qui recherche spécifiquement la version du système d’exploitation obtiendra un numéro de version plus élevé, ce qui peut entraîner une ou plusieurs des situations suivantes :</span><span class="sxs-lookup"><span data-stu-id="d7143-116">This means that any application that specifically checks for the operating system version will get a higher version number, which can lead to one or more of the following situations:</span></span>

-   <span data-ttu-id="d7143-117">Les programmes d’installation d’application ne peuvent pas installer l’application, et les applications peuvent ne pas pouvoir démarrer</span><span class="sxs-lookup"><span data-stu-id="d7143-117">Application installers might be unable to install the application, and applications might be unable to start</span></span>
-   <span data-ttu-id="d7143-118">Les applications peuvent devenir instables ou se bloquer</span><span class="sxs-lookup"><span data-stu-id="d7143-118">Applications might become unstable or crash</span></span>
-   <span data-ttu-id="d7143-119">Les applications peuvent générer des messages d’erreur, mais continuer à fonctionner correctement</span><span class="sxs-lookup"><span data-stu-id="d7143-119">Applications might generate error messages, but continue to function properly</span></span>

## <a name="mitigation"></a><span data-ttu-id="d7143-120">Limitation des risques</span><span class="sxs-lookup"><span data-stu-id="d7143-120">Mitigation</span></span>

<span data-ttu-id="d7143-121">La plupart des applications fonctionneront correctement sur Windows 7 et Windows Server 2008 R2, car la compatibilité des applications dans Windows 7 et Windows Server 2008 R2 est très élevée.</span><span class="sxs-lookup"><span data-stu-id="d7143-121">Most applications will function properly on Windows 7 and Windows Server 2008 R2 because the application compatibility in Windows 7 and Windows Server 2008 R2 is very high.</span></span> <span data-ttu-id="d7143-122">Toutefois, Windows 7 et Windows Server 2008 R2 incluent une vue de compatibilité pour les programmes d’installation et les applications qui vérifient la version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d7143-122">However, Windows 7 and Windows Server 2008 R2 include a Compatibility View for installers and applications that check for operating system version.</span></span>

<span data-ttu-id="d7143-123">Pour activer l’affichage de compatibilité, les utilisateurs peuvent cliquer avec le bouton droit sur le raccourci ou le fichier exécutable, puis appliquer l’affichage de compatibilité Windows XP SP2 ou Windows Vista à partir de l’onglet compatibilité. Dans la plupart des cas, cela doit permettre à l’application de fonctionner correctement sans avoir à modifier l’application.</span><span class="sxs-lookup"><span data-stu-id="d7143-123">To enable the compatibility view, users can right-click the shortcut or the executable file, and then apply the Windows XP SP2 or Windows Vista Compatibility View from the Compatibility tab. In most cases, this should enable the application to operate properly without the need for any changes to the application.</span></span>

<span data-ttu-id="d7143-124">Les professionnels de l’informatique peuvent également appliquer l’un des correctifs de compatibilité VersionLie applicables, à l’aide de l’outil d’administration de la compatibilité, qui est installé avec Application Compatibility Toolkit (ACT).</span><span class="sxs-lookup"><span data-stu-id="d7143-124">IT Professionals can also apply any of the applicable VersionLie compatibility fixes, by using the Compatibility Administrator tool, which installs with the Application Compatibility Toolkit (ACT).</span></span> <span data-ttu-id="d7143-125">Par exemple, si une application ne fonctionne pas parce qu’elle recherche, mais ne trouve pas, les informations de version de Windows XP® avec Service Pack 2 (SP2), le WinXPSP2VersionLie peut être appliqué pour retourner les informations de numéro de version appropriées à l’application, quelle que soit la version du système d’exploitation en cours d’exécution sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d7143-125">For example, if an application fails to function because it is checking for, but not finding, the Windows XP® with Service Pack 2 (SP2) version information, the WinXPSP2VersionLie can be applied to return the proper version number information to the application, regardless of the actual operating system version that is running on the computer.</span></span> <span data-ttu-id="d7143-126">Les correctifs de compatibilité VersionLie disponibles sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="d7143-126">The available VersionLie compatibility fixes are:</span></span>

-   <span data-ttu-id="d7143-127">Win95VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-127">Win95VersionLie</span></span>
-   <span data-ttu-id="d7143-128">Win98VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-128">Win98VersionLie</span></span>
-   <span data-ttu-id="d7143-129">WinNT4SP5VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-129">WinNT4SP5VersionLie</span></span>
-   <span data-ttu-id="d7143-130">Win2000VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-130">Win2000VersionLie</span></span>
-   <span data-ttu-id="d7143-131">Win2000SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-131">Win2000SP1VersionLie</span></span>
-   <span data-ttu-id="d7143-132">Win2000SP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-132">Win2000SP2VersionLie</span></span>
-   <span data-ttu-id="d7143-133">Win2000SP3VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-133">Win2000SP3VersionLie</span></span>
-   <span data-ttu-id="d7143-134">WinXPVersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-134">WinXPVersionLie</span></span>
-   <span data-ttu-id="d7143-135">WinXPSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-135">WinXPSP1VersionLie</span></span>
-   <span data-ttu-id="d7143-136">WinXPSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-136">WinXPSP2VersionLie</span></span>
-   <span data-ttu-id="d7143-137">VistaRTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-137">VistaRTMVersionLie</span></span>
-   <span data-ttu-id="d7143-138">VistaSP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-138">VistaSP1VersionLie</span></span>
-   <span data-ttu-id="d7143-139">VistaSP2VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-139">VistaSP2VersionLie</span></span>
-   <span data-ttu-id="d7143-140">Win2K3RTMVersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-140">Win2K3RTMVersionLie</span></span>
-   <span data-ttu-id="d7143-141">Win2K3SP1VersionLie</span><span class="sxs-lookup"><span data-stu-id="d7143-141">Win2K3SP1VersionLie</span></span>

## <a name="solution"></a><span data-ttu-id="d7143-142">Solution</span><span class="sxs-lookup"><span data-stu-id="d7143-142">Solution</span></span>

<span data-ttu-id="d7143-143">En règle générale, les applications ne doivent pas effectuer de vérifications de version du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d7143-143">Generally, applications should not perform operating system version checks.</span></span> <span data-ttu-id="d7143-144">Si une application a besoin d’une fonctionnalité spécifique, il est préférable d’essayer de la trouver et d’échouer uniquement si la fonctionnalité nécessaire est manquante.</span><span class="sxs-lookup"><span data-stu-id="d7143-144">If an application needs a specific feature, it is preferable to try to find the feature, and fail only if the needed feature is missing.</span></span> <span data-ttu-id="d7143-145">Au minimum, les applications doivent toujours accepter les numéros de version supérieurs ou égaux à la version la plus ancienne prise en charge du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d7143-145">At a minimum, applications should always accept version numbers greater than or equal to the lowest supported version of the operating system.</span></span> <span data-ttu-id="d7143-146">Les exceptions doivent se produire uniquement si une exigence légale, commerciale ou de composant système spécifique est requise.</span><span class="sxs-lookup"><span data-stu-id="d7143-146">Exceptions should occur only if there is a specific legal, business, or system-component requirement.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="d7143-147">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="d7143-147">Links to Other Resources</span></span>

-   [<span data-ttu-id="d7143-148">Téléchargement de l’outil Application Compatibility Toolkit</span><span class="sxs-lookup"><span data-stu-id="d7143-148">Application Compatibility Toolkit Download</span></span>](/windows-hardware/get-started/adk-install)
-   <span data-ttu-id="d7143-149">[Correctifs de compatibilité connus, modes de compatibilité et messages AppHelp](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="d7143-149">[Known Compatibility Fixes, Compatibility Modes, and AppHelp Messages](/previous-versions/windows/it-pro/windows-7/cc765984(v=ws.10))</span></span>

 

 
