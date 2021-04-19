---
title: On Attribute (Fill) (VML)
description: On Attribute (Fill) (VML)
ms.assetid: 9b7d42e5-4fd9-402d-8d1f-af01f6577475
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79e25e805be23b4678b1be828b711365a8624f10
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511705"
---
# <a name="on-attribute-fillvml"></a><span data-ttu-id="5720a-103">On Attribute (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="5720a-103">On Attribute (Fill)(VML)</span></span>

<span data-ttu-id="5720a-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5720a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5720a-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5720a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5720a-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="5720a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5720a-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="5720a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5720a-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5720a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5720a-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5720a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5720a-110">Détermine si le remplissage doit être affiché.</span><span class="sxs-lookup"><span data-stu-id="5720a-110">Determines whether the fill will be displayed.</span></span> <span data-ttu-id="5720a-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="5720a-111">Read/write.</span></span> <span data-ttu-id="5720a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="5720a-112">**VgTriState**.</span></span>

<span data-ttu-id="5720a-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="5720a-113">**Applies To**</span></span>

[<span data-ttu-id="5720a-114">Complète</span><span class="sxs-lookup"><span data-stu-id="5720a-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="5720a-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="5720a-115">**Tag Syntax**</span></span>

<span data-ttu-id="5720a-116"><v : *Element* on = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5720a-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="5720a-117">**Syntaxe du script**</span><span class="sxs-lookup"><span data-stu-id="5720a-117">**Script Syntax**</span></span>

<span data-ttu-id="5720a-118">*Element* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="5720a-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="5720a-119">*expression* = *élément*. on</span><span class="sxs-lookup"><span data-stu-id="5720a-119">*expression*=*element*.on</span></span>

<span data-ttu-id="5720a-120">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="5720a-120">**Remarks**</span></span>

<span data-ttu-id="5720a-121">Si la **valeur est false**, le remplissage n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="5720a-121">If **False**, the fill is not displayed.</span></span> <span data-ttu-id="5720a-122">La valeur par défaut est **True**.</span><span class="sxs-lookup"><span data-stu-id="5720a-122">The default is **True**.</span></span>

<span data-ttu-id="5720a-123">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="5720a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="5720a-124">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="5720a-124">**Example**</span></span>

<span data-ttu-id="5720a-125">Même si le remplissage est défini comme rouge, il n’est pas affiché.</span><span class="sxs-lookup"><span data-stu-id="5720a-125">Even though the fill is defined to be red, it is not displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" on="False"/>
   </v:shape>
```



 

 