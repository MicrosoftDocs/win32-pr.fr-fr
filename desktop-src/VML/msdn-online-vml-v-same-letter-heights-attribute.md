---
title: Attribut VML V-caractères de hauteur identique
description: Attribut VML V-caractères de hauteur identique
ms.assetid: f06c0a50-1de1-47d8-8b94-01fe0599ed59
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6d155c3c72eb67718edd33ae601d22f8e5d074a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727764"
---
# <a name="vml-v-same-letter-heights-attribute"></a><span data-ttu-id="b2439-103">Attribut VML V-caractères de hauteur identique</span><span class="sxs-lookup"><span data-stu-id="b2439-103">VML V-Same-Letter-Heights Attribute</span></span>

<span data-ttu-id="b2439-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b2439-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b2439-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="b2439-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b2439-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="b2439-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b2439-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="b2439-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b2439-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b2439-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b2439-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b2439-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b2439-110">Détermine si toutes les lettres auront la même hauteur, quel que soit le cas initial.</span><span class="sxs-lookup"><span data-stu-id="b2439-110">Determines whether all letters will be the same height regardless of initial case.</span></span> <span data-ttu-id="b2439-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b2439-111">Read/write.</span></span> <span data-ttu-id="b2439-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="b2439-112">**VgTriState**.</span></span>

<span data-ttu-id="b2439-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="b2439-113">**Applies To**</span></span>

[<span data-ttu-id="b2439-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="b2439-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="b2439-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="b2439-115">**Tag Syntax**</span></span>

<span data-ttu-id="b2439-116"><v : *Element* style = "v-after-letter-largers : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="b2439-116"><v: *element* style="v-same-letter-heights: *expression* "></span></span>

<span data-ttu-id="b2439-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="b2439-117">**Script Syntax**</span></span>

<span data-ttu-id="b2439-118">*Element* . style. v-comflat-hauteur = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="b2439-118">*element* .style.v-same-letter-heights="*expression*"</span></span>

<span data-ttu-id="b2439-119">*expression* = *Element*. style. v-Lettres identiques</span><span class="sxs-lookup"><span data-stu-id="b2439-119">*expression*=*element*.style.v-same-letter-heights</span></span>

<span data-ttu-id="b2439-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="b2439-120">**Remarks**</span></span>

<span data-ttu-id="b2439-121">Si la **valeur est true**, les lettres minuscules sont étirées jusqu’à la hauteur des lettres majuscules.</span><span class="sxs-lookup"><span data-stu-id="b2439-121">If **True**, the lowercase letters are stretched to the height of the uppercase letters.</span></span> <span data-ttu-id="b2439-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="b2439-122">The default value is **False**.</span></span>

<span data-ttu-id="b2439-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="b2439-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b2439-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="b2439-124">**Example**</span></span>

<span data-ttu-id="b2439-125">Toutes les lettres auront la même hauteur, quelle que soit la casse.</span><span class="sxs-lookup"><span data-stu-id="b2439-125">All letters will be the same height, regardless of case.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-same-letter-heights:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 