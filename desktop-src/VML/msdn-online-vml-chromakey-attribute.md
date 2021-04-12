---
title: Chromakey VML (attribut)
description: Chromakey VML (attribut)
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315635"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="8ad0b-103">Chromakey VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="8ad0b-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="8ad0b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="8ad0b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="8ad0b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="8ad0b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="8ad0b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="8ad0b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="8ad0b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="8ad0b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="8ad0b-110">Définit la valeur de couleur de l’image qui sera traitée comme transparente.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="8ad0b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-111">Read/write.</span></span> <span data-ttu-id="8ad0b-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-112">**VgColor**.</span></span>

<span data-ttu-id="8ad0b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="8ad0b-113">**Applies To**</span></span>

[<span data-ttu-id="8ad0b-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="8ad0b-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="8ad0b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="8ad0b-115">**Tag Syntax**</span></span>

<span data-ttu-id="8ad0b-116"><v : *Element* chromakey = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="8ad0b-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="8ad0b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="8ad0b-117">**Script Syntax**</span></span>

<span data-ttu-id="8ad0b-118">*Element* . chromakey = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="8ad0b-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="8ad0b-119">*expression* = *élément*. chromakey</span><span class="sxs-lookup"><span data-stu-id="8ad0b-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="8ad0b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="8ad0b-120">**Remarks**</span></span>

<span data-ttu-id="8ad0b-121">Utilisez cet attribut pour rendre des parties d’une image transparentes en masquant la transparence à une couleur spécifique.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="8ad0b-122">Par exemple, si vous définissez la valeur **chromakey** en **noir**, toute partie de l’image qui est noire est transparente et la couleur de remplissage « s’affiche » dans cette partie de l’image.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="8ad0b-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="8ad0b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="8ad0b-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="8ad0b-124">**Example**</span></span>

<span data-ttu-id="8ad0b-125">Les zones de l’image qui sont de couleur noire unie deviennent transparentes, ce qui permet à la couleur de remplissage verte de s’afficher à la place dans ces zones.</span><span class="sxs-lookup"><span data-stu-id="8ad0b-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 