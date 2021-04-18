---
title: LockRotationCenter VML (attribut)
description: LockRotationCenter VML (attribut)
ms.assetid: 80b822d3-9122-475b-88ca-7019daa5de77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49dd6ccada3f713f1cf2384a96f131c9a7714db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511904"
---
# <a name="vml-lockrotationcenter-attribute"></a><span data-ttu-id="c5b4b-103">LockRotationCenter VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="c5b4b-103">VML LockRotationCenter Attribute</span></span>

<span data-ttu-id="c5b4b-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5b4b-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5b4b-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5b4b-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5b4b-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5b4b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5b4b-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5b4b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c5b4b-110">Détermine si la rotation de l’objet extrudé est spécifiée par l’attribut [RotationAngle](msdn-online-vml-rotationangle-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c5b4b-110">Determines whether the rotation of the extruded object is specified by the [RotationAngle](msdn-online-vml-rotationangle-attribute.md) attribute.</span></span> <span data-ttu-id="c5b4b-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-111">Read/write.</span></span> <span data-ttu-id="c5b4b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-112">**VgTriState**.</span></span>

<span data-ttu-id="c5b4b-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="c5b4b-113">**Applies To**</span></span>

[<span data-ttu-id="c5b4b-114">Extrusion</span><span class="sxs-lookup"><span data-stu-id="c5b4b-114">Extrusion</span></span>](msdn-online-vml-extrusion-element.md)

<span data-ttu-id="c5b4b-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="c5b4b-115">**Tag Syntax**</span></span>

<span data-ttu-id="c5b4b-116"><o : *Element* lockrotationcenter = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c5b4b-116"><o: *element* lockrotationcenter=" *expression* "></span></span>

<span data-ttu-id="c5b4b-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="c5b4b-117">**Script Syntax**</span></span>

<span data-ttu-id="c5b4b-118">*Element* . lockrotationcenter = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="c5b4b-118">*element* .lockrotationcenter="*expression*"</span></span>

<span data-ttu-id="c5b4b-119">*expression* = *élément*. lockrotationcenter</span><span class="sxs-lookup"><span data-stu-id="c5b4b-119">*expression*=*element*.lockrotationcenter</span></span>

<span data-ttu-id="c5b4b-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="c5b4b-120">**Remarks**</span></span>

<span data-ttu-id="c5b4b-121">Si la **valeur est false**, la rotation est spécifiée par l’attribut [orientation](msdn-online-vml-orientation-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="c5b4b-121">If **False**, the rotation is specified by the [Orientation](msdn-online-vml-orientation-attribute.md) attribute.</span></span> <span data-ttu-id="c5b4b-122">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="c5b4b-122">The default is **True**.</span></span>

<span data-ttu-id="c5b4b-123">Notez les points suivants :</span><span class="sxs-lookup"><span data-stu-id="c5b4b-123">Note that:</span></span>


```HTML
   <o:extrusion lockrotationcenter="false" orientationangle="45" orientation="(0,1,0)"/>
```



<span data-ttu-id="c5b4b-124">est identique à :</span><span class="sxs-lookup"><span data-stu-id="c5b4b-124">is the same as:</span></span>


```HTML
   <o:extrusion lockrotationcenter="true" rotationangle="45"/>
```



<span data-ttu-id="c5b4b-125">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c5b4b-125">*Microsoft Office Extensions Attribute*</span></span>

 

 