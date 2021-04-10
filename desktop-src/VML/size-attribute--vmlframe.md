---
title: Attribut Size (VMLFrame)
description: Attribut Size (VMLFrame)
ms.assetid: 95d953fa-cbe2-4ebc-9b23-408347232fee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779b0401c414a3536e22bdb7328b2b08b2fbcf45
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031304"
---
# <a name="size-attribute-vmlframe"></a><span data-ttu-id="a0d9f-103">Attribut Size (VMLFrame)</span><span class="sxs-lookup"><span data-stu-id="a0d9f-103">Size Attribute (VMLFrame)</span></span>

<span data-ttu-id="a0d9f-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a0d9f-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a0d9f-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a0d9f-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a0d9f-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a0d9f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a0d9f-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a0d9f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a0d9f-110">Définit la taille de la zone de découpage du frame.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-110">Defines the size of the clipping region of the frame.</span></span> <span data-ttu-id="a0d9f-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-111">Read/write.</span></span> <span data-ttu-id="a0d9f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-112">**VgVector2D**.</span></span>

<span data-ttu-id="a0d9f-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a0d9f-113">**Applies To**</span></span>

[<span data-ttu-id="a0d9f-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="a0d9f-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="a0d9f-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a0d9f-115">**Tag Syntax**</span></span>

<span data-ttu-id="a0d9f-116"><v : *Element* size = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a0d9f-116"><v: *element* size=" *expression* "></span></span>

<span data-ttu-id="a0d9f-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="a0d9f-117">**Script Syntax**</span></span>

<span data-ttu-id="a0d9f-118">*Element* . Size = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="a0d9f-118">*element* .size="*expression*"</span></span>

<span data-ttu-id="a0d9f-119">*expression* = *Element*. Size</span><span class="sxs-lookup"><span data-stu-id="a0d9f-119">*expression*=*element*.size</span></span>

<span data-ttu-id="a0d9f-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a0d9f-120">**Remarks**</span></span>

<span data-ttu-id="a0d9f-121">La valeur par défaut est 0,0.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-121">The default value is 0,0.</span></span> <span data-ttu-id="a0d9f-122">Notez que la **taille** ne fonctionne que si [clip](msdn-online-vml-clip-attribute.md) a la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-122">Note that **Size** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="a0d9f-123">Dans cet attribut, la taille est définie comme la largeur et la hauteur du cadre.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-123">In this attribute, the size is defined as the width and height of the frame.</span></span>

<span data-ttu-id="a0d9f-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="a0d9f-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a0d9f-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a0d9f-125">**Example**</span></span>

<span data-ttu-id="a0d9f-126">La taille de la zone de découpage sera 50pt, 50pt.</span><span class="sxs-lookup"><span data-stu-id="a0d9f-126">The size of the clipping region will be 50pt, 50pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 