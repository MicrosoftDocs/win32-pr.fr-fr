---
title: BWMode VML (attribut)
description: BWMode VML (attribut)
ms.assetid: 929daebb-c402-46a0-9abc-b91c4ebda7fa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f595159398e32fdb1c80ad5d949ef48758aea95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728293"
---
# <a name="vml-bwmode-attribute"></a><span data-ttu-id="71157-103">BWMode VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="71157-103">VML BWMode Attribute</span></span>

<span data-ttu-id="71157-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="71157-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="71157-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="71157-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="71157-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="71157-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="71157-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="71157-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="71157-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="71157-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="71157-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="71157-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="71157-110">Détermine la façon dont une forme s’affiche pour les périphériques de sortie noir et blanc.</span><span class="sxs-lookup"><span data-stu-id="71157-110">Determines how a shape will render for black-and-white output devices.</span></span> <span data-ttu-id="71157-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="71157-111">Read/write.</span></span> <span data-ttu-id="71157-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span><span class="sxs-lookup"><span data-stu-id="71157-112">[VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).</span></span>

<span data-ttu-id="71157-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="71157-113">**Applies To**</span></span>

[<span data-ttu-id="71157-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="71157-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="71157-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="71157-115">**Tag Syntax**</span></span>

<span data-ttu-id="71157-116"><v : *Element* o :bwmode = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="71157-116"><v: *element* o:bwmode=" *expression* "></span></span>

<span data-ttu-id="71157-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="71157-117">**Remarks**</span></span>

<span data-ttu-id="71157-118">Quand une forme est imprimée sur une imprimante noir et blanc, ou affichée dans une vue en noir et blanc dans une application, plusieurs options sont possibles.</span><span class="sxs-lookup"><span data-stu-id="71157-118">When a shape is printed on a black-and-white printer or displayed in a black-and-white view in an application, several options are possible.</span></span> <span data-ttu-id="71157-119">Pour plus d’informations sur les valeurs de cet attribut, consultez la rubrique [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) .</span><span class="sxs-lookup"><span data-stu-id="71157-119">For more information about the values of this attribute, see the [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) topic.</span></span> <span data-ttu-id="71157-120">La valeur par défaut est **auto**.</span><span class="sxs-lookup"><span data-stu-id="71157-120">The default value is **auto**.</span></span>

<span data-ttu-id="71157-121">Si **auto** est spécifié, [BWNormal](msdn-online-vml-bwnormal-attribute.md) est utilisé pour déterminer le comportement de sortie noir et blanc normale, tandis que [BWPure](msdn-online-vml-bwpure-attribute.md) est utilisé pour déterminer le comportement de sortie en noir et blanc pur.</span><span class="sxs-lookup"><span data-stu-id="71157-121">If **auto** is specified, [BWNormal](msdn-online-vml-bwnormal-attribute.md) is used to determine the behavior for normal black-and-white output, and [BWPure](msdn-online-vml-bwpure-attribute.md) is used to determine the behavior for pure black-and-white output.</span></span>

<span data-ttu-id="71157-122">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="71157-122">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="71157-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="71157-123">**Example**</span></span>

<span data-ttu-id="71157-124">Le mode noir et blanc de la forme est **auto**.</span><span class="sxs-lookup"><span data-stu-id="71157-124">The black-and-white mode of the shape is **auto**.</span></span>


```HTML
   <v:rect id="myrect" fillcolor="red" o:bwmode="auto"
     style="top:1;left:1;width:20;height:20"/>
```



 

 