---
title: Attribut Text-Decoration VML
description: Attribut Text-Decoration VML
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee85007db2dbca04221604cafd79c5d7052c91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941060"
---
# <a name="vml-text-decoration-attribute"></a><span data-ttu-id="f1ca3-103">Attribut Text-Decoration VML</span><span class="sxs-lookup"><span data-stu-id="f1ca3-103">VML Text-Decoration Attribute</span></span>

<span data-ttu-id="f1ca3-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f1ca3-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f1ca3-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f1ca3-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f1ca3-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f1ca3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f1ca3-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f1ca3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f1ca3-110">Définit le style de la décoration de texte.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-110">Defines the style of text decoration.</span></span> <span data-ttu-id="f1ca3-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-111">Read/write.</span></span> <span data-ttu-id="f1ca3-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-112">**String**.</span></span>

<span data-ttu-id="f1ca3-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f1ca3-113">**Applies To**</span></span>

[<span data-ttu-id="f1ca3-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="f1ca3-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="f1ca3-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="f1ca3-115">**Tag Syntax**</span></span>

<span data-ttu-id="f1ca3-116"><v : *Element* style = "text-decoration : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f1ca3-116"><v: *element* style="text-decoration: *expression* "></span></span>

<span data-ttu-id="f1ca3-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="f1ca3-117">**Script Syntax**</span></span>

<span data-ttu-id="f1ca3-118">*Element* . style. TextDecoration = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="f1ca3-118">*element* .style.textdecoration="*expression*"</span></span>

<span data-ttu-id="f1ca3-119">*expression* = *Element*. style. TextDecoration</span><span class="sxs-lookup"><span data-stu-id="f1ca3-119">*expression*=*element*.style.textdecoration</span></span>

<span data-ttu-id="f1ca3-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="f1ca3-120">**Remarks**</span></span>

<span data-ttu-id="f1ca3-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="f1ca3-121">Values include:</span></span>

-   <span data-ttu-id="f1ca3-122">aucun (par défaut)</span><span class="sxs-lookup"><span data-stu-id="f1ca3-122">none (default)</span></span>
-   <span data-ttu-id="f1ca3-123">souligné</span><span class="sxs-lookup"><span data-stu-id="f1ca3-123">underline</span></span>
-   <span data-ttu-id="f1ca3-124">surligné</span><span class="sxs-lookup"><span data-stu-id="f1ca3-124">overline</span></span>
-   <span data-ttu-id="f1ca3-125">ligne par ligne</span><span class="sxs-lookup"><span data-stu-id="f1ca3-125">line-through</span></span>
-   <span data-ttu-id="f1ca3-126">blink</span><span class="sxs-lookup"><span data-stu-id="f1ca3-126">blink</span></span>

<span data-ttu-id="f1ca3-127">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="f1ca3-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="f1ca3-128">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="f1ca3-128">**Example**</span></span>

<span data-ttu-id="f1ca3-129">Le texte est souligné.</span><span class="sxs-lookup"><span data-stu-id="f1ca3-129">The text will be underlined.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 