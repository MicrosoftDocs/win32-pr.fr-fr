---
title: Attributs de liste prédéfinis (TsAttrid. h)
description: Les valeurs suivantes identifient les attributs de liste obtenus avec la méthode ITfContext GetAppProperty. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- Attributs de liste prédéfinis (Text Services Framework)
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105385"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="a1c7a-105">Attributs de liste prédéfinis</span><span class="sxs-lookup"><span data-stu-id="a1c7a-105">Predefined List Attributes</span></span>

<span data-ttu-id="a1c7a-106">Les valeurs suivantes identifient les attributs de liste obtenus avec la méthode [ITfContext :: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="a1c7a-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="a1c7a-107">Le format de données et le contenu de chaque type de propriété sont inclus.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="a1c7a-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1c7a-108">Properties</span></span>



| <span data-ttu-id="a1c7a-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="a1c7a-109">Property</span></span>                          | <span data-ttu-id="a1c7a-110">Description</span><span class="sxs-lookup"><span data-stu-id="a1c7a-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c7a-111">\_Liste TSATTRID</span><span class="sxs-lookup"><span data-stu-id="a1c7a-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="a1c7a-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="a1c7a-113">TSATTRID \_ liste de \_ LevelIndel</span><span class="sxs-lookup"><span data-stu-id="a1c7a-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="a1c7a-114">Contient le niveau d’index de la liste.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-114">Contains the index level of the list.</span></span> <span data-ttu-id="a1c7a-115">1 est le niveau le plus à l’extérieur, 2 est le niveau suivant, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="a1c7a-116">\_Type de liste TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="a1c7a-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="a1c7a-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="a1c7a-118">\_Type de liste TSATTRID \_ \_ arabe</span><span class="sxs-lookup"><span data-stu-id="a1c7a-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="a1c7a-119">Contient une valeur différente de zéro si la liste est une liste de chiffres arabes ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="a1c7a-120">\_ \_ Puce type de liste TSATTRID \_</span><span class="sxs-lookup"><span data-stu-id="a1c7a-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="a1c7a-121">Contient une valeur différente de zéro si la liste est une liste à puces ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="a1c7a-122">\_Type de liste TSATTRID \_ \_ LowerLetter</span><span class="sxs-lookup"><span data-stu-id="a1c7a-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="a1c7a-123">Contient une valeur différente de zéro si la liste est une liste avec des lettres minuscules ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="a1c7a-124">\_Type de liste TSATTRID \_ \_ LowerRoman</span><span class="sxs-lookup"><span data-stu-id="a1c7a-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="a1c7a-125">Contient une valeur différente de zéro si la liste est une liste de chiffres romains en minuscules ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="a1c7a-126">\_Type de liste TSATTRID \_ \_ UpperLetter</span><span class="sxs-lookup"><span data-stu-id="a1c7a-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="a1c7a-127">Contient une valeur différente de zéro si la liste est une liste avec lettres majuscules ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="a1c7a-128">\_Type de liste TSATTRID \_ \_ UpperRoman</span><span class="sxs-lookup"><span data-stu-id="a1c7a-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="a1c7a-129">Contient une valeur différente de zéro si la liste est une liste de chiffres romains en majuscules ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a1c7a-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="a1c7a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1c7a-130">Requirements</span></span>



| <span data-ttu-id="a1c7a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a1c7a-131">Requirement</span></span> | <span data-ttu-id="a1c7a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="a1c7a-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1c7a-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1c7a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a1c7a-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1c7a-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a1c7a-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a1c7a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a1c7a-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1c7a-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1c7a-137">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a1c7a-137">Redistributable</span></span><br/>          | <span data-ttu-id="a1c7a-138">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a1c7a-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="a1c7a-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="a1c7a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1c7a-140"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1c7a-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1c7a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1c7a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1c7a-142">ITfContext :: GetAppProperty</span><span class="sxs-lookup"><span data-stu-id="a1c7a-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

