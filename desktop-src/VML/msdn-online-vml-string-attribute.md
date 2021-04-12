---
title: Attribut de chaîne VML
description: Attribut de chaîne VML
ms.assetid: 99609814-29c9-4349-9509-8c91f2aaeff5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf9d6c172b4ca1f5049a3e89528a2333378164f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382224"
---
# <a name="vml-string-attribute"></a><span data-ttu-id="1f1ff-103">Attribut de chaîne VML</span><span class="sxs-lookup"><span data-stu-id="1f1ff-103">VML String Attribute</span></span>

<span data-ttu-id="1f1ff-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1f1ff-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1f1ff-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1f1ff-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1f1ff-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1f1ff-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1f1ff-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1f1ff-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1f1ff-110">Définit le texte du tracé de texte.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-110">Defines the text of the text path.</span></span> <span data-ttu-id="1f1ff-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-111">Read/write.</span></span> <span data-ttu-id="1f1ff-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-112">**String**.</span></span>

<span data-ttu-id="1f1ff-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="1f1ff-113">**Applies To**</span></span>

[<span data-ttu-id="1f1ff-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="1f1ff-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="1f1ff-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="1f1ff-115">**Tag Syntax**</span></span>

<span data-ttu-id="1f1ff-116"><v : *Element* String = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="1f1ff-116"><v: *element* string=" *expression* "></span></span>

<span data-ttu-id="1f1ff-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="1f1ff-117">**Script Syntax**</span></span>

<span data-ttu-id="1f1ff-118">*Element* . String = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="1f1ff-118">*element* .string="*expression*"</span></span>

<span data-ttu-id="1f1ff-119">*expression* = *élément*. String</span><span class="sxs-lookup"><span data-stu-id="1f1ff-119">*expression*=*element*.string</span></span>

<span data-ttu-id="1f1ff-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="1f1ff-120">**Remarks**</span></span>

<span data-ttu-id="1f1ff-121">Vous devez assigner une chaîne de texte pour afficher du texte sur un tracé de texte.</span><span class="sxs-lookup"><span data-stu-id="1f1ff-121">You must assign a text string to display text on a text path.</span></span>

<span data-ttu-id="1f1ff-122">Attribut standard VML</span><span class="sxs-lookup"><span data-stu-id="1f1ff-122">VML Standard Attribute</span></span>

<span data-ttu-id="1f1ff-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="1f1ff-123">**Example**</span></span>

<span data-ttu-id="1f1ff-124">La chaîne qui s’affiche est « VML Text ».</span><span class="sxs-lookup"><span data-stu-id="1f1ff-124">The string that will be displayed is "VML Text".</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 