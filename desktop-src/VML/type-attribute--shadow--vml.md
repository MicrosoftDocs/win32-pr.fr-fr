---
title: Attribut type (Shadow) (VML)
description: Attribut type (Shadow) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382304"
---
# <a name="type-attribute-shadowvml"></a><span data-ttu-id="33c84-103">Attribut type (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="33c84-103">Type Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="33c84-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="33c84-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="33c84-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="33c84-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="33c84-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="33c84-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="33c84-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="33c84-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="33c84-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="33c84-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="33c84-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="33c84-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="33c84-110">Spécifie le type d’ombre.</span><span class="sxs-lookup"><span data-stu-id="33c84-110">Specifies the type of shadow.</span></span> <span data-ttu-id="33c84-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="33c84-111">Read/write.</span></span> <span data-ttu-id="33c84-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="33c84-112">**String**.</span></span>

<span data-ttu-id="33c84-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="33c84-113">**Applies To**</span></span>

[<span data-ttu-id="33c84-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="33c84-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="33c84-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="33c84-115">**Tag Syntax**</span></span>

<span data-ttu-id="33c84-116"><v : type d' *élément* = « *expression* » ></span><span class="sxs-lookup"><span data-stu-id="33c84-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="33c84-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="33c84-117">**Script Syntax**</span></span>

<span data-ttu-id="33c84-118">*Element* . type = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="33c84-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="33c84-119">*expression* = *Element*. type</span><span class="sxs-lookup"><span data-stu-id="33c84-119">*expression*=*element*.type</span></span>

<span data-ttu-id="33c84-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="33c84-120">**Remarks**</span></span>

<span data-ttu-id="33c84-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="33c84-121">Values include:</span></span>



| <span data-ttu-id="33c84-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="33c84-122">Value</span></span>           | <span data-ttu-id="33c84-123">Description</span><span class="sxs-lookup"><span data-stu-id="33c84-123">Description</span></span>                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33c84-124">unique</span><span class="sxs-lookup"><span data-stu-id="33c84-124">single</span></span>          | <span data-ttu-id="33c84-125">Ombre unique.</span><span class="sxs-lookup"><span data-stu-id="33c84-125">Single shadow.</span></span> <span data-ttu-id="33c84-126">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="33c84-126">Default.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="33c84-127">double</span><span class="sxs-lookup"><span data-stu-id="33c84-127">double</span></span>          | <span data-ttu-id="33c84-128">Ombre double.</span><span class="sxs-lookup"><span data-stu-id="33c84-128">A double shadow.</span></span> <span data-ttu-id="33c84-129">[Color2](color2-attribute--shadow--vml.md) est utilisé pour la couleur de la deuxième ombre et [Offset2](msdn-online-vml-offset2-attribute.md) est utilisé pour le décalage de la deuxième ombre.</span><span class="sxs-lookup"><span data-stu-id="33c84-129">[Color2](color2-attribute--shadow--vml.md) is used for the color of the second shadow and [Offset2](msdn-online-vml-offset2-attribute.md) is used for the second shadow's offset.</span></span> |
| <span data-ttu-id="33c84-130">perspective</span><span class="sxs-lookup"><span data-stu-id="33c84-130">perspective</span></span>     | <span data-ttu-id="33c84-131">Ombre de perspective.</span><span class="sxs-lookup"><span data-stu-id="33c84-131">A perspective shadow.</span></span>                                                                                                                                                                                |
| <span data-ttu-id="33c84-132">shapeRelative</span><span class="sxs-lookup"><span data-stu-id="33c84-132">shapeRelative</span></span>   | <span data-ttu-id="33c84-133">L’ombre est créée par rapport à la forme.</span><span class="sxs-lookup"><span data-stu-id="33c84-133">The shadow is created relative to the shape.</span></span>                                                                                                                                                         |
| <span data-ttu-id="33c84-134">drawingRelative</span><span class="sxs-lookup"><span data-stu-id="33c84-134">drawingRelative</span></span> | <span data-ttu-id="33c84-135">L’ombre est créée par rapport au dessin.</span><span class="sxs-lookup"><span data-stu-id="33c84-135">The shadow is created relative to the drawing.</span></span>                                                                                                                                                       |
| <span data-ttu-id="33c84-136">gaufrage</span><span class="sxs-lookup"><span data-stu-id="33c84-136">emboss</span></span>          | <span data-ttu-id="33c84-137">L’ombre a un aspect en relief.</span><span class="sxs-lookup"><span data-stu-id="33c84-137">The shadow has an embossed look.</span></span>                                                                                                                                                                     |



 

<span data-ttu-id="33c84-138">**Attribut standard VML**</span><span class="sxs-lookup"><span data-stu-id="33c84-138">**VML Standard Attribute**</span></span>

<span data-ttu-id="33c84-139">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="33c84-139">**Example**</span></span>

<span data-ttu-id="33c84-140">Une double ombre est créée avec le deuxième vert de l’ombre et le décalage de 5 points vers le point et vers la droite.</span><span class="sxs-lookup"><span data-stu-id="33c84-140">A double shadow is created with the second shadow green and offset 5 points down and to the right.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 