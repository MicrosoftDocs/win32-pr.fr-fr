---
title: Attribut de couleur (trait) (VML)
description: Attribut de couleur (trait) (VML)
ms.assetid: 8fa19789-0bd6-4e9f-8af4-566155eafc6a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faa91522adcba5fa854d4749dc257f5489969270
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511506"
---
# <a name="color-attribute-strokevml"></a><span data-ttu-id="f6438-103">Attribut de couleur (trait) (VML)</span><span class="sxs-lookup"><span data-stu-id="f6438-103">Color Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="f6438-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f6438-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f6438-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f6438-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f6438-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="f6438-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f6438-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="f6438-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f6438-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f6438-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f6438-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f6438-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f6438-110">Définit la couleur d’un trait.</span><span class="sxs-lookup"><span data-stu-id="f6438-110">Defines the color of a stroke.</span></span> <span data-ttu-id="f6438-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f6438-111">Read/write.</span></span> <span data-ttu-id="f6438-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="f6438-112">**VgColor**.</span></span>

<span data-ttu-id="f6438-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f6438-113">**Applies To**</span></span>

[<span data-ttu-id="f6438-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="f6438-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="f6438-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="f6438-115">**Tag Syntax**</span></span>

<span data-ttu-id="f6438-116"><v : *Element* Color = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f6438-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="f6438-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="f6438-117">**Script Syntax**</span></span>

<span data-ttu-id="f6438-118">*Element* . Color = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f6438-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="f6438-119">*expression* = *Element*. Color</span><span class="sxs-lookup"><span data-stu-id="f6438-119">*expression*=*element*.color</span></span>

<span data-ttu-id="f6438-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="f6438-120">**Remarks**</span></span>

<span data-ttu-id="f6438-121">Remplace l’attribut **StrokeColor** d’une forme.</span><span class="sxs-lookup"><span data-stu-id="f6438-121">Overrides the **StrokeColor** attribute of a shape.</span></span> <span data-ttu-id="f6438-122">La valeur par défaut est **noir**.</span><span class="sxs-lookup"><span data-stu-id="f6438-122">The default value is **black**.</span></span>

<span data-ttu-id="f6438-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="f6438-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f6438-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f6438-124">**Example**</span></span>

<span data-ttu-id="f6438-125">La couleur du trait de la forme est **verte**, et non **rouge**.</span><span class="sxs-lookup"><span data-stu-id="f6438-125">The shape has a stroke color of **green**, not **red**.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke color="green"/>
   </v:shape>
```



 

 