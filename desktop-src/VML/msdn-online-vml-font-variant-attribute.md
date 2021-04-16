---
title: Attribut Font-Variant VML
description: Attribut Font-Variant VML
ms.assetid: f58bf3e0-e285-474c-83b1-203fce4f3c3a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 243f8b36d36d8bb9b210a916cef239cda6061e0f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382023"
---
# <a name="vml-font-variant-attribute"></a><span data-ttu-id="50634-103">Attribut Font-Variant VML</span><span class="sxs-lookup"><span data-stu-id="50634-103">VML Font-Variant Attribute</span></span>

<span data-ttu-id="50634-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="50634-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="50634-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="50634-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="50634-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="50634-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="50634-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="50634-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="50634-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="50634-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="50634-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="50634-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="50634-110">Définit le style de variante d’une police.</span><span class="sxs-lookup"><span data-stu-id="50634-110">Defines the variant style of a font.</span></span> <span data-ttu-id="50634-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="50634-111">Read/write.</span></span> <span data-ttu-id="50634-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="50634-112">**String**.</span></span>

<span data-ttu-id="50634-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="50634-113">**Applies To**</span></span>

[<span data-ttu-id="50634-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="50634-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="50634-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="50634-115">**Tag Syntax**</span></span>

<span data-ttu-id="50634-116"><v : *Element* style = "font-variant : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="50634-116"><v: *element* style="font-variant: *expression* "></span></span>

<span data-ttu-id="50634-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="50634-117">**Script Syntax**</span></span>

<span data-ttu-id="50634-118">*Element* . style. fontVariant = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="50634-118">*element* .style.fontvariant="*expression*"</span></span>

<span data-ttu-id="50634-119">*expression* = *Element*. style. fontVariant</span><span class="sxs-lookup"><span data-stu-id="50634-119">*expression*=*element*.style.fontvariant</span></span>

<span data-ttu-id="50634-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="50634-120">**Remarks**</span></span>

<span data-ttu-id="50634-121">Les valeurs sont :</span><span class="sxs-lookup"><span data-stu-id="50634-121">The values are:</span></span>

-   <span data-ttu-id="50634-122">normal (par défaut)</span><span class="sxs-lookup"><span data-stu-id="50634-122">normal (default)</span></span>
-   <span data-ttu-id="50634-123">petites majuscules</span><span class="sxs-lookup"><span data-stu-id="50634-123">small-caps</span></span>

<span data-ttu-id="50634-124">Les valeurs sont les mêmes que les attributs de style HTML standard.</span><span class="sxs-lookup"><span data-stu-id="50634-124">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="50634-125">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="50634-125">*VML Standard Attribute*</span></span>

<span data-ttu-id="50634-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="50634-126">**Example**</span></span>

<span data-ttu-id="50634-127">La police est rendue sous la forme de petites lettres majuscules.</span><span class="sxs-lookup"><span data-stu-id="50634-127">The font is rendered as small capital letters.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal small-caps normal 36pt Arial"/>
   </v:line>
```



 

 