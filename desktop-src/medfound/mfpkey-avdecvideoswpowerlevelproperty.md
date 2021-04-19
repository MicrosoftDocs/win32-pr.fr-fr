---
description: Spécifie le niveau de puissance pour le décodeur.
ms.assetid: c4ede790-e7ef-4ed0-bdbe-a635350d92f3
title: MFPKEY_AVDecVideoSWPowerLevel, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2180e26d3e14263c14f2f3603c8c92cf8c11daec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518947"
---
# <a name="mfpkey_avdecvideoswpowerlevel-property"></a><span data-ttu-id="023ea-103">MFPKEY \_ propriété AVDecVideoSWPowerLevel</span><span class="sxs-lookup"><span data-stu-id="023ea-103">MFPKEY\_AVDecVideoSWPowerLevel Property</span></span>

<span data-ttu-id="023ea-104">Spécifie le niveau de puissance pour le décodeur.</span><span class="sxs-lookup"><span data-stu-id="023ea-104">Specifies the power level for the decoder.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="023ea-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="023ea-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="023ea-106">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="023ea-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="023ea-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="023ea-107">Data Type</span></span>

<span data-ttu-id="023ea-108">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="023ea-108">**VT\_UI4**</span></span>

## <a name="default-value"></a><span data-ttu-id="023ea-109">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="023ea-109">Default Value</span></span>

<span data-ttu-id="023ea-110">**100**</span><span class="sxs-lookup"><span data-stu-id="023ea-110">**100**</span></span>

## <a name="remarks"></a><span data-ttu-id="023ea-111">Notes</span><span class="sxs-lookup"><span data-stu-id="023ea-111">Remarks</span></span>

<span data-ttu-id="023ea-112">Cette propriété doit être définie sur l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="023ea-112">This property must be set to one of the following values.</span></span>



| <span data-ttu-id="023ea-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="023ea-113">Value</span></span> | <span data-ttu-id="023ea-114">Signification</span><span class="sxs-lookup"><span data-stu-id="023ea-114">Meaning</span></span>                                                             |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="023ea-115">0</span><span class="sxs-lookup"><span data-stu-id="023ea-115">0</span></span>     | <span data-ttu-id="023ea-116">Le décodeur utilise un niveau de puissance optimisé pour la durée de vie de la batterie.</span><span class="sxs-lookup"><span data-stu-id="023ea-116">The decoder uses a power level that is optimized for battery life.</span></span>  |
| <span data-ttu-id="023ea-117">50</span><span class="sxs-lookup"><span data-stu-id="023ea-117">50</span></span>    | <span data-ttu-id="023ea-118">Le décodeur utilise un niveau de puissance équilibré.</span><span class="sxs-lookup"><span data-stu-id="023ea-118">The decoder uses a balanced power level.</span></span>                            |
| <span data-ttu-id="023ea-119">100</span><span class="sxs-lookup"><span data-stu-id="023ea-119">100</span></span>   | <span data-ttu-id="023ea-120">Le décodeur utilise un niveau de puissance optimisé pour la qualité vidéo.</span><span class="sxs-lookup"><span data-stu-id="023ea-120">The decoder uses a power level that is optimized for video quality.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="023ea-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="023ea-121">Requirements</span></span>



| <span data-ttu-id="023ea-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="023ea-122">Requirement</span></span> | <span data-ttu-id="023ea-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="023ea-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="023ea-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="023ea-124">Minimum supported client</span></span><br/> | <span data-ttu-id="023ea-125">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="023ea-125">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="023ea-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="023ea-126">Minimum supported server</span></span><br/> | <span data-ttu-id="023ea-127">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="023ea-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="023ea-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="023ea-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="023ea-129"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="023ea-129"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="023ea-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="023ea-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="023ea-131">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="023ea-131">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
