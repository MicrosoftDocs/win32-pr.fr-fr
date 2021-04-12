---
title: StartArrowLength VML (attribut)
description: StartArrowLength VML (attribut)
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382225"
---
# <a name="vml-startarrowlength-attribute"></a><span data-ttu-id="cd475-103">StartArrowLength VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="cd475-103">VML StartArrowLength Attribute</span></span>

<span data-ttu-id="cd475-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cd475-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cd475-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="cd475-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cd475-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="cd475-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cd475-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="cd475-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cd475-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cd475-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cd475-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cd475-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cd475-110">Définit la longueur de la flèche pour le début d’une ligne.</span><span class="sxs-lookup"><span data-stu-id="cd475-110">Defines the arrowhead length for the start of a line.</span></span> <span data-ttu-id="cd475-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cd475-111">Read/write.</span></span> <span data-ttu-id="cd475-112">**VgArrowheadLength**.</span><span class="sxs-lookup"><span data-stu-id="cd475-112">**VgArrowheadLength**.</span></span>

<span data-ttu-id="cd475-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="cd475-113">**Applies To**</span></span>

[<span data-ttu-id="cd475-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="cd475-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="cd475-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="cd475-115">**Tag Syntax**</span></span>

<span data-ttu-id="cd475-116"><v : *Element* startarrowlength = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cd475-116"><v: *element* startarrowlength=" *expression* "></span></span>

<span data-ttu-id="cd475-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="cd475-117">**Script Syntax**</span></span>

<span data-ttu-id="cd475-118">*Element* . startarrowlength = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="cd475-118">*element* .startarrowlength="*expression*"</span></span>

<span data-ttu-id="cd475-119">*expression* = *élément*. startarrowlength</span><span class="sxs-lookup"><span data-stu-id="cd475-119">*expression*=*element*.startarrowlength</span></span>

<span data-ttu-id="cd475-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="cd475-120">**Remarks**</span></span>

<span data-ttu-id="cd475-121">Ces valeurs comprennent :</span><span class="sxs-lookup"><span data-stu-id="cd475-121">Values include:</span></span>

-   <span data-ttu-id="cd475-122">Court</span><span class="sxs-lookup"><span data-stu-id="cd475-122">Short</span></span>
-   <span data-ttu-id="cd475-123">Moyenne (par défaut)</span><span class="sxs-lookup"><span data-stu-id="cd475-123">Medium (default)</span></span>
-   <span data-ttu-id="cd475-124">Long</span><span class="sxs-lookup"><span data-stu-id="cd475-124">Long</span></span>

<span data-ttu-id="cd475-125">Attribut standard VML</span><span class="sxs-lookup"><span data-stu-id="cd475-125">VML Standard Attribute</span></span>

<span data-ttu-id="cd475-126">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="cd475-126">**Example**</span></span>

<span data-ttu-id="cd475-127">Une ligne est dessinée avec une petite flèche classique au début du trait.</span><span class="sxs-lookup"><span data-stu-id="cd475-127">A line is drawn with a short classic arrowhead on the start of the stroke.</span></span>


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 