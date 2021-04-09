---
title: Attribut VML V-Rotate-Letters
description: Attribut VML V-Rotate-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9397fe8a819e9f4c8b517e1ac92e0094ad8e4458
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101709"
---
# <a name="vml-v-rotate-letters-attribute"></a><span data-ttu-id="5bbd4-103">Attribut VML V-Rotate-Letters</span><span class="sxs-lookup"><span data-stu-id="5bbd4-103">VML V-Rotate-Letters Attribute</span></span>

<span data-ttu-id="5bbd4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5bbd4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5bbd4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5bbd4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5bbd4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5bbd4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5bbd4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5bbd4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5bbd4-110">Détermine si les lettres du texte sont pivotées.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-110">Determines whether the letters of the text are rotated.</span></span> <span data-ttu-id="5bbd4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-111">Read/write.</span></span> <span data-ttu-id="5bbd4-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-112">**VgTriState**.</span></span>

<span data-ttu-id="5bbd4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5bbd4-113">**Applies To**</span></span>

[<span data-ttu-id="5bbd4-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="5bbd4-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="5bbd4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="5bbd4-115">**Tag Syntax**</span></span>

<span data-ttu-id="5bbd4-116"><v : *Element* style = "v-Rotate-Letters : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5bbd4-116"><v: *element* style="v-rotate-letters: *expression* "></span></span>

<span data-ttu-id="5bbd4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="5bbd4-117">**Script Syntax**</span></span>

<span data-ttu-id="5bbd4-118">*Element* . style. v-Rotate-letters = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5bbd4-118">*element* .style.v-rotate-letters="*expression*"</span></span>

<span data-ttu-id="5bbd4-119">*expression* = *Element*. style. v-Rotate-lettres</span><span class="sxs-lookup"><span data-stu-id="5bbd4-119">*expression*=*element*.style.v-rotate-letters</span></span>

<span data-ttu-id="5bbd4-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5bbd4-120">**Remarks**</span></span>

<span data-ttu-id="5bbd4-121">Si la **valeur est true**, les lettres du texte sont pivotées de 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-121">If **True**, the letters of the text are rotated 90 degrees.</span></span> <span data-ttu-id="5bbd4-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-122">The default value is **False**.</span></span>

<span data-ttu-id="5bbd4-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="5bbd4-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5bbd4-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="5bbd4-124">**Example**</span></span>

<span data-ttu-id="5bbd4-125">Les lettres sont pivotées de 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="5bbd4-125">The letters are rotated 90 degrees.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 