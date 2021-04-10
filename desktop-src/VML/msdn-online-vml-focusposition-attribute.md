---
title: FocusPosition VML (attribut)
description: FocusPosition VML (attribut)
ms.assetid: 1aebf79d-c887-4a61-b50c-01a4ebfd68a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92a418916efb1721c41b7db37256ac3a040ea4b5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102317"
---
# <a name="vml-focusposition-attribute"></a><span data-ttu-id="2c7b4-103">FocusPosition VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="2c7b4-103">VML FocusPosition Attribute</span></span>

<span data-ttu-id="2c7b4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2c7b4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2c7b4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2c7b4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2c7b4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2c7b4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2c7b4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2c7b4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2c7b4-110">Définit le centre d’un dégradé radial.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-110">Defines the center of a radial gradient.</span></span> <span data-ttu-id="2c7b4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-111">Read/write.</span></span> <span data-ttu-id="2c7b4-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-112">**VgVector2D**.</span></span>

<span data-ttu-id="2c7b4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-113">**Applies To**</span></span>

[<span data-ttu-id="2c7b4-114">Complète</span><span class="sxs-lookup"><span data-stu-id="2c7b4-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="2c7b4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-115">**Tag Syntax**</span></span>

<span data-ttu-id="2c7b4-116"><v : *Element* focusposition = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2c7b4-116"><v: *element* focusposition=" *expression* "></span></span>

<span data-ttu-id="2c7b4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-117">**Script Syntax**</span></span>

<span data-ttu-id="2c7b4-118">*Element* . focusposition = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2c7b4-118">*element* .focusposition="*expression*"</span></span>

<span data-ttu-id="2c7b4-119">*expression* = *élément*. focusposition</span><span class="sxs-lookup"><span data-stu-id="2c7b4-119">*expression*=*element*.focusposition</span></span>

<span data-ttu-id="2c7b4-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-120">**Remarks**</span></span>

<span data-ttu-id="2c7b4-121">Spécifie les dégradés radiaux positionfor centraux.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-121">Specifies the center positionfor radial gradients.</span></span> <span data-ttu-id="2c7b4-122">Le vecteur est une fraction de la largeur et de la hauteur de la forme.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-122">The vector is a fraction of the width and height of the shape.</span></span> <span data-ttu-id="2c7b4-123">Le premier est un pourcentage du remplissage jusqu’au bord gauche ; le deuxième est un pourcentage du remplissage vers le haut.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-123">The first is a percentage of the fill to the left edge; the second is a percentage of the fill to the top.</span></span> <span data-ttu-id="2c7b4-124">La valeur par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-124">The default value is 0,0.</span></span> <span data-ttu-id="2c7b4-125">Pour positionner un remplissage radial au centre d’une forme, utilisez la valeur 50%, 50%.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-125">To position a radial fill at the center of a shape, use the value of 50%,50%.</span></span>

<span data-ttu-id="2c7b4-126">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="2c7b4-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="2c7b4-127">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2c7b4-127">**Example**</span></span>

<span data-ttu-id="2c7b4-128">Le remplissage radial est centré afin que le bleu démarre au centre et rayonne vers l’extérieur, passant progressivement en rouge au moment où il atteint les bords extérieurs et les angles.</span><span class="sxs-lookup"><span data-stu-id="2c7b4-128">The radial fill will be centered so that blue will start in the center and radiate outward, gradually changing to red by the time it reaches the outside edges and corners.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="GradientRadial" color="red" color2="blue"
   focusposition="50%,50%"/>
   </v:shape>
```



 

 