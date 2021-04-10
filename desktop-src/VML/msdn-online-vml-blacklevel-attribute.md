---
title: BlackLevel VML (attribut)
description: BlackLevel VML (attribut)
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031451"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="85a39-103">BlackLevel VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="85a39-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="85a39-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="85a39-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="85a39-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="85a39-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="85a39-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="85a39-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="85a39-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="85a39-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="85a39-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="85a39-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="85a39-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="85a39-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="85a39-110">Définit l’intensité du noir dans une image.</span><span class="sxs-lookup"><span data-stu-id="85a39-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="85a39-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="85a39-111">Read/write.</span></span> <span data-ttu-id="85a39-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="85a39-112">**VgNumber**.</span></span>

<span data-ttu-id="85a39-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="85a39-113">**Applies To**</span></span>

[<span data-ttu-id="85a39-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="85a39-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="85a39-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="85a39-115">**Tag Syntax**</span></span>

<span data-ttu-id="85a39-116"><v : *Element* blacklevel = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="85a39-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="85a39-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="85a39-117">**Script Syntax**</span></span>

<span data-ttu-id="85a39-118">*Element* . blacklevel = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="85a39-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="85a39-119">*expression* = *élément*. blacklevel</span><span class="sxs-lookup"><span data-stu-id="85a39-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="85a39-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="85a39-120">**Remarks**</span></span>

<span data-ttu-id="85a39-121">Permet de modifier le niveau de couleur afin que les noirs apparaissent comme des véritables noirs, et que toutes les autres couleurs soient visibles en tant que nuances au-dessus du noir.</span><span class="sxs-lookup"><span data-stu-id="85a39-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="85a39-122">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="85a39-122">The default value is 0.</span></span> <span data-ttu-id="85a39-123">Bien qu’un nombre quelconque entre le nombre positif et l’infini négatif soit autorisé, les valeurs inférieures à-0,5 s’affichent en noir et les valeurs supérieures à 0,5 s’affichent comme tout en blanc.</span><span class="sxs-lookup"><span data-stu-id="85a39-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="85a39-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="85a39-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="85a39-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="85a39-125">**Example**</span></span>

<span data-ttu-id="85a39-126">L’image sera affichée avec des tons très sombres.</span><span class="sxs-lookup"><span data-stu-id="85a39-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 