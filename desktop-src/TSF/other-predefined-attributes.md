---
title: Autres attributs prédéfinis (TsAttrid. h)
description: Les valeurs suivantes identifient les attributs divers obtenus avec la méthode ITfContext GetAppProperty. Le format de données et le contenu de chaque type de propriété sont inclus.
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- Autres attributs prédéfinis Text Services Framework
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536917"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="4c9c0-105">Autres attributs prédéfinis</span><span class="sxs-lookup"><span data-stu-id="4c9c0-105">Other Predefined Attributes</span></span>

<span data-ttu-id="4c9c0-106">Les valeurs suivantes identifient les attributs divers obtenus avec la méthode [ITfContext :: GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) .</span><span class="sxs-lookup"><span data-stu-id="4c9c0-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="4c9c0-107">Le format de données et le contenu de chaque type de propriété sont inclus.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="4c9c0-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4c9c0-108">Properties</span></span>



| <span data-ttu-id="4c9c0-109">Propriété</span><span class="sxs-lookup"><span data-stu-id="4c9c0-109">Property</span></span>                             | <span data-ttu-id="4c9c0-110">Description</span><span class="sxs-lookup"><span data-stu-id="4c9c0-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="4c9c0-111">**\_Application TSATTRID**</span><span class="sxs-lookup"><span data-stu-id="4c9c0-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="4c9c0-112">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="4c9c0-113">**\_Application TSATTRID \_ IncorrectGrammar**</span><span class="sxs-lookup"><span data-stu-id="4c9c0-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="4c9c0-114">Contient une valeur différente de zéro si le texte contient une erreur de grammaire ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="4c9c0-115">**\_Application TSATTRID \_ IncorrectSpelling**</span><span class="sxs-lookup"><span data-stu-id="4c9c0-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="4c9c0-116">Contient une valeur différente de zéro si le texte contient une faute d’orthographe ou zéro dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="4c9c0-117">**TSATTRID \_ autres**</span><span class="sxs-lookup"><span data-stu-id="4c9c0-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="4c9c0-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="4c9c0-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="4c9c0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4c9c0-119">Requirements</span></span>



| <span data-ttu-id="4c9c0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4c9c0-120">Requirement</span></span> | <span data-ttu-id="4c9c0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="4c9c0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c9c0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c9c0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="4c9c0-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c9c0-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="4c9c0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4c9c0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="4c9c0-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4c9c0-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4c9c0-126">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="4c9c0-126">Redistributable</span></span><br/>          | <span data-ttu-id="4c9c0-127">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="4c9c0-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="4c9c0-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="4c9c0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="4c9c0-129"><dt>TsAttrid. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c9c0-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

