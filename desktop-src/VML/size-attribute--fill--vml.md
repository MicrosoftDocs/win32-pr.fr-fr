---
title: Size, attribut (Fill) (VML)
description: Size, attribut (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941054"
---
# <a name="size-attribute-fillvml"></a><span data-ttu-id="5d80c-103">Size, attribut (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="5d80c-103">Size Attribute (Fill)(VML)</span></span>

<span data-ttu-id="5d80c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5d80c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5d80c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5d80c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5d80c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="5d80c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5d80c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="5d80c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5d80c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5d80c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5d80c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5d80c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5d80c-110">Définit la taille de l’image pour le remplissage.</span><span class="sxs-lookup"><span data-stu-id="5d80c-110">Defines the size of the image for the fill.</span></span> <span data-ttu-id="5d80c-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5d80c-111">Read/write.</span></span> <span data-ttu-id="5d80c-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="5d80c-112">[VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .</span></span>

<span data-ttu-id="5d80c-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5d80c-113">**Applies To**</span></span>

[<span data-ttu-id="5d80c-114">Complète</span><span class="sxs-lookup"><span data-stu-id="5d80c-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="5d80c-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="5d80c-115">**Tag Syntax**</span></span>

<span data-ttu-id="5d80c-116"><v : *Element* size = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5d80c-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="5d80c-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="5d80c-117">**Script Syntax**</span></span>

<span data-ttu-id="5d80c-118">*Element* . Size = "*expression \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="5d80c-118">*element* .size="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="5d80c-119">*expression* = *Element*. Size</span><span class="sxs-lookup"><span data-stu-id="5d80c-119">*expression*=*element*.size</span></span>

<span data-ttu-id="5d80c-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5d80c-120">**Remarks**</span></span>

<span data-ttu-id="5d80c-121">La valeur par défaut est la taille de l’image d’origine.</span><span class="sxs-lookup"><span data-stu-id="5d80c-121">The default is the size of the original image.</span></span> <span data-ttu-id="5d80c-122">Les tailles supérieures à shapewill affichent une version agrandie mais tronquée de l’image.</span><span class="sxs-lookup"><span data-stu-id="5d80c-122">Sizes that are larger than the shapewill display a magnified but clipped version of the image.</span></span>

<span data-ttu-id="5d80c-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="5d80c-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5d80c-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="5d80c-124">**Example**</span></span>

<span data-ttu-id="5d80c-125">Bien que la taille d’origine de l’image soit de 50 à 50 points, l’image est affichée sous la forme d’une image 10 par 10 au centre du remplissage.</span><span class="sxs-lookup"><span data-stu-id="5d80c-125">Even though the original size of the image is 50-by-50 points, the image will be displayed as a 10-by-10 image in the center of the fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 