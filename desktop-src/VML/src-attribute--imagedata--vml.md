---
title: Attribut SRC (ImageData) (VML)
description: Attribut SRC (ImageData) (VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca630606ba476356a046b0079da4c0593f76473
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031303"
---
# <a name="src-attribute-imagedatavml"></a><span data-ttu-id="36ea2-103">Attribut SRC (ImageData) (VML)</span><span class="sxs-lookup"><span data-stu-id="36ea2-103">Src Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="36ea2-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="36ea2-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="36ea2-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="36ea2-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="36ea2-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="36ea2-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="36ea2-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="36ea2-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="36ea2-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="36ea2-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="36ea2-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="36ea2-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="36ea2-110">Définit une source pour l’image.</span><span class="sxs-lookup"><span data-stu-id="36ea2-110">Defines a source for the image.</span></span> <span data-ttu-id="36ea2-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="36ea2-111">Read/write.</span></span> <span data-ttu-id="36ea2-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="36ea2-112">**String**.</span></span>

<span data-ttu-id="36ea2-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="36ea2-113">**Applies To**</span></span>

[<span data-ttu-id="36ea2-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="36ea2-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="36ea2-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="36ea2-115">**Tag Syntax**</span></span>

<span data-ttu-id="36ea2-116"><v : *Element* SRC = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="36ea2-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="36ea2-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="36ea2-117">**Script Syntax**</span></span>

<span data-ttu-id="36ea2-118">*Element* . src = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="36ea2-118">*element* .src="*expression*"</span></span>

<span data-ttu-id="36ea2-119">*expression* = *élément*. SRC</span><span class="sxs-lookup"><span data-stu-id="36ea2-119">*expression*=*element*.src</span></span>

<span data-ttu-id="36ea2-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="36ea2-120">**Remarks**</span></span>

<span data-ttu-id="36ea2-121">Cet attribut doit toujours être utilisé avec l’élément [ImageData](msdn-online-vml-imagedata-element.md) et pointer vers des données d’image valides pour qu’une image soit affichée.</span><span class="sxs-lookup"><span data-stu-id="36ea2-121">This attribute must always be used with the [ImageData](msdn-online-vml-imagedata-element.md) element and point to valid image data for a picture to be displayed.</span></span> <span data-ttu-id="36ea2-122">Si cet attribut apparaît sans [href](https://www.bing.com/search?q=HRef) ou [title](title-attribute--imagedata--vml.md), l’image est liée.</span><span class="sxs-lookup"><span data-stu-id="36ea2-122">If this attribute appears without [HRef](https://www.bing.com/search?q=HRef) or [Title](title-attribute--imagedata--vml.md), then the image is linked.</span></span>

<span data-ttu-id="36ea2-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="36ea2-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="36ea2-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="36ea2-124">**Example**</span></span>

<span data-ttu-id="36ea2-125">La source de l’image est un fichier nommé « kids.jpg ».</span><span class="sxs-lookup"><span data-stu-id="36ea2-125">The source of the image is a file named "kids.jpg".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 