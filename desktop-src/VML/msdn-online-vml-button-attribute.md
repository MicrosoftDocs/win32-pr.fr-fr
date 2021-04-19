---
title: Attribut de bouton VML
description: Attribut de bouton VML
ms.assetid: 273024ac-683f-48d2-b6a0-574824f4c05d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f2760fceaf52e3f9ee217d4c3d249fb670a845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509045"
---
# <a name="vml-button-attribute"></a><span data-ttu-id="a7943-103">Attribut de bouton VML</span><span class="sxs-lookup"><span data-stu-id="a7943-103">VML Button Attribute</span></span>

<span data-ttu-id="a7943-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a7943-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a7943-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="a7943-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a7943-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="a7943-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a7943-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="a7943-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a7943-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a7943-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a7943-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a7943-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a7943-110">Détermine si une forme sera traitée comme un bouton.</span><span class="sxs-lookup"><span data-stu-id="a7943-110">Determines whether a shape will be processed as a button.</span></span> <span data-ttu-id="a7943-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="a7943-111">Read/write.</span></span> <span data-ttu-id="a7943-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a7943-112">**VgTriState**.</span></span>

<span data-ttu-id="a7943-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="a7943-113">**Applies To**</span></span>

[<span data-ttu-id="a7943-114">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="a7943-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a7943-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="a7943-115">**Tag Syntax**</span></span>

<span data-ttu-id="a7943-116"><v : *Element* o :Button = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="a7943-116"><v: *element* o:button=" *expression* "></span></span>

<span data-ttu-id="a7943-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="a7943-117">**Remarks**</span></span>

<span data-ttu-id="a7943-118">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="a7943-118">The default is **False**.</span></span> <span data-ttu-id="a7943-119">Si la **valeur est true**, la forme est traitée comme un bouton.</span><span class="sxs-lookup"><span data-stu-id="a7943-119">If **True**, the shape is processed as a button.</span></span>

<span data-ttu-id="a7943-120">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="a7943-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="a7943-121">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="a7943-121">**Example**</span></span>

<span data-ttu-id="a7943-122">La forme est un bouton.</span><span class="sxs-lookup"><span data-stu-id="a7943-122">The shape is a button.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:button="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 