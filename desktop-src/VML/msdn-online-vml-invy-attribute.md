---
title: InvY VML (attribut)
description: InvY VML (attribut)
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315534"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="f91dd-103">InvY VML (attribut)</span><span class="sxs-lookup"><span data-stu-id="f91dd-103">VML InvY Attribute</span></span>

<span data-ttu-id="f91dd-104">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f91dd-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f91dd-105">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="f91dd-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f91dd-106">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="f91dd-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f91dd-107">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="f91dd-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f91dd-108">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f91dd-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f91dd-109">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f91dd-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f91dd-110">Détermine si la position y du handle est inversée.</span><span class="sxs-lookup"><span data-stu-id="f91dd-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="f91dd-111">En lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f91dd-111">Read/write.</span></span> <span data-ttu-id="f91dd-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="f91dd-112">**VgTriState**.</span></span>

<span data-ttu-id="f91dd-113">**S’applique à**</span><span class="sxs-lookup"><span data-stu-id="f91dd-113">**Applies To**</span></span>

<span data-ttu-id="f91dd-114">[H](msdn-online-vml-h-element.md) (sous-élément de [Handles](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="f91dd-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="f91dd-115">**Syntaxe de balise**</span><span class="sxs-lookup"><span data-stu-id="f91dd-115">**Tag Syntax**</span></span>

<span data-ttu-id="f91dd-116"><v : *Element* invy = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f91dd-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="f91dd-117">**Remarques**</span><span class="sxs-lookup"><span data-stu-id="f91dd-117">**Remarks**</span></span>

<span data-ttu-id="f91dd-118">Si la valeur est **true**, la position y du handle est inversée en soustrayant la valeur y de la valeur y de **CoordOrigin** ajoutée à la valeur y de **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="f91dd-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="f91dd-119">La valeur par défaut est **False**.</span><span class="sxs-lookup"><span data-stu-id="f91dd-119">The default value is **False**.</span></span>

<span data-ttu-id="f91dd-120">Cet attribut est l’équivalent de</span><span class="sxs-lookup"><span data-stu-id="f91dd-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="f91dd-121">*Attribut standard VML*</span><span class="sxs-lookup"><span data-stu-id="f91dd-121">*VML Standard Attribute*</span></span>

 

 