---
title: Attribut HRef (Shape) (VML)
description: Attribut HRef (Shape) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031766"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="0a0d3-103">Attribut HRef (Shape) (VML)</span><span class="sxs-lookup"><span data-stu-id="0a0d3-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="0a0d3-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0a0d3-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0a0d3-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0a0d3-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0a0d3-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0a0d3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0a0d3-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0a0d3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0a0d3-110">Définit une URL pour une forme.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-110">Defines a URL for a shape.</span></span> <span data-ttu-id="0a0d3-111">Lorsque l’utilisateur clique sur la forme, le navigateur charge l’URL.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="0a0d3-112">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-112">Read/write.</span></span> <span data-ttu-id="0a0d3-113">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-113">**String**.</span></span>

<span data-ttu-id="0a0d3-114">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="0a0d3-114">**Applies To**</span></span>

[<span data-ttu-id="0a0d3-115">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="0a0d3-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0a0d3-116">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="0a0d3-116">**Tag Syntax**</span></span>

<span data-ttu-id="0a0d3-117"><v : *Element* href = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="0a0d3-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="0a0d3-118">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="0a0d3-118">**Script Syntax**</span></span>

<span data-ttu-id="0a0d3-119">*Element* . href = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="0a0d3-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="0a0d3-120">*expression* = *élément*. href</span><span class="sxs-lookup"><span data-stu-id="0a0d3-120">*expression*=*element*.href</span></span>

<span data-ttu-id="0a0d3-121">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="0a0d3-121">**Remarks**</span></span>

<span data-ttu-id="0a0d3-122">L’attribut **href** est similaire à l’attribut HTML **href** standard des points d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="0a0d3-123">L’utilisation de la fonction **href** vous permet de créer facilement des boutons intéressants sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="0a0d3-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="0a0d3-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="0a0d3-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="0a0d3-125">**Example**</span></span>

<span data-ttu-id="0a0d3-126">Quand vous cliquez sur le rectangle, le navigateur charge la page d’accueil de Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="0a0d3-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="0a0d3-127">[Exemple d’attribut href](/previous-versions/bb229672(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0a0d3-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="0a0d3-128">(Nécessite Microsoft Internet Explorer 5 ou version ultérieure.)</span><span class="sxs-lookup"><span data-stu-id="0a0d3-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 