---
title: Attribut de puce VML
description: Attribut de puce VML
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382178"
---
# <a name="vml-bullet-attribute"></a><span data-ttu-id="de28c-103">Attribut de puce VML</span><span class="sxs-lookup"><span data-stu-id="de28c-103">VML Bullet Attribute</span></span>

<span data-ttu-id="de28c-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="de28c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="de28c-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="de28c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="de28c-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="de28c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="de28c-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="de28c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="de28c-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="de28c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="de28c-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="de28c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="de28c-110">Détermine si une forme est une puce graphique.</span><span class="sxs-lookup"><span data-stu-id="de28c-110">Determines whether a shape is a graphical bullet.</span></span> <span data-ttu-id="de28c-111">**VgTriState** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="de28c-111">Read/write **VgTriState**.</span></span>

<span data-ttu-id="de28c-112">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="de28c-112">**Applies To**</span></span>

[<span data-ttu-id="de28c-113">Graphique à base de formes</span><span class="sxs-lookup"><span data-stu-id="de28c-113">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="de28c-114">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="de28c-114">**Tag Syntax**</span></span>

<span data-ttu-id="de28c-115"><v : *Element* o :Bullet = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="de28c-115"><v: *element* o:bullet=" *expression* "></span></span>

<span data-ttu-id="de28c-116">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="de28c-116">**Remarks**</span></span>

<span data-ttu-id="de28c-117">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="de28c-117">The default is **False**.</span></span> <span data-ttu-id="de28c-118">Si la **valeur est true**, la forme est un graphique à puce.</span><span class="sxs-lookup"><span data-stu-id="de28c-118">If **True**, the shape is a graphical bullet.</span></span>

<span data-ttu-id="de28c-119">*Attribut extensions Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="de28c-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="de28c-120">**Exemple**</span><span class="sxs-lookup"><span data-stu-id="de28c-120">**Example**</span></span>

<span data-ttu-id="de28c-121">La forme est une puce.</span><span class="sxs-lookup"><span data-stu-id="de28c-121">The shape is a bullet.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 