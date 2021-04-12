---
title: Attribut de nuances de gris VML
description: Attribut de nuances de gris VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382168"
---
# <a name="vml-grayscale-attribute"></a><span data-ttu-id="08943-103">Attribut de nuances de gris VML</span><span class="sxs-lookup"><span data-stu-id="08943-103">VML GrayScale Attribute</span></span>

<span data-ttu-id="08943-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="08943-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08943-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="08943-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08943-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="08943-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08943-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="08943-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08943-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="08943-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08943-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="08943-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08943-110">Détermine si une image sera affichée en mode nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="08943-110">Determines whether a picture will be displayed in grayscale mode.</span></span> <span data-ttu-id="08943-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="08943-111">Read/write.</span></span> <span data-ttu-id="08943-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="08943-112">**VgTriState**.</span></span>

<span data-ttu-id="08943-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="08943-113">**Applies To**</span></span>

[<span data-ttu-id="08943-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="08943-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="08943-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="08943-115">**Tag Syntax**</span></span>

<span data-ttu-id="08943-116"><v : *élément* nuances de gris = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="08943-116"><v: *element* grayscale=" *expression* "></span></span>

<span data-ttu-id="08943-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="08943-117">**Script Syntax**</span></span>

<span data-ttu-id="08943-118">*Element* . nuances de gris = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="08943-118">*element* .grayscale="*expression*"</span></span>

<span data-ttu-id="08943-119">*expression* = *élément*. nuances de gris</span><span class="sxs-lookup"><span data-stu-id="08943-119">*expression*=*element*.grayscale</span></span>

<span data-ttu-id="08943-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="08943-120">**Remarks**</span></span>

<span data-ttu-id="08943-121">Si la **valeur est true**, l’image s’affiche en nuances de gris au lieu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="08943-121">If **True**, the picture will be displayed in grayscale instead of color.</span></span> <span data-ttu-id="08943-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="08943-122">The default is **False**.</span></span>

<span data-ttu-id="08943-123">La valeur est basée sur la recommandation CCIR 709, qui privilégie davantage le poids vert et produit des résultats plus agréables pour la couleur naturelle.</span><span class="sxs-lookup"><span data-stu-id="08943-123">The value is based according to CCIR recommendation 709, which favors more green weight and produces more pleasing results for natural color.</span></span>

<span data-ttu-id="08943-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="08943-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="08943-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="08943-125">**Example**</span></span>

<span data-ttu-id="08943-126">L’image sera affichée en nuances de gris au lieu de la couleur.</span><span class="sxs-lookup"><span data-stu-id="08943-126">The image will be displayed in grayscale instead of color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 