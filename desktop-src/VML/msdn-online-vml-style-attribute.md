---
title: Attribut de style VML
description: Attribut de style VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463190"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="2143b-103">Attribut de style VML</span><span class="sxs-lookup"><span data-stu-id="2143b-103">VML Style Attribute</span></span>

<span data-ttu-id="2143b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2143b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2143b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="2143b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2143b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="2143b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2143b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="2143b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2143b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2143b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2143b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2143b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2143b-110">Définit le style du frame.</span><span class="sxs-lookup"><span data-stu-id="2143b-110">Defines the style of the frame.</span></span> <span data-ttu-id="2143b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="2143b-111">Read/write.</span></span> <span data-ttu-id="2143b-112">**Chaîne**.</span><span class="sxs-lookup"><span data-stu-id="2143b-112">**String**.</span></span>

<span data-ttu-id="2143b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="2143b-113">**Applies To**</span></span>

[<span data-ttu-id="2143b-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="2143b-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="2143b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="2143b-115">**Tag Syntax**</span></span>

<span data-ttu-id="2143b-116"><v : *Element* style = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2143b-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="2143b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="2143b-117">**Script Syntax**</span></span>

<span data-ttu-id="2143b-118">*Element* . style = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="2143b-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="2143b-119">*expression* = *Element*. style</span><span class="sxs-lookup"><span data-stu-id="2143b-119">*expression*=*element*.style</span></span>

<span data-ttu-id="2143b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="2143b-120">**Remarks**</span></span>

<span data-ttu-id="2143b-121">Cet attribut utilise les attributs de style CSS normaux pour le positionnement.</span><span class="sxs-lookup"><span data-stu-id="2143b-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="2143b-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="2143b-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="2143b-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="2143b-123">**Example**</span></span>

<span data-ttu-id="2143b-124">Le style définit la position réelle du frame.</span><span class="sxs-lookup"><span data-stu-id="2143b-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 