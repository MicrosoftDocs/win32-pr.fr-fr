---
title: AlignShape VML (attribut)
description: AlignShape VML (attribut)
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316301"
---
# <a name="vml-alignshape-attribute"></a><span data-ttu-id="1a8e3-103">AlignShape VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="1a8e3-103">VML AlignShape Attribute</span></span>

<span data-ttu-id="1a8e3-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1a8e3-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1a8e3-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1a8e3-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1a8e3-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1a8e3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1a8e3-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1a8e3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1a8e3-110">Détermine si une image est alignée sur une forme.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-110">Determines whether an image will align with a shape.</span></span> <span data-ttu-id="1a8e3-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-111">Read/write.</span></span> <span data-ttu-id="1a8e3-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-112">**VgTriState**.</span></span>

<span data-ttu-id="1a8e3-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1a8e3-113">**Applies To**</span></span>

[<span data-ttu-id="1a8e3-114">Complète</span><span class="sxs-lookup"><span data-stu-id="1a8e3-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1a8e3-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="1a8e3-115">**Tag Syntax**</span></span>

<span data-ttu-id="1a8e3-116"><v : *Element* alignshape = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1a8e3-116"><v: *element* alignshape=" *expression* "></span></span>

<span data-ttu-id="1a8e3-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="1a8e3-117">**Script Syntax**</span></span>

<span data-ttu-id="1a8e3-118">*Element* . alignshape = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="1a8e3-118">*element* .alignshape="*expression*"</span></span>

<span data-ttu-id="1a8e3-119">*expression* = *élément*. alignshape</span><span class="sxs-lookup"><span data-stu-id="1a8e3-119">*expression*=*element*.alignshape</span></span>

<span data-ttu-id="1a8e3-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="1a8e3-120">**Remarks**</span></span>

<span data-ttu-id="1a8e3-121">Si la **valeur est true**, l’image utilisée pour créer le remplissage est alignée avec la forme.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-121">If **True**, the image used to create the fill is aligned with the shape.</span></span> <span data-ttu-id="1a8e3-122">Si la **valeur est false**, l’image utilisée pour créer le remplissage est alignée avec la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-122">If **False**, the image used to create the fill is aligned with the window.</span></span> <span data-ttu-id="1a8e3-123">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-123">Default is **True**.</span></span>

<span data-ttu-id="1a8e3-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="1a8e3-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="1a8e3-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="1a8e3-125">**Example**</span></span>

<span data-ttu-id="1a8e3-126">L’image de remplissage en mosaïque créée à partir de myimage.gif est alignée avec la fenêtre, et non la forme ; même si la forme est pivotée, l’image ne l’est pas.</span><span class="sxs-lookup"><span data-stu-id="1a8e3-126">The tiled fill image created from myimage.gif is aligned with the window, not the shape; even though the shape is rotated, the image is not.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 