---
description: Interface utilisateur - Prise en charge de la haute résolution
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: Interface utilisateur - Prise en charge de la haute résolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116067"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="3dd74-103">Interface utilisateur - Prise en charge de la haute résolution</span><span class="sxs-lookup"><span data-stu-id="3dd74-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="3dd74-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="3dd74-104">Affected Platforms</span></span>

 <span data-ttu-id="3dd74-105">**Clients** -Windows XP Windows \| Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="3dd74-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="3dd74-106">Impact sur les fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="3dd74-106">Feature Impact</span></span>

<span data-ttu-id="3dd74-107">**Gravité** -moyenne</span><span class="sxs-lookup"><span data-stu-id="3dd74-107">**Severity** - Medium</span></span>  
<span data-ttu-id="3dd74-108">**Fréquence** -moyenne</span><span class="sxs-lookup"><span data-stu-id="3dd74-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="3dd74-109">Description</span><span class="sxs-lookup"><span data-stu-id="3dd74-109">Description</span></span>

<span data-ttu-id="3dd74-110">L’objectif est d’encourager les utilisateurs finaux à définir leurs affichages sur la résolution native et à utiliser DPI plutôt que la résolution d’écran pour modifier la taille du texte affiché et des images.</span><span class="sxs-lookup"><span data-stu-id="3dd74-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="3dd74-111">Windows 7 peut détecter automatiquement et configurer une résolution par défaut pour les nouvelles installations sur les ordinateurs configurés par leurs OEM à l’aide des paramètres ppp.</span><span class="sxs-lookup"><span data-stu-id="3dd74-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="3dd74-112">Il existe des outils que vous pouvez utiliser pour concevoir des applications qui prennent en charge la résolution élevée afin de garantir les résultats les plus lisibles.</span><span class="sxs-lookup"><span data-stu-id="3dd74-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="3dd74-113">Nous avons ajouté deux nouvelles fonctionnalités haute résolution à Windows 7 :</span><span class="sxs-lookup"><span data-stu-id="3dd74-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="3dd74-114">Paramètre PPP par utilisateur (précédemment par ordinateur)</span><span class="sxs-lookup"><span data-stu-id="3dd74-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="3dd74-115">Modifier le DPI sans redémarrer (la fermeture/la connexion est toujours requise)</span><span class="sxs-lookup"><span data-stu-id="3dd74-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="3dd74-116">Manifeste de l’impact</span><span class="sxs-lookup"><span data-stu-id="3dd74-116">Manifestation of Impact</span></span>

<span data-ttu-id="3dd74-117">Les applications qui ne gèrent pas le cas de résolution élevée sont susceptibles d’exposer des artefacts visuels, notamment :</span><span class="sxs-lookup"><span data-stu-id="3dd74-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="3dd74-118">Découpage de l’interface utilisateur ou du texte par d’autres éléments d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3dd74-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="3dd74-119">Tailles de police incohérentes</span><span class="sxs-lookup"><span data-stu-id="3dd74-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="3dd74-120">Interfaces utilisateur hors écran</span><span class="sxs-lookup"><span data-stu-id="3dd74-120">Off-screen UIs</span></span>
-   <span data-ttu-id="3dd74-121">Flou du texte ou de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3dd74-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="3dd74-122">Opérations de glisser-déplacer ou autres entrées rompues</span><span class="sxs-lookup"><span data-stu-id="3dd74-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="3dd74-123">Rendu partiel des applications DX plein écran</span><span class="sxs-lookup"><span data-stu-id="3dd74-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="3dd74-124">Solution</span><span class="sxs-lookup"><span data-stu-id="3dd74-124">Solution</span></span>

<span data-ttu-id="3dd74-125">Pour que vos applications prennent en charge DPI :</span><span class="sxs-lookup"><span data-stu-id="3dd74-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="3dd74-126">Effectuez une série de tests fonctionnels de haut niveau, y compris l’installation et la désinstallation, aux paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="3dd74-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="3dd74-127">Paramètre</span><span class="sxs-lookup"><span data-stu-id="3dd74-127">Setting</span></span>                                              | <span data-ttu-id="3dd74-128">Éléments à rechercher</span><span class="sxs-lookup"><span data-stu-id="3dd74-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="3dd74-129">1024x768 @ 120 ppp (125% de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="3dd74-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="3dd74-130">Il s’agit d’une résolution efficace de ~ 800x600, donc recherchez l’interface utilisateur découpée des problèmes d’écran ou de disposition.</span><span class="sxs-lookup"><span data-stu-id="3dd74-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="3dd74-131">Recherchez également les bitmaps pixelisée & icônes.</span><span class="sxs-lookup"><span data-stu-id="3dd74-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="3dd74-132">1600 x 1200 @144 (150% de mise à l’échelle)</span><span class="sxs-lookup"><span data-stu-id="3dd74-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="3dd74-133">Interface utilisateur floue.</span><span class="sxs-lookup"><span data-stu-id="3dd74-133">Blurry UI.</span></span> <span data-ttu-id="3dd74-134">Vérifiez que toutes les opérations de la souris fonctionnent, en particulier faire glisser & opérations de déplacement.</span><span class="sxs-lookup"><span data-stu-id="3dd74-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="3dd74-135">Vérifiez également que les modes plein écran fonctionnent correctement.</span><span class="sxs-lookup"><span data-stu-id="3dd74-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="3dd74-136">1600 x 1200 144 ppp avec la virtualisation DPI désactivée</span><span class="sxs-lookup"><span data-stu-id="3dd74-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="3dd74-137">Souvent, les boutons et l’interface utilisateur ne sont pas mis à l’échelle en fonction du texte plus grand & il y a un extrait de texte significatif.</span><span class="sxs-lookup"><span data-stu-id="3dd74-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="3dd74-138">Recherchez les problèmes de disposition en général & pixelisée bitmats & icônes.</span><span class="sxs-lookup"><span data-stu-id="3dd74-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="3dd74-139">Notez tous les problèmes détectés, notamment l’emplacement, la résolution d’écran et les paramètres ppp, ainsi que la façon dont l’application se comporte dans les autres configurations PPP/résolution pour l’exhaustivité</span><span class="sxs-lookup"><span data-stu-id="3dd74-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="3dd74-140">Vérifier chaque problème par rapport aux problèmes courants de codage PPP</span><span class="sxs-lookup"><span data-stu-id="3dd74-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="3dd74-141">Évaluer le coût de la prise en charge de la résolution complète de l’application</span><span class="sxs-lookup"><span data-stu-id="3dd74-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="3dd74-142">Créer une liste des ressources haute résolution requises (par exemple, des boutons, des icônes)</span><span class="sxs-lookup"><span data-stu-id="3dd74-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="3dd74-143">Traiter et corriger la liste des problèmes de résolution détectés à l’étape 1</span><span class="sxs-lookup"><span data-stu-id="3dd74-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="3dd74-144">Intégrer les nouvelles ressources de l’étape 5</span><span class="sxs-lookup"><span data-stu-id="3dd74-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="3dd74-145">Déclarer la prise en charge DPI de votre application</span><span class="sxs-lookup"><span data-stu-id="3dd74-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="3dd74-146">Compatibilité, performances, fiabilité et test d’utilisabilité</span><span class="sxs-lookup"><span data-stu-id="3dd74-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="3dd74-147">Réexécutez l’évaluation de la détection des PPP et vérifiez que les problèmes sont résolus.</span><span class="sxs-lookup"><span data-stu-id="3dd74-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="3dd74-148">Liens vers d’autres ressources</span><span class="sxs-lookup"><span data-stu-id="3dd74-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="3dd74-149">Développement d’applications de bureau haute résolution sur Windows</span><span class="sxs-lookup"><span data-stu-id="3dd74-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="3dd74-150">**Contactez-nous pour obtenir des questions techniques :**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="3dd74-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
