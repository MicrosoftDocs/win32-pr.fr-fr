---
title: Pourquoi utiliser DirectComposition
description: Cette rubrique décrit les fonctionnalités et les avantages de Microsoft DirectComposition.
ms.assetid: D597E737-24A1-49E9-8861-9DDD6D7FF2F8
keywords:
- Pourquoi utiliser DirectComposition
- raisons d’utiliser DirectComposition
- Fonctionnalités et avantages de DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7ad68f779abc023b7645ed9e66f8af3bf63a140
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513734"
---
# <a name="why-use-directcomposition"></a><span data-ttu-id="2ae23-106">Pourquoi utiliser DirectComposition ?</span><span class="sxs-lookup"><span data-stu-id="2ae23-106">Why use DirectComposition?</span></span>

> [!NOTE]
> <span data-ttu-id="2ae23-107">Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="2ae23-107">For apps on Windows 10, we recommend using Windows.UI.Composition APIs instead of DirectComposition.</span></span> <span data-ttu-id="2ae23-108">Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).</span><span class="sxs-lookup"><span data-stu-id="2ae23-108">For more info, see [Modernize your desktop app using the Visual layer](/windows/uwp/composition/visual-layer-in-desktop-apps).</span></span>

<span data-ttu-id="2ae23-109">Cette rubrique décrit les fonctionnalités et les avantages de Microsoft DirectComposition.</span><span class="sxs-lookup"><span data-stu-id="2ae23-109">This topic describes the capabilities and benefits of Microsoft DirectComposition.</span></span> <span data-ttu-id="2ae23-110">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ae23-110">It contains the following sections:</span></span>

-   [<span data-ttu-id="2ae23-111">Créer une interface utilisateur attrayante</span><span class="sxs-lookup"><span data-stu-id="2ae23-111">Create a visually engaging user interface</span></span>](#create-a-visually-engaging-user-interface)
-   [<span data-ttu-id="2ae23-112">Activer des animations riches et lisses pour votre application</span><span class="sxs-lookup"><span data-stu-id="2ae23-112">Enable rich, smooth animations for your application</span></span>](#enable-rich-smooth-animations-for-your-application)
-   [<span data-ttu-id="2ae23-113">Combiner des bitmaps de diverses sources</span><span class="sxs-lookup"><span data-stu-id="2ae23-113">Combine bitmaps from a variety of sources</span></span>](#combine-bitmaps-from-a-variety-of-sources)
-   [<span data-ttu-id="2ae23-114">Économies de mémoire grâce à l’intégration avec DWM</span><span class="sxs-lookup"><span data-stu-id="2ae23-114">Memory savings though integration with DWM</span></span>](#memory-savings-though-integration-with-dwm)
-   [<span data-ttu-id="2ae23-115">Conserver ce que vous avez déjà</span><span class="sxs-lookup"><span data-stu-id="2ae23-115">Keep what you already have</span></span>](#keep-what-you-already-have)
-   [<span data-ttu-id="2ae23-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ae23-116">Related topics</span></span>](#related-topics)

## <a name="create-a-visually-engaging-user-interface"></a><span data-ttu-id="2ae23-117">Créer une interface utilisateur attrayante</span><span class="sxs-lookup"><span data-stu-id="2ae23-117">Create a visually engaging user interface</span></span>

<span data-ttu-id="2ae23-118">DirectComposition vous permet de combiner et d’animer des éléments [*visuels*](directcomposition-glossary.md) pour créer une interface utilisateur visuellement attrayante pour vos applications Windows.</span><span class="sxs-lookup"><span data-stu-id="2ae23-118">DirectComposition lets you combine and animate [*visuals*](directcomposition-glossary.md) to create a visually engaging UI for your Windows-based applications.</span></span> <span data-ttu-id="2ae23-119">Il peut vous aider à donner à votre application une apparence unique, en établissant une identité qui la distingue des autres applications.</span><span class="sxs-lookup"><span data-stu-id="2ae23-119">It can help give your application a unique look and feel, establishing an identity that sets it apart from other applications.</span></span>

<span data-ttu-id="2ae23-120">DirectComposition peut également aider à faciliter l’utilisation de vos applications.</span><span class="sxs-lookup"><span data-stu-id="2ae23-120">DirectComposition can also help make your applications easier to use.</span></span> <span data-ttu-id="2ae23-121">Par exemple, vous pouvez l’utiliser pour créer des signaux visuels et des transitions d’écran animées qui montrent les relations entre les différents éléments à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2ae23-121">For example, you can use it to create visual cues and animated screen transitions that show relationships among items on the screen.</span></span>

## <a name="enable-rich-smooth-animations-for-your-application"></a><span data-ttu-id="2ae23-122">Activer des animations riches et lisses pour votre application</span><span class="sxs-lookup"><span data-stu-id="2ae23-122">Enable rich, smooth animations for your application</span></span>

<span data-ttu-id="2ae23-123">DirectComposition est un moteur de composition bitmap à hautes performances qui utilise des graphiques accélérés par le matériel pour obtenir des fréquences d’images élevées, ce qui permet de lisser et de contourner le panoramique, le défilement et les animations de contenu complexe.</span><span class="sxs-lookup"><span data-stu-id="2ae23-123">DirectComposition is a high-performance bitmap composition engine that uses hardware-accelerated graphics to achieve high frame rates, resulting in smooth and consistent panning, scrolling, and animations of complex content.</span></span> <span data-ttu-id="2ae23-124">Étant donné qu’il opère sur un thread dédié distinct du thread utilisé pour le rendu de l’interface utilisateur de l’application, DirectComposition ne peut jamais « priver » le thread d’interface utilisateur ou interférer avec la capacité de l’application à dessiner ses éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ae23-124">Because it operates on a dedicated thread that is separate from the thread used to render the application UI, DirectComposition can never "starve" the UI thread or interfere with the application's ability to draw its UI elements.</span></span>

## <a name="combine-bitmaps-from-a-variety-of-sources"></a><span data-ttu-id="2ae23-125">Combiner des bitmaps de diverses sources</span><span class="sxs-lookup"><span data-stu-id="2ae23-125">Combine bitmaps from a variety of sources</span></span>

<span data-ttu-id="2ae23-126">De nombreuses applications basées sur Windows ont une interface utilisateur qui se compose d’éléments créés par différents frameworks graphiques.</span><span class="sxs-lookup"><span data-stu-id="2ae23-126">Many Windows-based applications have a UI that consists of elements created by a variety of different graphics frameworks.</span></span> <span data-ttu-id="2ae23-127">Par exemple, une application peut utiliser Windows Forms pour créer une barre d’État, GDI (Windows Graphics Device Interface) pour créer le contenu de la fenêtre principale, Microsoft DirectX pour le contenu graphique, etc.</span><span class="sxs-lookup"><span data-stu-id="2ae23-127">For example, an application might use Windows Forms to create a status bar, Windows Graphics Device Interface (GDI) to create the main window content, Microsoft DirectX for graphics content, and so on.</span></span> <span data-ttu-id="2ae23-128">DirectComposition vous permet de combiner le contenu de diverses infrastructures graphiques et de l’afficher dans la même fenêtre de niveau supérieur ou enfant sans avoir à vous soucier de ce qui se passe si le contenu de différents frameworks chevauche.</span><span class="sxs-lookup"><span data-stu-id="2ae23-128">DirectComposition enables you to combine the content from a variety of graphics frameworks and have it render to the same top-level or child window without needing to worry about what happens if the content from different frameworks overlaps.</span></span>

## <a name="memory-savings-though-integration-with-dwm"></a><span data-ttu-id="2ae23-129">Économies de mémoire grâce à l’intégration avec DWM</span><span class="sxs-lookup"><span data-stu-id="2ae23-129">Memory savings though integration with DWM</span></span>

<span data-ttu-id="2ae23-130">Les compositions et les animations créées par DirectComposition sont passées à un composant intégré de Windows appelé [Gestionnaire de fenêtrage (DWM)](/windows/desktop/dwm/dwm-overview) pour le rendu à l’écran.</span><span class="sxs-lookup"><span data-stu-id="2ae23-130">Compositions and animations created by DirectComposition are passed to a built-in component of Windows called [Desktop Window Manager (DWM)](/windows/desktop/dwm/dwm-overview) for rendering to the screen.</span></span> <span data-ttu-id="2ae23-131">Par conséquent, aucun composant de rendu spécial ou infrastructure d’interface utilisateur n’est requis sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="2ae23-131">Therefore, no special rendering components or UI frameworks are required on the computer.</span></span>

## <a name="keep-what-you-already-have"></a><span data-ttu-id="2ae23-132">Conserver ce que vous avez déjà</span><span class="sxs-lookup"><span data-stu-id="2ae23-132">Keep what you already have</span></span>

<span data-ttu-id="2ae23-133">Le code d’interface utilisateur d’une application Windows existante représente un investissement significatif.</span><span class="sxs-lookup"><span data-stu-id="2ae23-133">The UI code in an existing Windows-based application represents a significant investment.</span></span> <span data-ttu-id="2ae23-134">Pour l’essentiel, DirectComposition vous permet de composer et d’animer le contenu existant de votre interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ae23-134">For the most part, DirectComposition lets you compose and animate your existing UI content.</span></span> <span data-ttu-id="2ae23-135">Cela signifie que vous pouvez utiliser DirectComposition pour effectuer des mises à jour et des améliorations significatives de l’interface utilisateur de votre application sans avoir à apporter de modifications importantes à votre base de code d’interface utilisateur existante.</span><span class="sxs-lookup"><span data-stu-id="2ae23-135">This means you can use DirectComposition to make significant updates and enhancements to your application UI without needing to make extensive changes to your existing UI code base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ae23-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ae23-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ae23-137">DirectComposition</span><span class="sxs-lookup"><span data-stu-id="2ae23-137">DirectComposition</span></span>](directcomposition-portal.md)
</dt> </dl>

 

 