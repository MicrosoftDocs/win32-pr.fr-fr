---
title: Attribut AltHRef (Stroke) (VML)
description: Attribut AltHRef (Stroke) (VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021e89e87f70910561e55406e282920cdbed2963
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512749"
---
# <a name="althref-attribute-strokevml"></a><span data-ttu-id="64e49-103">Attribut AltHRef (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="64e49-103">AltHRef Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="64e49-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="64e49-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="64e49-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="64e49-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="64e49-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="64e49-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="64e49-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="64e49-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="64e49-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="64e49-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="64e49-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="64e49-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="64e49-110">Spécifie une autre référence pour une image.</span><span class="sxs-lookup"><span data-stu-id="64e49-110">Specifies an alternate reference for an image.</span></span> <span data-ttu-id="64e49-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="64e49-111">Read/write.</span></span> <span data-ttu-id="64e49-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="64e49-112">**String**.</span></span>

<span data-ttu-id="64e49-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="64e49-113">**Applies To**</span></span>

[<span data-ttu-id="64e49-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="64e49-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="64e49-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="64e49-115">**Tag Syntax**</span></span>

<span data-ttu-id="64e49-116"><v : *Element* o :althref = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="64e49-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="64e49-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="64e49-117">**Script Syntax**</span></span>

<span data-ttu-id="64e49-118">*Element* . althref = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="64e49-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="64e49-119">*expression* = *élément*. althref</span><span class="sxs-lookup"><span data-stu-id="64e49-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="64e49-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="64e49-120">**Remarks**</span></span>

<span data-ttu-id="64e49-121">Prend en charge la préservation des données PICT via des roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="64e49-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="64e49-122">Lors de l’écriture HTML, l’autre représentation (c’est-à-dire, les données PICT d’origine si le fichier provient du Macintosh) est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="64e49-122">On HTML write, the alternate representation (i.e., the original PICT data if the file originated from the Macintosh) is saved.</span></span> <span data-ttu-id="64e49-123">Lors de la lecture HTML, **AltHRef** est privilégié sur **src**.</span><span class="sxs-lookup"><span data-stu-id="64e49-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="64e49-124">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="64e49-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="64e49-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="64e49-125">**Example**</span></span>

<span data-ttu-id="64e49-126">Le trait de la forme a un **AltHRef** qui pointe vers un fichier nommé myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="64e49-126">The stroke of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 