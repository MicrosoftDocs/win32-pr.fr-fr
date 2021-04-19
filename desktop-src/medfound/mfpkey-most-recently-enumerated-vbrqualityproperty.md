---
description: Spécifie le niveau de qualité VBR du type de sortie énuméré le plus récemment.
ms.assetid: 7d67e41f-060b-49a1-9e17-5db081ef4210
title: MFPKEY_MOST_RECENT_ENUMERATED_VBRQUALITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd3b5f3aae6dc5347672cf6697c3431163dcbd1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521741"
---
# <a name="mfpkey_most_recent_enumerated_vbrquality-property"></a><span data-ttu-id="17b2f-103">MFPKEY \_ \_ \_ propriété VBRQUALITY énumérée la plus récente \_</span><span class="sxs-lookup"><span data-stu-id="17b2f-103">MFPKEY\_MOST\_RECENT\_ENUMERATED\_VBRQUALITY Property</span></span>

<span data-ttu-id="17b2f-104">Spécifie le niveau de qualité VBR du type de sortie énuméré le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="17b2f-104">Specifies the VBR quality level of the most recently enumerated output type.</span></span> <span data-ttu-id="17b2f-105">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="17b2f-105">Read-only.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="17b2f-106">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="17b2f-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="17b2f-107">Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="17b2f-107">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="17b2f-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="17b2f-108">Data Type</span></span>

<span data-ttu-id="17b2f-109">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="17b2f-109">**VT\_UI4**</span></span>

## <a name="remarks"></a><span data-ttu-id="17b2f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="17b2f-110">Remarks</span></span>

<span data-ttu-id="17b2f-111">Lorsque l’encodeur agit comme une Media Foundation transformation (MFT) et qu’il énumère un type de sortie sur un appel à [**IMFTransform :: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), vous pouvez interroger la table MFT pour obtenir la propriété **\_ \_ \_ \_ VBRQUALITY énumérée la plus récente de MFPKEY** .</span><span class="sxs-lookup"><span data-stu-id="17b2f-111">When the encoder is acting as an Media Foundation Transform (MFT) and it enumerates an output type on a call to [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype), you can query the MFT for the **MFPKEY\_MOST\_RECENTLY\_ENUMERATED\_VBRQUALITY** property.</span></span> <span data-ttu-id="17b2f-112">La valeur retournée indique la qualité VBR du type de média de sortie retourné le plus récemment.</span><span class="sxs-lookup"><span data-stu-id="17b2f-112">The value returned indicates the VBR quality of the most recently returned output media type.</span></span> <span data-ttu-id="17b2f-113">Vous pouvez ensuite utiliser cette valeur pour définir la propriété [**MFPKEY \_ souhaitée \_ VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="17b2f-113">Then you can use that value to set the [**MFPKEY\_DESIRED\_VBRQUALITY**](mfpkey-desired-vbrqualityproperty.md) property of the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="17b2f-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17b2f-114">Requirements</span></span>



| <span data-ttu-id="17b2f-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17b2f-115">Requirement</span></span> | <span data-ttu-id="17b2f-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="17b2f-116">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17b2f-117">Client</span><span class="sxs-lookup"><span data-stu-id="17b2f-117">Client</span></span><br/> | <span data-ttu-id="17b2f-118">Windows Vista ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="17b2f-118">Windows Vista or Windows 7</span></span><br/>                                                   |
| <span data-ttu-id="17b2f-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="17b2f-119">Header</span></span><br/> | <dl> <span data-ttu-id="17b2f-120"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b2f-120"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b2f-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17b2f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b2f-122">**MFPKEY \_ VBRENABLED**</span><span class="sxs-lookup"><span data-stu-id="17b2f-122">**MFPKEY\_VBRENABLED**</span></span>](mfpkey-vbrenabledproperty.md)
</dt> <dt>

[<span data-ttu-id="17b2f-123">**MFPKEY de \_ contrainte \_ énumérée \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="17b2f-123">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="17b2f-124">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="17b2f-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
