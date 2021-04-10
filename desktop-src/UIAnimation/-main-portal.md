---
title: Gestionnaire d’animations Windows
description: Le gestionnaire d’animations Windows (animation Windows) permet une animation détaillée des éléments d’interface utilisateur.
ms.assetid: 1d840263-d9da-4cab-9bc3-0c143c9c8741
keywords:
- Animation Windows Animation Windows, portail
- Windows animation Manager Windows animation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d274b9f2d5e386fbe01c2caeb9e1e65ddbdc73f3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941113"
---
# <a name="windows-animation-manager"></a><span data-ttu-id="071dd-105">Gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="071dd-105">Windows Animation Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="071dd-106">Objectif</span><span class="sxs-lookup"><span data-stu-id="071dd-106">Purpose</span></span>

<span data-ttu-id="071dd-107">Le gestionnaire d’animations Windows (animation Windows) permet une animation détaillée des éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="071dd-107">The Windows Animation Manager (Windows Animation) enables rich animation of user interface elements.</span></span> <span data-ttu-id="071dd-108">Il est conçu pour simplifier le processus d’ajout d’animation à l’interface utilisateur d’une application et pour permettre aux développeurs d’implémenter des animations lisses, naturelles et interactives.</span><span class="sxs-lookup"><span data-stu-id="071dd-108">It is designed to simplify the process of adding animation to an application's user interface and to enable developers to implement animations that are smooth, natural, and interactive.</span></span>

<span data-ttu-id="071dd-109">L’infrastructure d’animation gère la planification et l’exécution des animations.</span><span class="sxs-lookup"><span data-stu-id="071dd-109">The animation framework manages the scheduling and execution of animations.</span></span> <span data-ttu-id="071dd-110">Il fournit une bibliothèque de fonctions mathématiques utiles pour spécifier le comportement d’un élément d’interface utilisateur au fil du temps, et permet également aux développeurs d’implémenter des fonctions personnalisées qui fournissent des comportements supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="071dd-110">It supplies a library of useful mathematical functions for specifying the behavior of a UI element over time, and also enables developers to implement custom functions that provide additional behaviors.</span></span>

<span data-ttu-id="071dd-111">L’animation Windows n’effectue pas le rendu ; Il peut être utilisé avec n’importe quelle plateforme graphique, y compris Direct2D, Direct3D ou GDI+.</span><span class="sxs-lookup"><span data-stu-id="071dd-111">Windows Animation does not perform the rendering; it can be used with any graphics platform, including Direct2D, Direct3D, or GDI+.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="071dd-112">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="071dd-112">In this section</span></span>



| <span data-ttu-id="071dd-113">Rubrique</span><span class="sxs-lookup"><span data-stu-id="071dd-113">Topic</span></span>                                                                                   | <span data-ttu-id="071dd-114">Description</span><span class="sxs-lookup"><span data-stu-id="071dd-114">Description</span></span>                                                                                                                                       |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="071dd-115">Guide de développement d’animation Windows</span><span class="sxs-lookup"><span data-stu-id="071dd-115">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)<br/> | <span data-ttu-id="071dd-116">Le Guide du développeur fournit une vue d’ensemble de l’animation Windows et fournit un exemple de code qui couvre les tâches de base de l’animation.</span><span class="sxs-lookup"><span data-stu-id="071dd-116">The developer guide provides an overview of Windows Animation and provides sample code that covers the basic animation tasks.</span></span><br/>          |
| [<span data-ttu-id="071dd-117">Informations de référence sur les animations Windows</span><span class="sxs-lookup"><span data-stu-id="071dd-117">Windows Animation Reference</span></span>](windows-animation-reference.md)<br/>               | <span data-ttu-id="071dd-118">Les rubriques contenues dans cette section fournissent les spécifications de référence du gestionnaire d’animations Windows.</span><span class="sxs-lookup"><span data-stu-id="071dd-118">The topics contained in this section provide the reference specifications for the Windows Animation Manager.</span></span><br/>                           |
| [<span data-ttu-id="071dd-119">Exemples d’animation Windows</span><span class="sxs-lookup"><span data-stu-id="071dd-119">Windows Animation Samples</span></span>](windows-animation-samples.md)<br/>                   | <span data-ttu-id="071dd-120">Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation du gestionnaire d’animations Windows.</span><span class="sxs-lookup"><span data-stu-id="071dd-120">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span> <br/> |
| [<span data-ttu-id="071dd-121">Glossaire Windows animation</span><span class="sxs-lookup"><span data-stu-id="071dd-121">Windows Animation Glossary</span></span>](-ui-animation-glossary.md)<br/>                     | <span data-ttu-id="071dd-122">Ce glossaire contient des termes et des acronymes intéressants pour les développeurs qui utilisent le gestionnaire d’animations Windows.</span><span class="sxs-lookup"><span data-stu-id="071dd-122">This glossary contains terms and acronyms of interest to developers using the Windows Animation Manager.</span></span><br/>                               |



 

## <a name="developer-audience"></a><span data-ttu-id="071dd-123">Développeurs concernés</span><span class="sxs-lookup"><span data-stu-id="071dd-123">Developer audience</span></span>

<span data-ttu-id="071dd-124">L’animation Windows est conçue pour être utilisée par les développeurs C/C++ expérimentés qui connaissent COM, les concepts de programmation de l’interface utilisateur et les concepts d’animation généraux.</span><span class="sxs-lookup"><span data-stu-id="071dd-124">Windows Animation is designed for use by experienced C/C++ developers who are familiar with COM, UI programming concepts, and general animation concepts.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="071dd-125">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="071dd-125">Run-time requirements</span></span>

<span data-ttu-id="071dd-126">Le gestionnaire d’animations Windows a été introduit dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="071dd-126">The Windows Animation Manager was introduced in Windows 7.</span></span>

<span data-ttu-id="071dd-127">Les applications qui requièrent la prise en charge du gestionnaire d’animations Windows sur Windows Vista peuvent utiliser la mise à jour de la plateforme pour Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="071dd-127">Applications that require support for Windows Animation Manager on Windows Vista can utilize the Platform Update for Windows Vista.</span></span> <span data-ttu-id="071dd-128">Les applications qui requièrent une mise à jour de plateforme pour Windows Vista peuvent avoir des Windows Update vérifier qu’elles sont installées, ou les télécharger et les installer en arrière-plan dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="071dd-128">Applications that require Platform Update for Windows Vista can have Windows Update verify that it is installed, or download and install it in the background otherwise.</span></span> <span data-ttu-id="071dd-129">Pour plus d’informations, consultez à propos de la [mise à jour de plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span><span class="sxs-lookup"><span data-stu-id="071dd-129">For more information, see [About Platform Update for Windows Vista](../win7ip/platform-update-for-windows-vista-overview.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="071dd-130">Ressources supplémentaires</span><span class="sxs-lookup"><span data-stu-id="071dd-130">Additional resources</span></span>

-   <span data-ttu-id="071dd-131">[Vue d’ensemble de l’Animation Windows Scenic](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (vidéo)</span><span class="sxs-lookup"><span data-stu-id="071dd-131">[Windows Scenic Animation Overview](https://channel9.msdn.com/blogs/yochay/windows-scenic-animation-overview) (video)</span></span>
-   <span data-ttu-id="071dd-132">[À l’intérieur de Windows 7 : présentation approfondie du gestionnaire d’animations](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (vidéo)</span><span class="sxs-lookup"><span data-stu-id="071dd-132">[Inside Windows 7: Animation Manager Deep Dive and Tutorial](https://channel9.msdn.com/blogs/yochay/inside-windows-7-animation-manager-deep-dive) (video)</span></span>
-   <span data-ttu-id="071dd-133">[Animation Windows-rubriques avancées](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (vidéo)</span><span class="sxs-lookup"><span data-stu-id="071dd-133">[Windows Animation - Advanced Topics](https://channel9.msdn.com/posts/yochay/Windows-Animation-Advance-Topics/) (video)</span></span>
-   [<span data-ttu-id="071dd-134">Exemple de code du gestionnaire d’animations Windows</span><span class="sxs-lookup"><span data-stu-id="071dd-134">Windows Animation Manager Sample Code</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DirectCompositionWindowsAnimationManager)

## <a name="related-topics"></a><span data-ttu-id="071dd-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="071dd-135">Related topics</span></span>

[<span data-ttu-id="071dd-136">Vue d’ensemble de l’animation (.NET Framework)</span><span class="sxs-lookup"><span data-stu-id="071dd-136">Animation Overview (.NET Framework)</span></span>](/dotnet/framework/wpf/graphics-multimedia/animation-overview)