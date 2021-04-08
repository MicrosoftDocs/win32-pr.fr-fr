---
title: Attribut HRef (ImageData) (VML)
description: Attribut HRef (ImageData) (VML)
ms.assetid: vs|vml|~\shape\image\image_href.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4ea1c5a5eb4c37773d012c1ff888aa372cb7717
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727429"
---
# <a name="href-attribute-imagedatavml"></a><span data-ttu-id="59127-103">Attribut HRef (ImageData) (VML)</span><span class="sxs-lookup"><span data-stu-id="59127-103">HRef Attribute (ImageData)(VML)</span></span>

<span data-ttu-id="59127-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="59127-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="59127-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="59127-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="59127-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="59127-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="59127-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="59127-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="59127-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="59127-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="59127-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="59127-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="59127-110">Définit une URL pour une image.</span><span class="sxs-lookup"><span data-stu-id="59127-110">Defines a URL for an image.</span></span> <span data-ttu-id="59127-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="59127-111">Read/write.</span></span> <span data-ttu-id="59127-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="59127-112">**String**.</span></span>

<span data-ttu-id="59127-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="59127-113">**Applies To**</span></span>

[<span data-ttu-id="59127-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="59127-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="59127-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="59127-115">**Tag Syntax**</span></span>

<span data-ttu-id="59127-116"><v : *Element* o :href = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="59127-116"><v: *element* o:href=" *expression* "></span></span>

<span data-ttu-id="59127-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="59127-117">**Script Syntax**</span></span>

<span data-ttu-id="59127-118">*Element* . href = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="59127-118">*element* .href="*expression*"</span></span>

<span data-ttu-id="59127-119">*expression* = *élément*. href</span><span class="sxs-lookup"><span data-stu-id="59127-119">*expression*=*element*.href</span></span>

<span data-ttu-id="59127-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="59127-120">**Remarks**</span></span>

<span data-ttu-id="59127-121">Lorsque l’utilisateur clique sur la forme, le navigateur charge l’URL.</span><span class="sxs-lookup"><span data-stu-id="59127-121">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="59127-122">L’attribut **href** est similaire à l’attribut HTML **href** standard des points d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="59127-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="59127-123">L’utilisation de cet attribut facilite la création d’images buttonswith sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="59127-123">Using this attribute makes it easy to create buttonswith images on a Web page.</span></span>

<span data-ttu-id="59127-124">Cet attribut est utilisé par Microsoft Office uniquement si une image a été liée et incorporée. Microsoft Word dispose d’une interface utilisateur pour l’insertion d’images de cette façon.</span><span class="sxs-lookup"><span data-stu-id="59127-124">This attribute is used by Microsoft Office only if a picture has been linked and embedded.Microsoft Word has a user interface for inserting pictures this way.</span></span>

<span data-ttu-id="59127-125">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="59127-125">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="59127-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="59127-126">**Example**</span></span>

<span data-ttu-id="59127-127">Quand l’utilisateur clique sur l’image, le navigateur charge la page d’accueil de Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="59127-127">When the image is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata o:href="https://www.microsoft.com" src="kids.jpg"/>
   </v:shape>
```



 

 