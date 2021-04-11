---
description: Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.
ms.assetid: c03da576-cb58-4686-af6f-9575520c759c
title: MFPKEY_FOURCC, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbe852ad0d7113717428bdd832b8f327f8d0b6e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951666"
---
# <a name="mfpkey_fourcc-property"></a><span data-ttu-id="3f81d-103">MFPKEY, \_ propriété FourCC</span><span class="sxs-lookup"><span data-stu-id="3f81d-103">MFPKEY\_FOURCC Property</span></span>

<span data-ttu-id="3f81d-104">Spécifie le FOURCC qui identifie l’encodeur que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="3f81d-104">Specifies the FOURCC that identifies the encoder you want to use.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="3f81d-105">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="3f81d-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="3f81d-106">\_wszWMVCFOURCC g</span><span class="sxs-lookup"><span data-stu-id="3f81d-106">g\_wszWMVCFOURCC</span></span>

## <a name="data-type"></a><span data-ttu-id="3f81d-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="3f81d-107">Data Type</span></span>

<span data-ttu-id="3f81d-108">VT \_ I4 (valeur FourCC)</span><span class="sxs-lookup"><span data-stu-id="3f81d-108">VT\_I4 (FOURCC value)</span></span>

## <a name="remarks"></a><span data-ttu-id="3f81d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="3f81d-109">Remarks</span></span>

<span data-ttu-id="3f81d-110">Vous devez définir cette valeur avant de récupérer les valeurs des propriétés suivantes à l’aide de **IPropertyBag** ou **IPropertyStore**:</span><span class="sxs-lookup"><span data-stu-id="3f81d-110">You must set this value before retrieving the values for the following properties using **IPropertyBag** or **IPropertyStore**:</span></span>

-   [<span data-ttu-id="3f81d-111">MFPKEY \_ BUFFERFULLNESSINFIRSTBYTE</span><span class="sxs-lookup"><span data-stu-id="3f81d-111">MFPKEY\_BUFFERFULLNESSINFIRSTBYTE</span></span>](mfpkey-bufferfullnessinfirstbyteproperty.md)
-   [<span data-ttu-id="3f81d-112">MFPKEY \_ PASSESRECOMMENDED</span><span class="sxs-lookup"><span data-stu-id="3f81d-112">MFPKEY\_PASSESRECOMMENDED</span></span>](mfpkey-passesrecommendedproperty.md)

<span data-ttu-id="3f81d-113">Vous devez utiliser [**IWMCodecProps :: GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) pour récupérer les valeurs des propriétés dépendantes du FourCC indiquées précédemment.</span><span class="sxs-lookup"><span data-stu-id="3f81d-113">You should use [**IWMCodecProps::GetCodecProp**](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop) to retrieve the values of the FOURCC-dependent properties listed previously.</span></span> <span data-ttu-id="3f81d-114">Lorsque vous utilisez **GetCodecProp**, vous n’avez pas besoin de définir **MFPKEY \_ FourCC**.</span><span class="sxs-lookup"><span data-stu-id="3f81d-114">When using **GetCodecProp**, you do not need to set **MFPKEY\_FOURCC**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f81d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f81d-115">Requirements</span></span>



| <span data-ttu-id="3f81d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f81d-116">Requirement</span></span> | <span data-ttu-id="3f81d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f81d-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f81d-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f81d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3f81d-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f81d-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3f81d-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f81d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3f81d-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f81d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f81d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="3f81d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f81d-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f81d-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f81d-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f81d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f81d-125">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f81d-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




