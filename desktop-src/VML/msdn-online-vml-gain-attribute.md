---
title: Attribut gain de VML
description: Attribut gain de VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382310"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="238cf-103">Attribut gain de VML</span><span class="sxs-lookup"><span data-stu-id="238cf-103">VML Gain Attribute</span></span>

<span data-ttu-id="238cf-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="238cf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="238cf-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="238cf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="238cf-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="238cf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="238cf-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="238cf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="238cf-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="238cf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="238cf-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="238cf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="238cf-110">Définit l’intensité de toutes les couleurs d’une image.</span><span class="sxs-lookup"><span data-stu-id="238cf-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="238cf-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="238cf-111">Read/write.</span></span> <span data-ttu-id="238cf-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="238cf-112">**VgNumber**.</span></span>

<span data-ttu-id="238cf-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="238cf-113">**Applies To**</span></span>

[<span data-ttu-id="238cf-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="238cf-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="238cf-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="238cf-115">**Tag Syntax**</span></span>

<span data-ttu-id="238cf-116"><v : *élément* gain = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="238cf-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="238cf-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="238cf-117">**Script Syntax**</span></span>

<span data-ttu-id="238cf-118">*Element* . gain = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="238cf-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="238cf-119">*expression* = *Element*. gain</span><span class="sxs-lookup"><span data-stu-id="238cf-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="238cf-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="238cf-120">**Remarks**</span></span>

<span data-ttu-id="238cf-121">Cet attribut définit la luminosité du blanc de couleur, en affectant toutes les autres couleurs.</span><span class="sxs-lookup"><span data-stu-id="238cf-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="238cf-122">Les valeurs sont comprises entre 0 et Infinity.</span><span class="sxs-lookup"><span data-stu-id="238cf-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="238cf-123">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="238cf-123">The default value is 1.0.</span></span> <span data-ttu-id="238cf-124">La valeur 0 n’affiche aucune image.</span><span class="sxs-lookup"><span data-stu-id="238cf-124">A value of 0 displays no image.</span></span> <span data-ttu-id="238cf-125">Les valeurs supérieures à 1 éclaircissent l’image et les valeurs inférieures à 1 rendent l’image plus claire.</span><span class="sxs-lookup"><span data-stu-id="238cf-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="238cf-126">Cet attribut peut être utilisé pour créer des effets intéressants.</span><span class="sxs-lookup"><span data-stu-id="238cf-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="238cf-127">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="238cf-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="238cf-128">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="238cf-128">**Example**</span></span>

<span data-ttu-id="238cf-129">L’image s’affiche avec toutes les couleurs tendant vers le gris.</span><span class="sxs-lookup"><span data-stu-id="238cf-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 