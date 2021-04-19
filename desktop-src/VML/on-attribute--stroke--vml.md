---
title: Sur attribut (Stroke) (VML)
description: Sur attribut (Stroke) (VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106532040"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="08e7b-103">Sur attribut (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="08e7b-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="08e7b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="08e7b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="08e7b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="08e7b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="08e7b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="08e7b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="08e7b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="08e7b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="08e7b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="08e7b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="08e7b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="08e7b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="08e7b-110">Détermine si le trait sera affiché.</span><span class="sxs-lookup"><span data-stu-id="08e7b-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="08e7b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="08e7b-111">Read/write.</span></span> <span data-ttu-id="08e7b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="08e7b-112">**VgTriState**.</span></span>

<span data-ttu-id="08e7b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="08e7b-113">**Applies To**</span></span>

[<span data-ttu-id="08e7b-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="08e7b-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="08e7b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="08e7b-115">**Tag Syntax**</span></span>

<span data-ttu-id="08e7b-116"><v : *Element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="08e7b-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="08e7b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="08e7b-117">**Script Syntax**</span></span>

<span data-ttu-id="08e7b-118">*Element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="08e7b-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="08e7b-119">*expression* = *élément*. on</span><span class="sxs-lookup"><span data-stu-id="08e7b-119">*expression*=*element*.on</span></span>

<span data-ttu-id="08e7b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="08e7b-120">**Remarks**</span></span>

<span data-ttu-id="08e7b-121">Si la **valeur est false**, le trait n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="08e7b-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="08e7b-122">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="08e7b-122">The default is **True**.</span></span>

<span data-ttu-id="08e7b-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="08e7b-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="08e7b-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="08e7b-124">**Example**</span></span>

<span data-ttu-id="08e7b-125">Le trait ne s’affiche pas.</span><span class="sxs-lookup"><span data-stu-id="08e7b-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 