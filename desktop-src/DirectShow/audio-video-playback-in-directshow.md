---
description: Ce didacticiel montre comment écrire une application DirectShow qui lit un fichier multimédia.
ms.assetid: 88f4762a-e6e6-4b1e-9951-a409d9d80da9
title: Lecture audio/vidéo dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca3d681386d85eafc4f32b4e688b920253a51a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516547"
---
# <a name="audiovideo-playback-in-directshow"></a><span data-ttu-id="8de64-103">Lecture audio/vidéo dans DirectShow</span><span class="sxs-lookup"><span data-stu-id="8de64-103">Audio/Video Playback in DirectShow</span></span>

<span data-ttu-id="8de64-104">Ce didacticiel montre comment écrire une application DirectShow qui lit un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="8de64-104">This tutorial shows how to write a DirectShow application that plays a media file.</span></span>

<span data-ttu-id="8de64-105">Avant de lire ce didacticiel, vous souhaiterez peut-être lire les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="8de64-105">Before reading this tutorial, you might want to read the following topics:</span></span>

-   [<span data-ttu-id="8de64-106">Introduction à la programmation d’applications DirectShow</span><span class="sxs-lookup"><span data-stu-id="8de64-106">Introduction to DirectShow Application Programming</span></span>](introduction-to-directshow-application-programming.md)
-   [<span data-ttu-id="8de64-107">Comment lire un fichier</span><span class="sxs-lookup"><span data-stu-id="8de64-107">How To Play a File</span></span>](how-to-play-a-file.md)
-   [<span data-ttu-id="8de64-108">À propos des filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="8de64-108">About DirectShow Filters</span></span>](about-directshow-filters.md)
-   [<span data-ttu-id="8de64-109">À propos du gestionnaire de graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="8de64-109">About the Filter Graph Manager</span></span>](about-the-filter-graph-manager.md)

## <a name="in-this-section"></a><span data-ttu-id="8de64-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8de64-110">In this section</span></span>

-   [<span data-ttu-id="8de64-111">Étape 1 : déclarer la classe DShowPlayer</span><span class="sxs-lookup"><span data-stu-id="8de64-111">Step 1: Declare the DShowPlayer Class</span></span>](step-1--declare-the-dshowplayer-class.md)
-   [<span data-ttu-id="8de64-112">Étape 2 : déclarer CVideoRenderer et les classes dérivées</span><span class="sxs-lookup"><span data-stu-id="8de64-112">Step 2: Declare CVideoRenderer and Derived Classes</span></span>](step-2--declare-cvideorenderer-and-derived-classes.md)
-   [<span data-ttu-id="8de64-113">Étape 3 : générer le graphique de filtre</span><span class="sxs-lookup"><span data-stu-id="8de64-113">Step 3: Build the Filter Graph</span></span>](step-3--build-the-filter-graph.md)
-   [<span data-ttu-id="8de64-114">Étape 4 : ajouter le convertisseur vidéo</span><span class="sxs-lookup"><span data-stu-id="8de64-114">Step 4: Add the Video Renderer</span></span>](step-4--add-the-video-renderer.md)
-   [<span data-ttu-id="8de64-115">Étape 5 : ajouter la fonctionnalité vidéo</span><span class="sxs-lookup"><span data-stu-id="8de64-115">Step 5: Add Video Functionality</span></span>](step-5--add-video-functionality.md)
-   [<span data-ttu-id="8de64-116">Étape 6 : gérer les événements graphiques</span><span class="sxs-lookup"><span data-stu-id="8de64-116">Step 6: Handle Graph Events</span></span>](step-6--handle-graph-events.md)
-   [<span data-ttu-id="8de64-117">Étape 7 : contrôles de transport</span><span class="sxs-lookup"><span data-stu-id="8de64-117">Step 7: Transport Controls</span></span>](step-7--transport-controls.md)
-   [<span data-ttu-id="8de64-118">Exemple de lecture DirectShow</span><span class="sxs-lookup"><span data-stu-id="8de64-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)

## <a name="related-topics"></a><span data-ttu-id="8de64-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8de64-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8de64-120">Utilisation de DirectShow</span><span class="sxs-lookup"><span data-stu-id="8de64-120">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



