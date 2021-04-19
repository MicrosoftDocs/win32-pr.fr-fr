---
description: Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.
ms.assetid: 1C687FEC-276D-4759-A3B8-9A2A31CB0DE1
title: Attribut MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9631804c61fab953793c3f89d1eac3dc2e8f4dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524553"
---
# <a name="mf_capture_engine_disable_hardware_transforms-attribute"></a><span data-ttu-id="d0bdc-103">\_Attribut de \_ \_ désactivation \_ des \_ transformations matérielles du moteur de capture MF</span><span class="sxs-lookup"><span data-stu-id="d0bdc-103">MF\_CAPTURE\_ENGINE\_DISABLE\_HARDWARE\_TRANSFORMS attribute</span></span>

<span data-ttu-id="d0bdc-104">Désactive l’utilisation des transformations de Media Foundation basées sur le matériel (MFTs) dans le moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="d0bdc-104">Disables the use of hardware-based Media Foundation transforms (MFTs) in the capture engine.</span></span>

## <a name="data-type"></a><span data-ttu-id="d0bdc-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="d0bdc-105">Data type</span></span>

<span data-ttu-id="d0bdc-106">**Bool** stocké comme **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d0bdc-106">**BOOL** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="d0bdc-107">Notes</span><span class="sxs-lookup"><span data-stu-id="d0bdc-107">Remarks</span></span>

<span data-ttu-id="d0bdc-108">Par défaut, le moteur de capture utilise des décodeurs ou des encodeurs matériels.</span><span class="sxs-lookup"><span data-stu-id="d0bdc-108">By default, the capture engine uses hardware decoders or encoders.</span></span> <span data-ttu-id="d0bdc-109">Pour désactiver l’utilisation du matériel MFTs, affectez la valeur **true** à cet attribut lorsque vous créez le moteur de capture.</span><span class="sxs-lookup"><span data-stu-id="d0bdc-109">To disable the use of hardware MFTs, set this attribute to **TRUE** when you create the capture engine.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0bdc-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0bdc-110">Requirements</span></span>



| <span data-ttu-id="d0bdc-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0bdc-111">Requirement</span></span> | <span data-ttu-id="d0bdc-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0bdc-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0bdc-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0bdc-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d0bdc-114">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0bdc-114">Windows 8 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="d0bdc-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0bdc-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d0bdc-116">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d0bdc-116">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d0bdc-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d0bdc-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0bdc-118"><dt>Mfcaptureengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0bdc-118"><dt>Mfcaptureengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0bdc-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0bdc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0bdc-120">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d0bdc-120">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0bdc-121">Attributs du moteur de capture</span><span class="sxs-lookup"><span data-stu-id="d0bdc-121">Capture Engine Attributes</span></span>](capture-engine-attributes.md)
</dt> <dt>

[<span data-ttu-id="d0bdc-122">**IMFCaptureEngine :: Initialize**</span><span class="sxs-lookup"><span data-stu-id="d0bdc-122">**IMFCaptureEngine::Initialize**</span></span>](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




