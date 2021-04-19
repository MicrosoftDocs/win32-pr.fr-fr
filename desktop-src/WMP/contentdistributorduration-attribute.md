---
title: Attribut ContentDistributorDuration
description: L’attribut ContentDistributorDuration est la durée de l’exécution de l’élément, en secondes.
ms.assetid: c64cb4ca-b0bc-4beb-b2ae-ddd0c5fcd35c
keywords:
- Attribut ContentDistributorDuration lecteur Windows Media
topic_type:
- apiref
api_name:
- ContentDistributorDuration
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9f17bad8ef5dd1ab4b0a3d1c7b5becec6fd34a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521662"
---
# <a name="contentdistributorduration-attribute"></a><span data-ttu-id="929ab-104">Attribut ContentDistributorDuration</span><span class="sxs-lookup"><span data-stu-id="929ab-104">ContentDistributorDuration Attribute</span></span>

<span data-ttu-id="929ab-105">L’attribut **ContentDistributorDuration** est la durée de l’exécution de l’élément, en secondes.</span><span class="sxs-lookup"><span data-stu-id="929ab-105">The **ContentDistributorDuration** attribute is the playing duration of the item, in seconds.</span></span>

## <a name="applies-to"></a><span data-ttu-id="929ab-106">S'applique à</span><span class="sxs-lookup"><span data-stu-id="929ab-106">Applies To</span></span>

-   [<span data-ttu-id="929ab-107">Éléments audio</span><span class="sxs-lookup"><span data-stu-id="929ab-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="929ab-108">Autres éléments</span><span class="sxs-lookup"><span data-stu-id="929ab-108">Other Items</span></span>](other-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="929ab-109">Notes</span><span class="sxs-lookup"><span data-stu-id="929ab-109">Remarks</span></span>

<span data-ttu-id="929ab-110">Si l’attribut de **durée** normale n’est pas défini (null) ou 0, la valeur de cet attribut est retournée à la place.</span><span class="sxs-lookup"><span data-stu-id="929ab-110">If the regular **Duration** attribute is either not set (Null) or 0, then the value of this attribute will be returned instead.</span></span>

<span data-ttu-id="929ab-111">Pour déterminer si vous pouvez modifier la valeur de cet attribut, utilisez la méthode [Media. isReadOnlyItem](media-isreadonlyitem.md) .</span><span class="sxs-lookup"><span data-stu-id="929ab-111">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="929ab-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="929ab-112">Requirements</span></span>



| <span data-ttu-id="929ab-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="929ab-113">Requirement</span></span> | <span data-ttu-id="929ab-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="929ab-114">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="929ab-115">Version</span><span class="sxs-lookup"><span data-stu-id="929ab-115">Version</span></span><br/> | <span data-ttu-id="929ab-116">Lecteur Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="929ab-116">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="929ab-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="929ab-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="929ab-118">**Référence d’attribut**</span><span class="sxs-lookup"><span data-stu-id="929ab-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> <dt>

[<span data-ttu-id="929ab-119">**Attribut Duration**</span><span class="sxs-lookup"><span data-stu-id="929ab-119">**Duration Attribute**</span></span>](duration-attribute.md)
</dt> </dl>

 

 





