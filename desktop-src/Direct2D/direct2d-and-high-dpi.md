---
title: Direct2D et haute résolution
description: Décrit comment Direct2D prend en charge l’affichage haute résolution.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, haute résolution
- haute résolution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941310"
---
# <a name="direct2d-and-high-dpi"></a><span data-ttu-id="1a798-105">Direct2D et haute résolution</span><span class="sxs-lookup"><span data-stu-id="1a798-105">Direct2D and High-DPI</span></span>

<span data-ttu-id="1a798-106">L’écriture d’une application prenant en charge DPI est la clé de l’affichage d’une interface utilisateur de manière cohérente sur un large éventail de paramètres d’affichage haute résolution.</span><span class="sxs-lookup"><span data-stu-id="1a798-106">Writing a DPI-aware application is the key to making a user interface (UI) look consistently good across a wide variety of high-DPI display settings.</span></span> <span data-ttu-id="1a798-107">Une application qui n’a pas de prise en charge DPI mais qui s’exécute sur un paramètre d’affichage haute résolution peut être affectée par un grand nombre d’artefacts visuels, y compris une mise à l’échelle incorrecte des éléments d’interface utilisateur, du texte tronqué et des images floues.</span><span class="sxs-lookup"><span data-stu-id="1a798-107">An application that is not DPI-aware but is running on a high-DPI display setting can suffer from many visual artifacts, including incorrect scaling of UI elements, clipped text, and blurry images.</span></span> <span data-ttu-id="1a798-108">En ajoutant la prise en charge dans votre application pour la reconnaissance DPI, vous rendez la présentation de l’interface utilisateur de votre application plus prévisible, ce qui rend plus attrayant et plus facile à lire pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="1a798-108">By adding support in your application for DPI-awareness, you make the presentation of your application's UI more predictable, making it more visually appealing and easier to read for users.</span></span> <span data-ttu-id="1a798-109">Heureusement, Direct2D facilite plus que jamais l’écriture d’applications qui fonctionnent correctement dans la haute résolution.</span><span class="sxs-lookup"><span data-stu-id="1a798-109">Fortunately, Direct2D makes it easier than ever to write applications that work well in high-DPI.</span></span> <span data-ttu-id="1a798-110">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="1a798-110">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="1a798-111">Prise en charge de la haute résolution dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="1a798-111">High-DPI Support in Direct2D</span></span>](#high-dpi-support-in-direct2d)
-   [<span data-ttu-id="1a798-112">Windows 8 et haute résolution</span><span class="sxs-lookup"><span data-stu-id="1a798-112">Windows 8 and High-DPI</span></span>](#windows-8-and-high-dpi)
-   [<span data-ttu-id="1a798-113">Qu’est-ce qu’une DIP ?</span><span class="sxs-lookup"><span data-stu-id="1a798-113">What is a DIP?</span></span>](#what-is-a-dip)
-   [<span data-ttu-id="1a798-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a798-114">Related topics</span></span>](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a><span data-ttu-id="1a798-115">Prise en charge de la haute résolution dans Direct2D</span><span class="sxs-lookup"><span data-stu-id="1a798-115">High-DPI Support in Direct2D</span></span>

<span data-ttu-id="1a798-116">Direct2D fournit les fonctionnalités suivantes pour l’utilisation de scénarios haute résolution :</span><span class="sxs-lookup"><span data-stu-id="1a798-116">Direct2D provides the following features for working with high-DPI scenarios:</span></span>

-   <span data-ttu-id="1a798-117">Il honore automatiquement la résolution du système en cas de création d’une cible de rendu avec fenêtres, tant que le manifeste d’application indique que l’application gère correctement DPI.</span><span class="sxs-lookup"><span data-stu-id="1a798-117">It automatically honors the system DPI when creating a windowed render target, so long as the application manifest indicates that the application handles DPI correctly.</span></span> <span data-ttu-id="1a798-118">(Pour plus d’informations sur la façon de déclarer que votre application prend en charge DPI, consultez [Comment garantir que votre application s’affiche correctement sur les affichages haute résolution](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span><span class="sxs-lookup"><span data-stu-id="1a798-118">(For information on how to declare that your application is DPI-aware, see [How to Ensure That Your Application Displays Properly on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)</span></span>
-   <span data-ttu-id="1a798-119">Il exprime les coordonnées en DIP (Device Independent Pixel), ce qui permet à l’application de se mettre à l’échelle automatiquement lorsque le paramètre DPI change.</span><span class="sxs-lookup"><span data-stu-id="1a798-119">It expresses coordinates in DIPs (Device Independent Pixels), which enables the application to scale automatically when the DPI setting changes.</span></span>
-   <span data-ttu-id="1a798-120">Il permet aux bitmaps d’avoir un PPP et de les mettre correctement à l’échelle en tenant compte des PPP.</span><span class="sxs-lookup"><span data-stu-id="1a798-120">It enables bitmaps to have a DPI and correctly scales them by taking the DPI into account.</span></span> <span data-ttu-id="1a798-121">Cette fonctionnalité peut également être utilisée pour gérer les icônes à des résolutions différentes.</span><span class="sxs-lookup"><span data-stu-id="1a798-121">This feature can also be used to maintain icons at different resolutions.</span></span>
-   <span data-ttu-id="1a798-122">Il exprime la plupart des ressources dans des DIP, ce qui rend les ressources automatiquement indépendantes de la résolution.</span><span class="sxs-lookup"><span data-stu-id="1a798-122">It expresses most resources in DIPs, which makes the resources automatically independent of resolution.</span></span>
-   <span data-ttu-id="1a798-123">Il utilise un espace de coordonnées à virgule flottante et un anticrénelage, de sorte que tout contenu peut être mis à l’échelle en PPP arbitraire.</span><span class="sxs-lookup"><span data-stu-id="1a798-123">It uses a floating-point coordinate space and antialiasing, so any content can be scaled to any arbitrary DPI.</span></span>

<span data-ttu-id="1a798-124">Le pipeline graphique Direct2D est conçu pour évoluer de 96 PPP à 1200DPI.</span><span class="sxs-lookup"><span data-stu-id="1a798-124">The Direct2D graphics pipeline is designed to scale from 96 DPI to 1200DPI.</span></span>

## <a name="windows-8-and-high-dpi"></a><span data-ttu-id="1a798-125">Windows 8 et haute résolution</span><span class="sxs-lookup"><span data-stu-id="1a798-125">Windows 8 and High-DPI</span></span>

<span data-ttu-id="1a798-126">À compter de Windows 8, il existe des fonctionnalités supplémentaires pour la prise en charge de la haute résolution.</span><span class="sxs-lookup"><span data-stu-id="1a798-126">Starting with Windows 8, there are additional features for high-DPI support.</span></span>

<span data-ttu-id="1a798-127">Si le contexte de périphérique PPP est suffisamment élevé, Direct2D modifie le seuil qu’il utilise pour activer l’anticrénelage vertical du texte.</span><span class="sxs-lookup"><span data-stu-id="1a798-127">If the device context DPI is high enough, Direct2D changes the threshold it uses to enable vertical antialiasing of text.</span></span> <span data-ttu-id="1a798-128">Cela aboutit à un rendu de texte plus rapide sur les affichages haute résolution.</span><span class="sxs-lookup"><span data-stu-id="1a798-128">This results in faster text rendering on high-DPI displays.</span></span> <span data-ttu-id="1a798-129">En outre, vous pouvez basculer le mode d’unité sur les pixels au lieu de DIP à l’aide de la méthode [**ID2D1DeviceContext :: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="1a798-129">Additionally, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span> <span data-ttu-id="1a798-130">Si vous définissez le mode d’unité sur pixels et le contexte de périphérique sur la résolution d’écran, l’optimisation est toujours activée.</span><span class="sxs-lookup"><span data-stu-id="1a798-130">If you set the unit mode to pixels and the device context DPI to the screen DPI, the optimization is still enabled.</span></span>

## <a name="what-is-a-dip"></a><span data-ttu-id="1a798-131">Qu’est-ce qu’une DIP ?</span><span class="sxs-lookup"><span data-stu-id="1a798-131">What is a DIP?</span></span>

<span data-ttu-id="1a798-132">Un DIP (Device Independent Pixel) est un pixel logique qui correspond aux pixels de l’appareil physique via une valeur scalaire, la valeur PPP.</span><span class="sxs-lookup"><span data-stu-id="1a798-132">A device independent pixel (DIP) is a logical pixel that maps to the pixels of the physical device through a scalar, the DPI.</span></span> <span data-ttu-id="1a798-133">PPP correspond aux points par pouce, où un point représente un pixel de l’appareil physique.</span><span class="sxs-lookup"><span data-stu-id="1a798-133">DPI stands for dots per inch, where a dot represents a physical device pixel.</span></span> <span data-ttu-id="1a798-134">(La nomenclature provient de l’impression, où les points sont le plus petit point d’encre qu’un processus d’impression peut produire).</span><span class="sxs-lookup"><span data-stu-id="1a798-134">(The nomenclature comes from printing, where dots are the smallest ink dot that a printing process can produce).</span></span> <span data-ttu-id="1a798-135">Comme un moniteur standard est utilisé pour 96 points par pouce, une résolution de 96 signifiait qu’un DIP (Device Independent Pixel) soit mappé 1:1 avec un pixel physique.</span><span class="sxs-lookup"><span data-stu-id="1a798-135">Because a standard monitor used to have 96 dots per inch, a DPI of 96 meant that a device independent pixel (or DIP) mapped 1:1 with a physical pixel.</span></span> <span data-ttu-id="1a798-136">Par exemple, si les PPP étaient 96 \* 2 = 192, un DIP unique englobe deux pixels physiques.</span><span class="sxs-lookup"><span data-stu-id="1a798-136">For example, if the DPI were 96\*2 = 192, then a single DIP would encompass two physical pixels.</span></span>

<span data-ttu-id="1a798-137">Il existe de nombreuses raisons pour lesquelles les applications ne gèrent pas nécessairement cette mise à l’échelle correctement. l’une des raisons les plus simples est qu’elle nécessite un travail supplémentaire pour découvrir et utiliser cette valeur scalaire lors du rendu.</span><span class="sxs-lookup"><span data-stu-id="1a798-137">There are many reasons why applications don't necessarily handle this scaling correctly; one of the simplest reasons is that it requires extra work to discover and use this scalar value when rendering.</span></span> <span data-ttu-id="1a798-138">Dans Direct2D, la mise à l’échelle est appliquée par défaut.</span><span class="sxs-lookup"><span data-stu-id="1a798-138">In Direct2D, the scaling is applied by default.</span></span> <span data-ttu-id="1a798-139">En raison de ce mappage, les pixels de l’appareil physique peuvent finir par des coordonnées DIP fractionnaires, ce qui est l’une des raisons pour lesquelles Direct2D utilise un espace de coordonnées à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="1a798-139">Because of this mapping, physical device pixels might end up at fractional DIP coordinates, which is one of the reasons why Direct2D uses a floating-point coordinate space.</span></span>

<dl> <span data-ttu-id="1a798-140">Pixel physique = (DIP × DPI)/96</span><span class="sxs-lookup"><span data-stu-id="1a798-140">physical pixel = (dip × DPI) / 96</span></span>  
</dl>

<span data-ttu-id="1a798-141">Pour convertir un pixel physique en DIP, utilisez la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="1a798-141">To convert a physical pixel to a DIP, use this formula:</span></span>

<dl> <span data-ttu-id="1a798-142">DIP = (pixel physique × 96)/ppp</span><span class="sxs-lookup"><span data-stu-id="1a798-142">dip = (physical pixel × 96) / DPI</span></span>  
</dl>

> [!Note]
>
> <span data-ttu-id="1a798-143">À compter de Windows 8, vous pouvez basculer le mode d’unité sur les pixels au lieu de DIP à l’aide de la méthode [**ID2D1DeviceContext :: SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) .</span><span class="sxs-lookup"><span data-stu-id="1a798-143">Starting with Windows 8, you can switch the unit mode to pixels instead of DIPs using the [**ID2D1DeviceContext::SetUnitMode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) method.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1a798-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1a798-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a798-145">Comment garantir que votre application s’affiche correctement sur les affichages haute résolution</span><span class="sxs-lookup"><span data-stu-id="1a798-145">How to Ensure That Your Application Displays Properly on High-DPI Displays</span></span>](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 