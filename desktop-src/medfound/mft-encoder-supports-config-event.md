---
description: Spécifie que l’encodeur MFT prend en charge la réception des événements MEEncodingParameter lors de la diffusion en continu.
ms.assetid: 8DE04537-641C-4154-9C7F-A7D025CA4C39
title: Attribut MFT_ENCODER_SUPPORTS_CONFIG_EVENT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c49c688abc4d372a463115c369e4616babe3bcaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519833"
---
# <a name="mft_encoder_supports_config_event-attribute"></a><span data-ttu-id="9a0d4-103">L' \_ encodeur MFT \_ prend en charge l' \_ attribut d’événement de configuration \_</span><span class="sxs-lookup"><span data-stu-id="9a0d4-103">MFT\_ENCODER\_SUPPORTS\_CONFIG\_EVENT attribute</span></span>

<span data-ttu-id="9a0d4-104">Spécifie que l’encodeur MFT prend en charge la réception des événements [MEEncodingParameter](meencodingparameters.md) lors de la diffusion en continu.</span><span class="sxs-lookup"><span data-stu-id="9a0d4-104">Specifies that the MFT encoder supports receiving [MEEncodingParameter](meencodingparameters.md) events while streaming.</span></span>

## <a name="data-type"></a><span data-ttu-id="9a0d4-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="9a0d4-105">Data type</span></span>

<span data-ttu-id="9a0d4-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="9a0d4-106">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="9a0d4-107">Notes</span><span class="sxs-lookup"><span data-stu-id="9a0d4-107">Remarks</span></span>

<span data-ttu-id="9a0d4-108">Envoyé par l’encodeur MFT via [**IMFTransform ::P rocessevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span><span class="sxs-lookup"><span data-stu-id="9a0d4-108">Sent by the MFT encoder through [**IMFTransform::ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent).</span></span>

## <a name="requirements"></a><span data-ttu-id="9a0d4-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a0d4-109">Requirements</span></span>



| <span data-ttu-id="9a0d4-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a0d4-110">Requirement</span></span> | <span data-ttu-id="9a0d4-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a0d4-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a0d4-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a0d4-112">Minimum supported client</span></span><br/> | <span data-ttu-id="9a0d4-113">\[Applications Windows 8.1 Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9a0d4-113">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9a0d4-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9a0d4-114">Minimum supported server</span></span><br/> | <span data-ttu-id="9a0d4-115">Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="9a0d4-115">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="9a0d4-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a0d4-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a0d4-117"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d4-117"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a0d4-118">MIDL</span><span class="sxs-lookup"><span data-stu-id="9a0d4-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a0d4-119"><dt>Mftransform. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a0d4-119"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a0d4-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a0d4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a0d4-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9a0d4-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9a0d4-122">**IMFTransform ::P rocessEvent**</span><span class="sxs-lookup"><span data-stu-id="9a0d4-122">**IMFTransform::ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
</dt> </dl>

 

 




