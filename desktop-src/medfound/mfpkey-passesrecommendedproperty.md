---
description: Spécifie le nombre maximal de passes prises en charge par l’encodeur.
ms.assetid: 7e21cd0f-f13f-4321-b246-f1adaa5c6094
title: MFPKEY_PASSESRECOMMENDED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 433e0a0d254c09965976e5659bacfacf3be06643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202343"
---
# <a name="mfpkey_passesrecommended-property"></a><span data-ttu-id="2c0d3-103">MFPKEY \_ propriété PASSESRECOMMENDED</span><span class="sxs-lookup"><span data-stu-id="2c0d3-103">MFPKEY\_PASSESRECOMMENDED Property</span></span>

<span data-ttu-id="2c0d3-104">Spécifie le nombre maximal de passes prises en charge par l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="2c0d3-104">Specifies the maximum number of passes supported by the encoder.</span></span> <span data-ttu-id="2c0d3-105">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="2c0d3-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="2c0d3-106">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="2c0d3-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="2c0d3-107">g \_ wszWMVCPassesRecommended, g \_ wszWMCPMaxPasses</span><span class="sxs-lookup"><span data-stu-id="2c0d3-107">g\_wszWMVCPassesRecommended, g\_wszWMCPMaxPasses</span></span>

## <a name="data-type"></a><span data-ttu-id="2c0d3-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="2c0d3-108">Data Type</span></span>

<span data-ttu-id="2c0d3-109">VT \_</span><span class="sxs-lookup"><span data-stu-id="2c0d3-109">VT\_I4</span></span>

## <a name="remarks"></a><span data-ttu-id="2c0d3-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2c0d3-110">Remarks</span></span>

<span data-ttu-id="2c0d3-111">Vous pouvez récupérer la valeur de cette propriété en appelant [IWMCodecProps :: GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span><span class="sxs-lookup"><span data-stu-id="2c0d3-111">You can get the value of this property calling [IWMCodecProps::GetCodecProp](/windows/desktop/api/wmcodecdsp/nf-wmcodecdsp-iwmcodecprops-getcodecprop).</span></span> <span data-ttu-id="2c0d3-112">Si vous utilisez **IPropertyBag**, vous devez d’abord définir la valeur FourCC du format compressé souhaité à l’aide de la propriété [ \_ FourCC MFPKEY](mfpkey-fourccproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="2c0d3-112">If you use **IPropertyBag**, you must first set the FOURCC value of the desired compressed format by using the [MFPKEY\_FOURCC](mfpkey-fourccproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c0d3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c0d3-113">Requirements</span></span>



| <span data-ttu-id="2c0d3-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c0d3-114">Requirement</span></span> | <span data-ttu-id="2c0d3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c0d3-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c0d3-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c0d3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2c0d3-117">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c0d3-117">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2c0d3-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2c0d3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2c0d3-119">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2c0d3-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2c0d3-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c0d3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2c0d3-121"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c0d3-121"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c0d3-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c0d3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c0d3-123">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c0d3-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




