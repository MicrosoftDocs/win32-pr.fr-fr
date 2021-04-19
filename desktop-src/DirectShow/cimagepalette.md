---
description: La classe CImagePalette gère les palettes pour les convertisseurs vidéo. Il peut être utilisé pour créer une palette logique à partir d’un format vidéo. Cette classe est destinée à être utilisée avec les classes CBaseWindow et CDrawImage. elle est donc un peu spécialisée.
ms.assetid: dcbe5049-0e8c-4221-825a-0fd8e6efd2a5
title: CImagePalette, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImagePalette
api_type:
- COM
api_location: ''
ms.openlocfilehash: 696c51e4918815e18accbadd66c764493dc0b98e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106539027"
---
# <a name="cimagepalette-class"></a><span data-ttu-id="2ab18-105">CImagePalette, classe</span><span class="sxs-lookup"><span data-stu-id="2ab18-105">CImagePalette class</span></span>

<span data-ttu-id="2ab18-106">La `CImagePalette` classe gère les palettes pour les convertisseurs vidéo.</span><span class="sxs-lookup"><span data-stu-id="2ab18-106">The `CImagePalette` class manages palettes for video renderers.</span></span> <span data-ttu-id="2ab18-107">Il peut être utilisé pour créer une palette logique à partir d’un format vidéo.</span><span class="sxs-lookup"><span data-stu-id="2ab18-107">It can be used to create a logical palette from a video format.</span></span> <span data-ttu-id="2ab18-108">Cette classe est destinée à être utilisée avec les classes [**CBaseWindow**](cbasewindow.md) et [**CDrawImage**](cdrawimage.md) . elle est donc un peu spécialisée.</span><span class="sxs-lookup"><span data-stu-id="2ab18-108">This class is intended to be used with the [**CBaseWindow**](cbasewindow.md) and [**CDrawImage**](cdrawimage.md) classes, so it is somewhat specialized.</span></span>



| <span data-ttu-id="2ab18-109">Variables membres protégées</span><span class="sxs-lookup"><span data-stu-id="2ab18-109">Protected Member Variables</span></span>                                       | <span data-ttu-id="2ab18-110">Description</span><span class="sxs-lookup"><span data-stu-id="2ab18-110">Description</span></span>                                                                                    |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ab18-111">**m \_ HPALETTE**</span><span class="sxs-lookup"><span data-stu-id="2ab18-111">**m\_hPalette**</span></span>](cimagepalette-m-hpalette.md)                  | <span data-ttu-id="2ab18-112">Handle vers la palette logique gérée par cet objet.</span><span class="sxs-lookup"><span data-stu-id="2ab18-112">Handle to the logical palette that this object manages.</span></span>                                        |
| [<span data-ttu-id="2ab18-113">**m \_ pBaseWindow**</span><span class="sxs-lookup"><span data-stu-id="2ab18-113">**m\_pBaseWindow**</span></span>](cimagepalette-m-pbasewindow.md)            | <span data-ttu-id="2ab18-114">Pointeur vers l’objet **CBaseWindow** qui gère la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="2ab18-114">Pointer to the **CBaseWindow** object that manages the window.</span></span>                                 |
| [<span data-ttu-id="2ab18-115">**m \_ pDrawImage**</span><span class="sxs-lookup"><span data-stu-id="2ab18-115">**m\_pDrawImage**</span></span>](cimagepalette-m-pdrawimage.md)              | <span data-ttu-id="2ab18-116">Pointeur vers l’objet **CDrawImage** qui dessine l’image vidéo.</span><span class="sxs-lookup"><span data-stu-id="2ab18-116">Pointer to the **CDrawImage** object that draws the video image.</span></span>                               |
| [<span data-ttu-id="2ab18-117">**m \_ pFilter**</span><span class="sxs-lookup"><span data-stu-id="2ab18-117">**m\_pFilter**</span></span>](cimagepalette-m-pfilter.md)                    | <span data-ttu-id="2ab18-118">Pointeur désignant le filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="2ab18-118">Pointer to the owning filter.</span></span>                                                                  |
| <span data-ttu-id="2ab18-119">M&#233;thodes publiques</span><span class="sxs-lookup"><span data-stu-id="2ab18-119">Public Methods</span></span>                                                   | <span data-ttu-id="2ab18-120">Description</span><span class="sxs-lookup"><span data-stu-id="2ab18-120">Description</span></span>                                                                                    |
| [<span data-ttu-id="2ab18-121">**CImagePalette**</span><span class="sxs-lookup"><span data-stu-id="2ab18-121">**CImagePalette**</span></span>](cimagepalette-cimagepalette.md)             | <span data-ttu-id="2ab18-122">Méthode de constructeur.</span><span class="sxs-lookup"><span data-stu-id="2ab18-122">Constructor method.</span></span>                                                                            |
| [<span data-ttu-id="2ab18-123">**CopyPalette**</span><span class="sxs-lookup"><span data-stu-id="2ab18-123">**CopyPalette**</span></span>](cimagepalette-copypalette.md)                 | <span data-ttu-id="2ab18-124">Copie la palette de toute structure **VIDEOINFO** vers toute structure en palette **VIDEOINFO** .</span><span class="sxs-lookup"><span data-stu-id="2ab18-124">Copies the palette from any **VIDEOINFO** structure to any palettized **VIDEOINFO** structure.</span></span> |
| [<span data-ttu-id="2ab18-125">**MakeIdentityPalette**</span><span class="sxs-lookup"><span data-stu-id="2ab18-125">**MakeIdentityPalette**</span></span>](cimagepalette-makeidentitypalette.md) | <span data-ttu-id="2ab18-126">Tente de créer une palette qui correspond directement à la palette sélectionnée dans le périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="2ab18-126">Attempts to make a palette that maps directly to the palette selected in the display device.</span></span>   |
| [<span data-ttu-id="2ab18-127">**MakePalette**</span><span class="sxs-lookup"><span data-stu-id="2ab18-127">**MakePalette**</span></span>](cimagepalette-makepalette.md)                 | <span data-ttu-id="2ab18-128">Crée une palette logique à partir de la table des couleurs dans un format vidéo.</span><span class="sxs-lookup"><span data-stu-id="2ab18-128">Creates a logical palette from the color table in a video format.</span></span>                              |
| [<span data-ttu-id="2ab18-129">**PreparePalette**</span><span class="sxs-lookup"><span data-stu-id="2ab18-129">**PreparePalette**</span></span>](cimagepalette-preparepalette.md)           | <span data-ttu-id="2ab18-130">Configure une palette en fonction d’un type de média à partir du filtre propriétaire.</span><span class="sxs-lookup"><span data-stu-id="2ab18-130">Sets up a palette, based on a media type from the owning filter.</span></span>                               |
| [<span data-ttu-id="2ab18-131">**RemovePalette**</span><span class="sxs-lookup"><span data-stu-id="2ab18-131">**RemovePalette**</span></span>](cimagepalette-removepalette.md)             | <span data-ttu-id="2ab18-132">Supprime la palette logique existante.</span><span class="sxs-lookup"><span data-stu-id="2ab18-132">Deletes the existing logical palette.</span></span>                                                          |



 

 

 



