---
description: Présentation des services de modification DirectShow
ms.assetid: 247c4ba9-53c1-46ed-83ef-a454351920e3
title: Présentation des services de modification DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c75d9cf22eba81ebb9794310f63983b991bcf22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481616"
---
# <a name="introduction-to-directshow-editing-services"></a><span data-ttu-id="cc91a-103">Présentation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="cc91a-103">Introduction to DirectShow Editing Services</span></span>

<span data-ttu-id="cc91a-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="cc91a-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="cc91a-105">Le cœur de DirectShow est une architecture puissante pour gérer le contenu multimédia en continu.</span><span class="sxs-lookup"><span data-stu-id="cc91a-105">The core of DirectShow is a powerful architecture for handling streaming media.</span></span> <span data-ttu-id="cc91a-106">Une application peut l’utiliser pour lire du contenu multimédia créé dans un grand nombre de formats, sans que le développeur ait à se soucier de la compression de fichiers et d’autres détails fastidieux.</span><span class="sxs-lookup"><span data-stu-id="cc91a-106">An application can use it to play multimedia content authored in a wide variety of formats, without the developer needing to worry about file compression and other tedious details.</span></span> <span data-ttu-id="cc91a-107">Avant les [services de modification DirectShow](directshow-editing-services.md) , toutefois, DirectShow n’avait pas la flexibilité nécessaire pour la modification non linéaire.</span><span class="sxs-lookup"><span data-stu-id="cc91a-107">Prior to [DirectShow Editing Services](directshow-editing-services.md) (DES), however, DirectShow lacked the flexibility needed for nonlinear editing.</span></span>

<span data-ttu-id="cc91a-108">Par exemple, supposons que vous souhaitiez créer une séquence vidéo composée de 4 secondes à partir de la source A, puis de 10 secondes à partir de la source B et se terminant à 5 secondes de la source C. Cela peut être très simple à utiliser uniquement l’API de base DirectShow.</span><span class="sxs-lookup"><span data-stu-id="cc91a-108">For example, suppose you wanted to create a video sequence consisting of 4 seconds from source A, followed by 10 seconds from source B, and ending with 5 seconds from source C. You could accomplish that much fairly easily using only the core DirectShow API.</span></span>

<span data-ttu-id="cc91a-109">Mais que se passe-vous si vous avez décidé que la source C doit être antérieure à la source B, pas après ; que la séquence doit utiliser 8 secondes de la source A, et non 4 ; et que l’ensemble de la production nécessitait la lecture d’une piste audio distincte en arrière-plan ?</span><span class="sxs-lookup"><span data-stu-id="cc91a-109">But what if you decided that source C should come before source B, not after; that the sequence should use 8 seconds from source A, not 4; and that the entire production needed a separate audio track playing in the background?</span></span> <span data-ttu-id="cc91a-110">Même les modifications mineures, telles que celles-ci, peuvent être difficiles à implémenter.</span><span class="sxs-lookup"><span data-stu-id="cc91a-110">Even minor changes such as these could be difficult to implement.</span></span> <span data-ttu-id="cc91a-111">Toutefois, le scénario qui vient d’être décrit est un projet de modification trivial dans DES. vous pouvez le faire avec quelques appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="cc91a-111">But the scenario just described is a trivial editing project in DES—you can do it with a handful of method calls.</span></span>

<span data-ttu-id="cc91a-112">Voici quelques-unes des fonctionnalités offertes par DirectShow :</span><span class="sxs-lookup"><span data-stu-id="cc91a-112">Here are some of the features that DES brings to DirectShow:</span></span>

-   <span data-ttu-id="cc91a-113">Modèle de chronologie qui organise les pistes audio et vidéo en couches imbriquées, ce qui facilite la manipulation de la production finale</span><span class="sxs-lookup"><span data-stu-id="cc91a-113">A timeline model that organizes video and audio tracks into nested layers, making it easy to manipulate the final production</span></span>
-   <span data-ttu-id="cc91a-114">La possibilité d’afficher un aperçu d’un projet vidéo à la volée</span><span class="sxs-lookup"><span data-stu-id="cc91a-114">The ability to preview a video project on the fly</span></span>
-   <span data-ttu-id="cc91a-115">Persistance de projet via un format XML</span><span class="sxs-lookup"><span data-stu-id="cc91a-115">Project persistence through an XML-based format</span></span>
-   <span data-ttu-id="cc91a-116">Prise en charge des effets audio et vidéo, ainsi que des transitions entre les pistes vidéo (comme les fondus et les effaces)</span><span class="sxs-lookup"><span data-stu-id="cc91a-116">Support for video and audio effects, as well as transitions between video tracks (such as fades and wipes)</span></span>
-   <span data-ttu-id="cc91a-117">Plus de 100 réinitialisations standard, telles que définies par la société des ingénieurs d’images animées et de télévision (SMPTE)</span><span class="sxs-lookup"><span data-stu-id="cc91a-117">Over 100 standard wipes, as defined by the Society of Motion Picture and Television Engineers (SMPTE)</span></span>
-   <span data-ttu-id="cc91a-118">Incrustation basée sur la teinte, la luminance, la valeur RVB ou la valeur alpha</span><span class="sxs-lookup"><span data-stu-id="cc91a-118">Keying based on hue, luminance, RGB value, or alpha value</span></span>
-   <span data-ttu-id="cc91a-119">Conversion automatique des fréquences d’images et des taux d’échantillonnage audio, ce qui permet à une production d’utiliser des sources hétérogènes</span><span class="sxs-lookup"><span data-stu-id="cc91a-119">Automatic conversion of frame rates and audio sampling rates, enabling a production to use heterogeneous sources</span></span>
-   <span data-ttu-id="cc91a-120">Redimensionnement ou rognage de la vidéo</span><span class="sxs-lookup"><span data-stu-id="cc91a-120">Resizing or cropping of video</span></span>

<span data-ttu-id="cc91a-121">Limites :</span><span class="sxs-lookup"><span data-stu-id="cc91a-121">Limitations:</span></span>

-   <span data-ttu-id="cc91a-122">DES ne prend pas en charge les sources vidéo MPEG-2 ou H. 264.</span><span class="sxs-lookup"><span data-stu-id="cc91a-122">DES does not support MPEG-2 or H.264 video sources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cc91a-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cc91a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc91a-124">Services d’édition DirectShow</span><span class="sxs-lookup"><span data-stu-id="cc91a-124">DirectShow Editing Services</span></span>](directshow-editing-services.md)
</dt> </dl>

 

 



