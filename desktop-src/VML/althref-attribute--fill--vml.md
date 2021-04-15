---
title: Attribut AltHRef (Fill) (VML)
description: Attribut AltHRef (Fill) (VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0679e5aa01b934092c21bfa5d0504b056f620f2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463310"
---
# <a name="althref-attribute-fillvml"></a><span data-ttu-id="e38ec-103">Attribut AltHRef (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="e38ec-103">AltHRef Attribute (Fill)(VML)</span></span>

<span data-ttu-id="e38ec-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e38ec-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e38ec-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="e38ec-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e38ec-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="e38ec-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e38ec-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="e38ec-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e38ec-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e38ec-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e38ec-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e38ec-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e38ec-110">Définit une autre référence pour une image.</span><span class="sxs-lookup"><span data-stu-id="e38ec-110">Defines an alternate reference for an image.</span></span> <span data-ttu-id="e38ec-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="e38ec-111">Read/write.</span></span> <span data-ttu-id="e38ec-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="e38ec-112">**String**.</span></span>

<span data-ttu-id="e38ec-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="e38ec-113">**Applies To**</span></span>

[<span data-ttu-id="e38ec-114">Complète</span><span class="sxs-lookup"><span data-stu-id="e38ec-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="e38ec-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="e38ec-115">**Tag Syntax**</span></span>

<span data-ttu-id="e38ec-116"><v : *Element* o :althref = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e38ec-116"><v: *element* o:althref=" *expression* "></span></span>

<span data-ttu-id="e38ec-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="e38ec-117">**Script Syntax**</span></span>

<span data-ttu-id="e38ec-118">*Element* . althref = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e38ec-118">*element* .althref="*expression*"</span></span>

<span data-ttu-id="e38ec-119">*expression* = *élément*. althref</span><span class="sxs-lookup"><span data-stu-id="e38ec-119">*expression*=*element*.althref</span></span>

<span data-ttu-id="e38ec-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="e38ec-120">**Remarks**</span></span>

<span data-ttu-id="e38ec-121">Prend en charge la préservation des données PICT via des roundtripping HTML.</span><span class="sxs-lookup"><span data-stu-id="e38ec-121">Supports preservation of PICT data through HTML roundtripping.</span></span> <span data-ttu-id="e38ec-122">Lors de l’écriture HTML, l’autre représentation (les données PICT d’origine si le fichier provient d’Apple Macintosh) est enregistrée.</span><span class="sxs-lookup"><span data-stu-id="e38ec-122">On HTML write, the alternate representation (the original PICT data if the file originated from the Apple Macintosh) is saved.</span></span> <span data-ttu-id="e38ec-123">Lors de la lecture HTML, **AltHRef** est privilégié sur **src**.</span><span class="sxs-lookup"><span data-stu-id="e38ec-123">On HTML read, **AltHRef** is favored over **Src**.</span></span>

<span data-ttu-id="e38ec-124">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="e38ec-124">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="e38ec-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="e38ec-125">**Example**</span></span>

<span data-ttu-id="e38ec-126">Le remplissage de la forme a un **AltHRef** qui pointe vers un fichier nommé myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="e38ec-126">The fill of the shape has an **AltHRef** that points to a file named myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 