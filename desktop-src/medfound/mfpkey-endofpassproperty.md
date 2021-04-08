---
description: Spécifie la fin d’une passe d’encodage.
ms.assetid: 8a7e6e09-766c-4346-8893-eea5614b2aa4
title: MFPKEY_ENDOFPASS, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a38e03867e11cde944bf902ae52f98cda7b8313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864162"
---
# <a name="mfpkey_endofpass-property"></a><span data-ttu-id="ff8b0-103">MFPKEY \_ propriété ENDOFPASS</span><span class="sxs-lookup"><span data-stu-id="ff8b0-103">MFPKEY\_ENDOFPASS Property</span></span>

<span data-ttu-id="ff8b0-104">Spécifie la fin d’une passe d’encodage.</span><span class="sxs-lookup"><span data-stu-id="ff8b0-104">Specifies the end of an encoding pass.</span></span>

## <a name="data-type"></a><span data-ttu-id="ff8b0-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="ff8b0-105">Data Type</span></span>

<span data-ttu-id="ff8b0-106">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="ff8b0-106">**VT\_BOOL**</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="ff8b0-107">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ff8b0-107">Constant for IPropertyBag</span></span>

<span data-ttu-id="ff8b0-108">\_wszWMVCEndOfPass g</span><span class="sxs-lookup"><span data-stu-id="ff8b0-108">g\_wszWMVCEndOfPass</span></span>

## <a name="data-type-for-ipropertybag"></a><span data-ttu-id="ff8b0-109">Type de données pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="ff8b0-109">Data Type for IPropertyBag</span></span>

<span data-ttu-id="ff8b0-110">Aucun type de données n’est requis.</span><span class="sxs-lookup"><span data-stu-id="ff8b0-110">No data type is required.</span></span> <span data-ttu-id="ff8b0-111">Pour définir cette propriété, transmettez un **Variant** non initialisé.</span><span class="sxs-lookup"><span data-stu-id="ff8b0-111">To set this property, pass an uninitialized **VARIANT**.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff8b0-112">Notes</span><span class="sxs-lookup"><span data-stu-id="ff8b0-112">Remarks</span></span>

<span data-ttu-id="ff8b0-113">Cette propriété n’est pas une propriété normale, car elle a le même effet que la valeur soit \_ true ou \_ false comme variant.</span><span class="sxs-lookup"><span data-stu-id="ff8b0-113">This property is not a normal property because it has the same effect regardless of whether the value is VARIANT\_TRUE or VARIANT\_FALSE.</span></span> <span data-ttu-id="ff8b0-114">Vous devez définir cette propriété après avoir traité les derniers échantillons d’entrée pour une passe de prétraitement.</span><span class="sxs-lookup"><span data-stu-id="ff8b0-114">You must set this property after you process the last input samples for a preprocessing pass.</span></span> <span data-ttu-id="ff8b0-115">Si vous effectuez plusieurs passes, vous devez définir cette propriété à la fin de chaque passe de prétraitement (à l’heure actuelle, aucun Codec ne prend en charge plus d’un).</span><span class="sxs-lookup"><span data-stu-id="ff8b0-115">If you are performing multiple passes, you must set this property at the end of each preprocessing pass (at present none of the codecs supports more than one).</span></span> <span data-ttu-id="ff8b0-116">Si vous ne définissez pas cette propriété, le codec suppose que vous passez toujours des exemples pour le prétraitement.</span><span class="sxs-lookup"><span data-stu-id="ff8b0-116">If you do not set this property, the codec will assume that you are still passing samples for preprocessing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff8b0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff8b0-117">Requirements</span></span>



| <span data-ttu-id="ff8b0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff8b0-118">Requirement</span></span> | <span data-ttu-id="ff8b0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff8b0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff8b0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff8b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ff8b0-121">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff8b0-121">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ff8b0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff8b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ff8b0-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff8b0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff8b0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff8b0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff8b0-125"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff8b0-125"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff8b0-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff8b0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff8b0-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ff8b0-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




