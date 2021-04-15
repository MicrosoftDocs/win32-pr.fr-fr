---
title: MiterLimit VML (attribut)
description: MiterLimit VML (attribut)
ms.assetid: 74744b8a-df73-4a2e-8df7-07fd0e423a47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b2d5b0a186ca416bb6af25df38c4f29964efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463302"
---
# <a name="vml-miterlimit-attribute"></a><span data-ttu-id="d6007-103">MiterLimit VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="d6007-103">VML MiterLimit Attribute</span></span>

<span data-ttu-id="d6007-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d6007-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d6007-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d6007-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d6007-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="d6007-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d6007-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="d6007-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d6007-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d6007-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d6007-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d6007-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d6007-110">Définit le lissage de l’articulation mitre.</span><span class="sxs-lookup"><span data-stu-id="d6007-110">Defines the smoothness of the miter joint.</span></span> <span data-ttu-id="d6007-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d6007-111">Read/write.</span></span> <span data-ttu-id="d6007-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="d6007-112">**VgNumber**.</span></span>

<span data-ttu-id="d6007-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="d6007-113">**Applies To**</span></span>

[<span data-ttu-id="d6007-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="d6007-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="d6007-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="d6007-115">**Tag Syntax**</span></span>

<span data-ttu-id="d6007-116"><v : *Element* MiterLimit = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d6007-116"><v: *element* miterlimit=" *expression* "></span></span>

<span data-ttu-id="d6007-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="d6007-117">**Script Syntax**</span></span>

<span data-ttu-id="d6007-118">*Element* . MiterLimit = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="d6007-118">*element* .miterlimit="*expression*"</span></span>

<span data-ttu-id="d6007-119">*expression* = *élément*. MiterLimit</span><span class="sxs-lookup"><span data-stu-id="d6007-119">*expression*=*element*.miterlimit</span></span>

<span data-ttu-id="d6007-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="d6007-120">**Remarks**</span></span>

<span data-ttu-id="d6007-121">Distance maximale entre le point interne et le point externe d’une jointure.</span><span class="sxs-lookup"><span data-stu-id="d6007-121">The maximum distance between the inner point and outer point of a joint.</span></span> <span data-ttu-id="d6007-122">Ce nombre est un multiple de l’épaisseur de la ligne.</span><span class="sxs-lookup"><span data-stu-id="d6007-122">This number is a multiple of the thickness of the line.</span></span>

<span data-ttu-id="d6007-123">La valeur par défaut est 8.</span><span class="sxs-lookup"><span data-stu-id="d6007-123">The default value is 8.</span></span>

<span data-ttu-id="d6007-124">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="d6007-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d6007-125">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="d6007-125">**Example**</span></span>

<span data-ttu-id="d6007-126">Les jointures sur la polyligne sont mitres avec une limite de 10, c’est-à-dire 5 fois 2 points.</span><span class="sxs-lookup"><span data-stu-id="d6007-126">The joints on the polyline are mitered with a limit of 10, that is, 5 times 2 points.</span></span>


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke miterlimit="5" joinstyle="miter"/>
   </v:polyline>
```



 

 