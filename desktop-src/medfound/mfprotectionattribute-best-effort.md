---
description: Défini en tant qu’attribut pour un objet IMFOutputSchema.
ms.assetid: 0CCCAB27-DEB0-41D8-A70C-D6CCEFE0601F
title: Attribut MFPROTECTIONATTRIBUTE_BEST_EFFORT (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd7d2f173b5bf85080e0de65866f84b3a317b7ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202257"
---
# <a name="mfprotectionattribute_best_effort-attribute"></a><span data-ttu-id="15ea5-103">\_Attribut de meilleur \_ effort MFPROTECTIONATTRIBUTE</span><span class="sxs-lookup"><span data-stu-id="15ea5-103">MFPROTECTIONATTRIBUTE\_BEST\_EFFORT attribute</span></span>

<span data-ttu-id="15ea5-104">Défini en tant qu’attribut pour un objet [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="15ea5-104">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span> <span data-ttu-id="15ea5-105">Si cet attribut est présent, l’échec d’une tentative d’application de la protection est ignoré.</span><span class="sxs-lookup"><span data-stu-id="15ea5-105">If this attribute is present, a failed attempt to apply the protection is ignored.</span></span> <span data-ttu-id="15ea5-106">Si la valeur de l’attribut associé est **true**, le schéma de protection avec l’attribut de [ \_ \_ basculement MFPROTECTIONATTRIBUTE](mfprotectionattribute-fail-over.md) doit être appliqué.</span><span class="sxs-lookup"><span data-stu-id="15ea5-106">If the associated attribute value is **TRUE**, the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute should be applied.</span></span>

## <a name="data-type"></a><span data-ttu-id="15ea5-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="15ea5-107">Data type</span></span>

<span data-ttu-id="15ea5-108">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="15ea5-108">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="15ea5-109">Notes</span><span class="sxs-lookup"><span data-stu-id="15ea5-109">Remarks</span></span>

<span data-ttu-id="15ea5-110">Si la **valeur est true**, applique le schéma de protection avec l’attribut de [ \_ basculement MFPROTECTIONATTRIBUTE en \_](mfprotectionattribute-fail-over.md) cas d’échec de la définition de cette protection.</span><span class="sxs-lookup"><span data-stu-id="15ea5-110">If **TRUE**, enforce the protection schema with the [MFPROTECTIONATTRIBUTE\_FAIL\_OVER](mfprotectionattribute-fail-over.md) attribute if setting this protection fails.</span></span>

<span data-ttu-id="15ea5-111">Défini en tant qu’attribut pour un objet [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) .</span><span class="sxs-lookup"><span data-stu-id="15ea5-111">Set as an attribute for an [**IMFOutputSchema**](/windows/desktop/api/mfidl/nn-mfidl-imfoutputschema) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="15ea5-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15ea5-112">Requirements</span></span>



| <span data-ttu-id="15ea5-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15ea5-113">Requirement</span></span> | <span data-ttu-id="15ea5-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="15ea5-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="15ea5-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15ea5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="15ea5-116">\[Applications UWP Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15ea5-116">Windows 8 \[UWP apps only\]</span></span><br/>                                             |
| <span data-ttu-id="15ea5-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15ea5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="15ea5-118">Applications UWP Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15ea5-118">Windows Server 2012 \[UWP apps only\]</span></span><br/>                                   |
| <span data-ttu-id="15ea5-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="15ea5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="15ea5-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="15ea5-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ea5-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15ea5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ea5-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="15ea5-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="15ea5-123">Attributs du type de média</span><span class="sxs-lookup"><span data-stu-id="15ea5-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




