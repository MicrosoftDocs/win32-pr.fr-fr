---
title: Exemples d’animation Windows
description: Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation du gestionnaire d’animations Windows.
ms.assetid: 33b1770a-5acb-4ab5-999c-9663f4c075f0
keywords:
- Animation Windows Animation Windows, exemples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c2fe31e7fa12feab010bec3da710d4b2b80dd1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310862"
---
# <a name="windows-animation-samples"></a><span data-ttu-id="973dd-104">Exemples d’animation Windows</span><span class="sxs-lookup"><span data-stu-id="973dd-104">Windows Animation Samples</span></span>

<span data-ttu-id="973dd-105">Les rubriques contenues dans cette section fournissent des détails sur les exemples de code qui prennent en charge la documentation du gestionnaire d’animations Windows.</span><span class="sxs-lookup"><span data-stu-id="973dd-105">The topics contained in this section provide details about the code samples that support the Windows Animation Manager documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="973dd-106">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="973dd-106">In this section</span></span>



| <span data-ttu-id="973dd-107">Rubrique</span><span class="sxs-lookup"><span data-stu-id="973dd-107">Topic</span></span>                                                                                     | <span data-ttu-id="973dd-108">Description</span><span class="sxs-lookup"><span data-stu-id="973dd-108">Description</span></span>                                                                                                         |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="973dd-109">Exemple d’animation pilotée par les applications</span><span class="sxs-lookup"><span data-stu-id="973dd-109">Application-Driven Animation Sample</span></span>](application-driven-animation-sample.md)<br/> |                                                                                                                     |
| [<span data-ttu-id="973dd-110">Exemple d’animation pilotée par minuterie</span><span class="sxs-lookup"><span data-stu-id="973dd-110">Timer-Driven Animation Sample</span></span>](timer-driven-animation-sample.md)<br/>             |                                                                                                                     |
| [<span data-ttu-id="973dd-111">Exemple d’interpolateur personnalisé</span><span class="sxs-lookup"><span data-stu-id="973dd-111">Custom Interpolator Sample</span></span>](custom-interpolator-sample.md)<br/>                   | <span data-ttu-id="973dd-112">Montre comment utiliser l’animation Windows avec votre propre interpolateur personnalisé, avec Direct2D utilisé pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="973dd-112">Shows how to use Windows Animation with your own Custom Interpolator, with Direct2D used for rendering.</span></span> <br/> |
| [<span data-ttu-id="973dd-113">Exemple de disposition en grille</span><span class="sxs-lookup"><span data-stu-id="973dd-113">Grid Layout Sample</span></span>](grid-layout-sample.md)<br/>                                   | <span data-ttu-id="973dd-114">Montre comment utiliser l’animation Windows, à l’aide de Direct2D pour animer une grille d’images.</span><span class="sxs-lookup"><span data-stu-id="973dd-114">Shows how to use Windows Animation, using Direct2D to animate a grid of images.</span></span> <br/>                         |
| [<span data-ttu-id="973dd-115">Exemple de comparaison de priorité</span><span class="sxs-lookup"><span data-stu-id="973dd-115">Priority Comparison Sample</span></span>](priority-comparison-sample.md)<br/>                   | <span data-ttu-id="973dd-116">Montre comment utiliser l’animation Windows avec votre propre comparaison de priorité, à l’aide de Direct2D pour le rendu.</span><span class="sxs-lookup"><span data-stu-id="973dd-116">Shows how to use Windows Animation with your own Priority Comparison, using Direct2D for rendering.</span></span><br/>      |



 

## <a name="sample-files"></a><span data-ttu-id="973dd-117">Fichiers exemples</span><span class="sxs-lookup"><span data-stu-id="973dd-117">Sample Files</span></span>

<span data-ttu-id="973dd-118">Chaque exemple contient un grand nombre des fichiers de clé suivants :</span><span class="sxs-lookup"><span data-stu-id="973dd-118">Each sample contains many of the following key files:</span></span>

<dl> <dt>

<span data-ttu-id="973dd-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application. cpp</span><span class="sxs-lookup"><span data-stu-id="973dd-119"><span id="Application.cpp"></span><span id="application.cpp"></span><span id="APPLICATION.CPP"></span>Application.cpp</span></span>
</dt> <dd>

<span data-ttu-id="973dd-120">Définit le point d’entrée de l’application.</span><span class="sxs-lookup"><span data-stu-id="973dd-120">Defines the application entry point.</span></span>

</dd> <dt>

<span data-ttu-id="973dd-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow. h</span><span class="sxs-lookup"><span data-stu-id="973dd-121"><span id="MainWindow.h"></span><span id="mainwindow.h"></span><span id="MAINWINDOW.H"></span>MainWindow.h</span></span>
</dt> <dd>

<span data-ttu-id="973dd-122">Déclare la classe CMainWindow.</span><span class="sxs-lookup"><span data-stu-id="973dd-122">Declares the CMainWindow class.</span></span>

</dd> <dt>

<span data-ttu-id="973dd-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow. cpp</span><span class="sxs-lookup"><span data-stu-id="973dd-123"><span id="MainWindow.cpp"></span><span id="mainwindow.cpp"></span><span id="MAINWINDOW.CPP"></span>MainWindow.cpp</span></span>
</dt> <dd>

<span data-ttu-id="973dd-124">Initialise les composants d’animation et la plateforme graphique, charge les images et restitue la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="973dd-124">Initializes the animation components and the graphics platform, loads images, and renders the client area.</span></span>

</dd> <dt>

<span data-ttu-id="973dd-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager. h</span><span class="sxs-lookup"><span data-stu-id="973dd-125"><span id="LayoutManager.h"></span><span id="layoutmanager.h"></span><span id="LAYOUTMANAGER.H"></span>LayoutManager.h</span></span>
</dt> <dd>

<span data-ttu-id="973dd-126">Déclare la classe CLayoutManager.</span><span class="sxs-lookup"><span data-stu-id="973dd-126">Declares the CLayoutManager class.</span></span>

</dd> <dt>

<span data-ttu-id="973dd-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager. cpp</span><span class="sxs-lookup"><span data-stu-id="973dd-127"><span id="LayoutManager.cpp"></span><span id="layoutmanager.cpp"></span><span id="LAYOUTMANAGER.CPP"></span>LayoutManager.cpp</span></span>
</dt> <dd>

<span data-ttu-id="973dd-128">Calcule la disposition des images dans la fenêtre principale, crée des storyboards, ajoute des transitions à la table de montage séquentiel et planifie le Storyboard.</span><span class="sxs-lookup"><span data-stu-id="973dd-128">Calculates the layout of images in the main window, creates storyboards, adds transitions to the storyboard, and schedules the storyboard.</span></span>

</dd> <dt>

<span data-ttu-id="973dd-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail. h</span><span class="sxs-lookup"><span data-stu-id="973dd-129"><span id="Thumbnail.h"></span><span id="thumbnail.h"></span><span id="THUMBNAIL.H"></span>Thumbnail.h</span></span>
</dt> <dd>

<span data-ttu-id="973dd-130">Déclare la classe CThumbNail.</span><span class="sxs-lookup"><span data-stu-id="973dd-130">Declares the CThumbNail class.</span></span>

</dd> <dt>

<span data-ttu-id="973dd-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail. cpp</span><span class="sxs-lookup"><span data-stu-id="973dd-131"><span id="Thumbnail.cpp"></span><span id="thumbnail.cpp"></span><span id="THUMBNAIL.CPP"></span>Thumbnail.cpp</span></span>
</dt> <dd>

<span data-ttu-id="973dd-132">Crée des variables d’animation et restitue des miniatures.</span><span class="sxs-lookup"><span data-stu-id="973dd-132">Creates animation variables and renders thumbnails.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="973dd-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="973dd-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="973dd-134">Guide de développement d’animation Windows</span><span class="sxs-lookup"><span data-stu-id="973dd-134">Windows Animation Development Guide</span></span>](windows-animation-developer-guide.md)
</dt> <dt>

[<span data-ttu-id="973dd-135">Informations de référence sur les animations Windows</span><span class="sxs-lookup"><span data-stu-id="973dd-135">Windows Animation Reference</span></span>](windows-animation-reference.md)
</dt> </dl>

 

 





