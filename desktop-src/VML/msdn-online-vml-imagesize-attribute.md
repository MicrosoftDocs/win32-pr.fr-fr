---
title: Attribut d’image VML
description: Attribut d’image VML
ms.assetid: 6b021ac1-e447-46ad-9153-91f936fca0d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ae01d3162fdff67f0385736e5f0450b14ed6115
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728085"
---
# <a name="vml-imagesize-attribute"></a><span data-ttu-id="3c4af-103">Attribut d’image VML</span><span class="sxs-lookup"><span data-stu-id="3c4af-103">VML ImageSize Attribute</span></span>

<span data-ttu-id="3c4af-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3c4af-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3c4af-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="3c4af-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3c4af-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="3c4af-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3c4af-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="3c4af-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3c4af-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3c4af-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3c4af-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3c4af-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3c4af-110">Définit la taille de l’image pour le trait.</span><span class="sxs-lookup"><span data-stu-id="3c4af-110">Defines the size of the image for the stroke.</span></span> <span data-ttu-id="3c4af-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3c4af-111">Read/write.</span></span> <span data-ttu-id="3c4af-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="3c4af-112">**VgVector2D**.</span></span>

<span data-ttu-id="3c4af-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="3c4af-113">**Applies To**</span></span>

[<span data-ttu-id="3c4af-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="3c4af-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="3c4af-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="3c4af-115">**Tag Syntax**</span></span>

<span data-ttu-id="3c4af-116"><v : *Element* ImageSize = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3c4af-116"><v: *element* imagesize=" *expression* "></span></span>

<span data-ttu-id="3c4af-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="3c4af-117">**Script Syntax**</span></span>

<span data-ttu-id="3c4af-118">*Element* . ImageSize = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="3c4af-118">*element* .imagesize="*expression*"</span></span>

<span data-ttu-id="3c4af-119">*expression* = *Element*. ImageSize</span><span class="sxs-lookup"><span data-stu-id="3c4af-119">*expression*=*element*.imagesize</span></span>

<span data-ttu-id="3c4af-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="3c4af-120">**Remarks**</span></span>

<span data-ttu-id="3c4af-121">La valeur par défaut est la taille de l’image.</span><span class="sxs-lookup"><span data-stu-id="3c4af-121">Default is the size of the image.</span></span>

<span data-ttu-id="3c4af-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="3c4af-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="3c4af-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="3c4af-123">**Example**</span></span>

<span data-ttu-id="3c4af-124">L’image du trait aura une taille de 10 par 10 points.</span><span class="sxs-lookup"><span data-stu-id="3c4af-124">The stroke image will be a 10-by-10 point size.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagesize="10pt,10pt"/>
   </v:shape>
```



 

 