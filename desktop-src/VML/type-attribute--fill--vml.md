---
title: Attribut type (Fill) (VML)
description: Attribut type (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728805"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="70e00-103">Attribut type (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="70e00-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="70e00-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="70e00-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="70e00-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="70e00-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="70e00-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="70e00-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="70e00-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="70e00-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="70e00-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="70e00-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="70e00-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="70e00-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="70e00-110">Détermine le type de remplissage.</span><span class="sxs-lookup"><span data-stu-id="70e00-110">Determines the type of fill.</span></span> <span data-ttu-id="70e00-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="70e00-111">Read/write.</span></span> <span data-ttu-id="70e00-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="70e00-112">**VgFillType**.</span></span>

<span data-ttu-id="70e00-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="70e00-113">**Applies To**</span></span>

[<span data-ttu-id="70e00-114">Complète</span><span class="sxs-lookup"><span data-stu-id="70e00-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="70e00-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="70e00-115">**Tag Syntax**</span></span>

<span data-ttu-id="70e00-116"><v : type d' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="70e00-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="70e00-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="70e00-117">**Script Syntax**</span></span>

<span data-ttu-id="70e00-118">*Element* . type = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="70e00-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="70e00-119">*expression* = *Element*. type</span><span class="sxs-lookup"><span data-stu-id="70e00-119">*expression*=*element*.type</span></span>

<span data-ttu-id="70e00-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="70e00-120">**Remarks**</span></span>

<span data-ttu-id="70e00-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="70e00-121">Values include:</span></span>



| <span data-ttu-id="70e00-122">Type</span><span class="sxs-lookup"><span data-stu-id="70e00-122">Type</span></span>           | <span data-ttu-id="70e00-123">Description</span><span class="sxs-lookup"><span data-stu-id="70e00-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="70e00-124">Solid</span><span class="sxs-lookup"><span data-stu-id="70e00-124">solid</span></span>          | <span data-ttu-id="70e00-125">Le motif de remplissage est plein.</span><span class="sxs-lookup"><span data-stu-id="70e00-125">The fill pattern is solid.</span></span> <span data-ttu-id="70e00-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="70e00-126">Default.</span></span>                                     |
| <span data-ttu-id="70e00-127">dégradé</span><span class="sxs-lookup"><span data-stu-id="70e00-127">gradient</span></span>       | <span data-ttu-id="70e00-128">Les couleurs de remplissage se combinent dans un dégradé linéaire de bas en haut.</span><span class="sxs-lookup"><span data-stu-id="70e00-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="70e00-129">gradientradial</span><span class="sxs-lookup"><span data-stu-id="70e00-129">gradientradial</span></span> | <span data-ttu-id="70e00-130">Les couleurs de remplissage se combinent dans un dégradé radial.</span><span class="sxs-lookup"><span data-stu-id="70e00-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="70e00-131">tile</span><span class="sxs-lookup"><span data-stu-id="70e00-131">tile</span></span>           | <span data-ttu-id="70e00-132">L’image de remplissage est en mosaïque.</span><span class="sxs-lookup"><span data-stu-id="70e00-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="70e00-133">modèle</span><span class="sxs-lookup"><span data-stu-id="70e00-133">pattern</span></span>        | <span data-ttu-id="70e00-134">L’image est utilisée pour créer un modèle à l’aide des couleurs de remplissage.</span><span class="sxs-lookup"><span data-stu-id="70e00-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="70e00-135">frame</span><span class="sxs-lookup"><span data-stu-id="70e00-135">frame</span></span>          | <span data-ttu-id="70e00-136">L’image est étirée pour remplir la forme.</span><span class="sxs-lookup"><span data-stu-id="70e00-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="70e00-137">**Attribut standard VML**</span><span class="sxs-lookup"><span data-stu-id="70e00-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="70e00-138">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="70e00-138">**Example**</span></span>

<span data-ttu-id="70e00-139">Un remplissage de premier plan rouge et un remplissage d’arrière-plan bleu sont créés à l’aide du modèle de l’image myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="70e00-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 