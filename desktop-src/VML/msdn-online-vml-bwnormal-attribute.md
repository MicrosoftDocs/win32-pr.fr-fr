---
title: BWNormal VML (attribut)
description: BWNormal VML (attribut)
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2fd14a50fc28c47154611b9a996fe0ef035f70
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031448"
---
# <a name="vml-bwnormal-attribute"></a><span data-ttu-id="aa9bb-103">BWNormal VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="aa9bb-103">VML BWNormal Attribute</span></span>

<span data-ttu-id="aa9bb-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="aa9bb-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="aa9bb-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="aa9bb-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="aa9bb-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="aa9bb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="aa9bb-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="aa9bb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="aa9bb-110">Définit le mode noir et blanc pour les périphériques de sortie noir et blanc normaux.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-110">Defines the black-and-white mode for normal black-and-white output devices.</span></span> <span data-ttu-id="aa9bb-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-111">Read/write.</span></span> <span data-ttu-id="aa9bb-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="aa9bb-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="aa9bb-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="aa9bb-113">**Applies To**</span></span>

[<span data-ttu-id="aa9bb-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="aa9bb-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="aa9bb-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="aa9bb-115">**Tag Syntax**</span></span>

<span data-ttu-id="aa9bb-116"><v : *Element* o :bwnormal = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="aa9bb-116"><v: *element* o:bwnormal=" *expression* "></span></span>

<span data-ttu-id="aa9bb-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="aa9bb-117">**Remarks**</span></span>

<span data-ttu-id="aa9bb-118">Quand [BWMode](msdn-online-vml-bwmode-attribute.md) est défini sur **auto**, cet attribut est utilisé pour déterminer comment afficher la forme en noir et blanc normal.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-118">When [BWMode](msdn-online-vml-bwmode-attribute.md) is set to **auto**, this attribute is used to determine how to render the shape in normal black and white.</span></span>

<span data-ttu-id="aa9bb-119">Pour plus d’informations sur les valeurs de cet attribut, consultez la rubrique [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9bb-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="aa9bb-120">La valeur par défaut est **auto**.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-120">The default value is **auto**.</span></span>

<span data-ttu-id="aa9bb-121">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="aa9bb-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="aa9bb-122">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="aa9bb-122">**Example**</span></span>

<span data-ttu-id="aa9bb-123">La forme est traitée comme une image en nuances de gris pour une sortie noir et blanc normale.</span><span class="sxs-lookup"><span data-stu-id="aa9bb-123">The shape is processed as a grayscale image for normal black-and-white output.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 