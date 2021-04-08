---
description: Spécifie si l’encodeur utilise l’encodage VBR (variable-bit-rate).
ms.assetid: e6826802-99b7-4a38-9b58-8a9cb8b753fb
title: MFPKEY_VBRENABLED, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9061abcc6ac7d7338b63eb5a7cd1a13ad22bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864129"
---
# <a name="mfpkey_vbrenabled-property"></a><span data-ttu-id="47a0b-103">MFPKEY \_ propriété VBRENABLED</span><span class="sxs-lookup"><span data-stu-id="47a0b-103">MFPKEY\_VBRENABLED Property</span></span>

<span data-ttu-id="47a0b-104">Spécifie si l’encodeur utilise l’encodage VBR (variable-bit-rate).</span><span class="sxs-lookup"><span data-stu-id="47a0b-104">Specifies whether the encoder uses variable-bit-rate (VBR) encoding.</span></span> <span data-ttu-id="47a0b-105">Lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="47a0b-105">Read-write.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="47a0b-106">Constante pour IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="47a0b-106">Constant for IPropertyBag</span></span>

<span data-ttu-id="47a0b-107">**g \_ wszWMVCVBREnabled**, **g \_ wszWMCPAudioVBRSupported**</span><span class="sxs-lookup"><span data-stu-id="47a0b-107">**g\_wszWMVCVBREnabled**, **g\_wszWMCPAudioVBRSupported**</span></span>

## <a name="data-type"></a><span data-ttu-id="47a0b-108">Type de données</span><span class="sxs-lookup"><span data-stu-id="47a0b-108">Data Type</span></span>

<span data-ttu-id="47a0b-109">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="47a0b-109">**VT\_BOOL**</span></span>

## <a name="default-value"></a><span data-ttu-id="47a0b-110">Valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="47a0b-110">Default Value</span></span>

<span data-ttu-id="47a0b-111">**VARIANTE \_ false**</span><span class="sxs-lookup"><span data-stu-id="47a0b-111">**VARIANT\_FALSE**</span></span>

## <a name="remarks"></a><span data-ttu-id="47a0b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="47a0b-112">Remarks</span></span>

<span data-ttu-id="47a0b-113">Cette valeur doit être définie sur **Variant \_ true** pour l’une des autres propriétés VBR à utiliser par le codec.</span><span class="sxs-lookup"><span data-stu-id="47a0b-113">This value must be set to **VARIANT\_TRUE** for any of the other VBR properties to be used by the codec.</span></span>

<span data-ttu-id="47a0b-114">Une fois que vous avez défini cette valeur sur **Variant \_ true** sur l’encodeur audio, les types de sortie récupérés à l’aide de la méthode [**IMediaObject :: GETOUTPUTTYPE**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) sont des types VBR.</span><span class="sxs-lookup"><span data-stu-id="47a0b-114">After you set this value to **VARIANT\_TRUE** on the audio encoder, the output types retrieved by using the [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype) method are VBR types.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a0b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47a0b-115">Requirements</span></span>



| <span data-ttu-id="47a0b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47a0b-116">Requirement</span></span> | <span data-ttu-id="47a0b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="47a0b-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="47a0b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47a0b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="47a0b-119">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47a0b-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="47a0b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="47a0b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="47a0b-121">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="47a0b-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="47a0b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="47a0b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="47a0b-123"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="47a0b-123"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a0b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47a0b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a0b-125">**MFPKEY de \_ contrainte \_ énumérée \_ VBRQUALITY**</span><span class="sxs-lookup"><span data-stu-id="47a0b-125">**MFPKEY\_CONSTRAIN\_ENUMERATED\_VBRQUALITY**</span></span>](mfpkey-constrain-enumerated-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="47a0b-126">**MFPKEY \_ \_ VBRQUALITY souhaité**</span><span class="sxs-lookup"><span data-stu-id="47a0b-126">**MFPKEY\_DESIRED\_VBRQUALITY**</span></span>](mfpkey-desired-vbrqualityproperty.md)
</dt> <dt>

[<span data-ttu-id="47a0b-127">Propriétés de la Media Foundation</span><span class="sxs-lookup"><span data-stu-id="47a0b-127">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
