---
title: Attribut Opacity (Stroke) (VML)
description: Attribut Opacity (Stroke) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463666"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="7fe85-103">Attribut Opacity (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="7fe85-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="7fe85-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7fe85-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7fe85-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="7fe85-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7fe85-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="7fe85-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7fe85-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="7fe85-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7fe85-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7fe85-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7fe85-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7fe85-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7fe85-110">Définit la quantité de transparence d’un trait.</span><span class="sxs-lookup"><span data-stu-id="7fe85-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="7fe85-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="7fe85-111">Read/write.</span></span> <span data-ttu-id="7fe85-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="7fe85-112">**VgFraction**.</span></span>

<span data-ttu-id="7fe85-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="7fe85-113">**Applies To**</span></span>

[<span data-ttu-id="7fe85-114">Stroke</span><span class="sxs-lookup"><span data-stu-id="7fe85-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="7fe85-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="7fe85-115">**Tag Syntax**</span></span>

<span data-ttu-id="7fe85-116"><v : *Element* Opacity = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="7fe85-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="7fe85-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="7fe85-117">**Script Syntax**</span></span>

<span data-ttu-id="7fe85-118">*Element* . Opacity = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="7fe85-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="7fe85-119">*expression* = *Element*. Opacity</span><span class="sxs-lookup"><span data-stu-id="7fe85-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="7fe85-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="7fe85-120">**Remarks**</span></span>

<span data-ttu-id="7fe85-121">La valeur par défaut est 1,0.</span><span class="sxs-lookup"><span data-stu-id="7fe85-121">The default value is 1.0.</span></span>

<span data-ttu-id="7fe85-122">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="7fe85-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="7fe85-123">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="7fe85-123">**Example**</span></span>

<span data-ttu-id="7fe85-124">Le trait est transparent 50%.</span><span class="sxs-lookup"><span data-stu-id="7fe85-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 