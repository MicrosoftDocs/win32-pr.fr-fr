---
title: Attribut de suppression VML
description: Attribut de suppression VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842654"
---
# <a name="vml-trim-attribute"></a><span data-ttu-id="6ee5a-103">Attribut de suppression VML</span><span class="sxs-lookup"><span data-stu-id="6ee5a-103">VML Trim Attribute</span></span>

<span data-ttu-id="6ee5a-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="6ee5a-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="6ee5a-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="6ee5a-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="6ee5a-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="6ee5a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="6ee5a-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="6ee5a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="6ee5a-110">Détermine si l’espace supplémentaire est supprimé au-dessus et au-dessous du texte.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-110">Determines whether extra space is removed above and below the text.</span></span> <span data-ttu-id="6ee5a-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-111">Read/write.</span></span> <span data-ttu-id="6ee5a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-112">**VgTriState**.</span></span>

<span data-ttu-id="6ee5a-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="6ee5a-113">**Applies To**</span></span>

[<span data-ttu-id="6ee5a-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="6ee5a-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="6ee5a-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="6ee5a-115">**Tag Syntax**</span></span>

<span data-ttu-id="6ee5a-116"><v : *Element* style = "Trim : *expression* " ></span><span class="sxs-lookup"><span data-stu-id="6ee5a-116"><v: *element* style="trim: *expression* "></span></span>

<span data-ttu-id="6ee5a-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="6ee5a-117">**Script Syntax**</span></span>

<span data-ttu-id="6ee5a-118">*Element* . style. Trim = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="6ee5a-118">*element* .style.trim="*expression*"</span></span>

<span data-ttu-id="6ee5a-119">*expression* = *Element*. style. Trim</span><span class="sxs-lookup"><span data-stu-id="6ee5a-119">*expression*=*element*.style.trim</span></span>

<span data-ttu-id="6ee5a-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="6ee5a-120">**Remarks**</span></span>

<span data-ttu-id="6ee5a-121">Si la **valeur est true**, l’espace réservé pour les hampes supérieures et les descendants est supprimé.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-121">If **True**, space reserved for ascenders and descenders is removed.</span></span> <span data-ttu-id="6ee5a-122">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-122">The default value is **False**.</span></span>

<span data-ttu-id="6ee5a-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="6ee5a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="6ee5a-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="6ee5a-124">**Example**</span></span>

<span data-ttu-id="6ee5a-125">L’espace supplémentaire au-dessus et au-dessous est tronqué.</span><span class="sxs-lookup"><span data-stu-id="6ee5a-125">The extra space above and below is trimmed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 