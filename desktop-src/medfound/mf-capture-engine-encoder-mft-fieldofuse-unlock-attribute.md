---
description: Permet au moteur de capture d’utiliser un encodeur qui a des restrictions de champ d’utilisation.
ms.assetid: 28421875-9629-4F14-8159-2D86012F517F
title: Attribut MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a9466162ff5551ee155343800d938276823ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201994"
---
# <a name="mf_capture_engine_encoder_mft_fieldofuse_unlock_attribute-attribute"></a><span data-ttu-id="29e24-103">\_Attribut d' \_ \_ attribut de \_ \_ \_ déverrouillage FIELDOFUSE de l’encodeur du moteur de capture \_ MF</span><span class="sxs-lookup"><span data-stu-id="29e24-103">MF\_CAPTURE\_ENGINE\_ENCODER\_MFT\_FIELDOFUSE\_UNLOCK\_Attribute attribute</span></span>

<span data-ttu-id="29e24-104">Permet au moteur de capture d’utiliser un encodeur qui a des restrictions de champ d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="29e24-104">Enables the capture engine to use an encoder that has field-of-use restrictions.</span></span>

## <a name="data-type"></a><span data-ttu-id="29e24-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="29e24-105">Data type</span></span>

<span data-ttu-id="29e24-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="29e24-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="29e24-107">Notes</span><span class="sxs-lookup"><span data-stu-id="29e24-107">Remarks</span></span>

<span data-ttu-id="29e24-108">La valeur de cet attribut est un pointeur vers l’interface [_ *IMFFieldOfUseMFTUnlock* \*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , implémentée par l’appelant.</span><span class="sxs-lookup"><span data-stu-id="29e24-108">The value of this attribute is a pointer to the [_ *IMFFieldOfUseMFTUnlock*\*](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) interface, implemented by the caller.</span></span> <span data-ttu-id="29e24-109">L’implémentation de cette interface par l’appelant est supposée effectuer une négociation avec l’encodeur, comme décrit dans [champ de restrictions d’utilisation](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="29e24-109">The caller's implementation of this interface is expected to perform a handshake with the encoder, as described in [Field of Use Restrictions](field-of-use-restrictions.md).</span></span> <span data-ttu-id="29e24-110">Microsoft Media Foundation ne définit pas le protocole de transfert, en général, il implique un certain type d’échange de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="29e24-110">Microsoft Media Foundation does not define the handshake—typically, it would involve some sort of cryptographic exchange.</span></span>

<span data-ttu-id="29e24-111">En interne, le moteur de capture définit le pointeur [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) sur l’encodeur en définissant l’attribut d' [ \_ \_ \_ attribut de déverrouillage MFT FIELDOFUSE](mft-fieldofuse-unlock-attribute.md) de l’encodeur.</span><span class="sxs-lookup"><span data-stu-id="29e24-111">Internally, the capture engine sets the [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) pointer on the encoder by setting the encoder's [MFT\_FIELDOFUSE\_UNLOCK\_Attribute](mft-fieldofuse-unlock-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="29e24-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="29e24-112">Requirements</span></span>



| <span data-ttu-id="29e24-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="29e24-113">Requirement</span></span> | <span data-ttu-id="29e24-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="29e24-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="29e24-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e24-115">Minimum supported client</span></span><br/> | <span data-ttu-id="29e24-116">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29e24-116">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="29e24-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="29e24-117">Minimum supported server</span></span><br/> | <span data-ttu-id="29e24-118">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="29e24-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="29e24-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="29e24-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="29e24-120"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="29e24-120"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29e24-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="29e24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29e24-122">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="29e24-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="29e24-123">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="29e24-123">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="29e24-124">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="29e24-124">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




