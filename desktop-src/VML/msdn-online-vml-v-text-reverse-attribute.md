---
title: VML V-Text-inversé (attribut)
description: VML V-Text-inversé (attribut)
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031545"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="341c4-103">VML V-Text-inversé (attribut)</span><span class="sxs-lookup"><span data-stu-id="341c4-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="341c4-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="341c4-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="341c4-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="341c4-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="341c4-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="341c4-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="341c4-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="341c4-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="341c4-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="341c4-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="341c4-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="341c4-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="341c4-110">Détermine si l’ordre de la disposition des lignes est inversé.</span><span class="sxs-lookup"><span data-stu-id="341c4-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="341c4-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="341c4-111">Read/write.</span></span> <span data-ttu-id="341c4-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="341c4-112">**VgTriState**.</span></span>

<span data-ttu-id="341c4-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="341c4-113">**Applies To**</span></span>

[<span data-ttu-id="341c4-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="341c4-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="341c4-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="341c4-115">**Tag Syntax**</span></span>

<span data-ttu-id="341c4-116"><v : *Element* style = "v-Text-inverser : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="341c4-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="341c4-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="341c4-117">**Script Syntax**</span></span>

<span data-ttu-id="341c4-118">*Element* . style. v-Text-inversion = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="341c4-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="341c4-119">*expression* = *Element*. style. v-Text-inversé</span><span class="sxs-lookup"><span data-stu-id="341c4-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="341c4-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="341c4-120">**Remarks**</span></span>

<span data-ttu-id="341c4-121">Si la **valeur est true**, l’ordre de la disposition des lignes est inversé.</span><span class="sxs-lookup"><span data-stu-id="341c4-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="341c4-122">Cet attribut est utilisé pour la disposition de texte verticale.</span><span class="sxs-lookup"><span data-stu-id="341c4-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="341c4-123">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="341c4-123">The default value is **False**.</span></span>

<span data-ttu-id="341c4-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="341c4-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="341c4-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="341c4-125">**Example**</span></span>

<span data-ttu-id="341c4-126">L’ordre de la disposition est inversé.</span><span class="sxs-lookup"><span data-stu-id="341c4-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 