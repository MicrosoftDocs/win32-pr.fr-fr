---
description: Contient le extrinsics de l’appareil photo pour l’exemple.
ms.assetid: C970E958-3866-491A-9806-DB300834360E
title: Attribut MFSampleExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3340f1ab84061fa00e12fa65960f1b2902690816
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533615"
---
# <a name="mfsampleextension_cameraextrinsics-attribute"></a><span data-ttu-id="5043b-103">\_Attribut MFSampleExtension CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="5043b-103">MFSampleExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="5043b-104">Contient le extrinsics de l’appareil photo pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="5043b-104">Contains the camera extrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="5043b-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="5043b-105">Data type</span></span>

<span data-ttu-id="5043b-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="5043b-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="5043b-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="5043b-107">Get/set</span></span>

<span data-ttu-id="5043b-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="5043b-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="5043b-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="5043b-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="5043b-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="5043b-110">Applies to</span></span>

[<span data-ttu-id="5043b-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="5043b-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="5043b-112">Notes</span><span class="sxs-lookup"><span data-stu-id="5043b-112">Remarks</span></span>

<span data-ttu-id="5043b-113">La valeur de l’attribut est un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="5043b-113">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

<span data-ttu-id="5043b-114">Cet attribut est facultatif pour prendre en charge les caméras qui ne sont pas calibrées.</span><span class="sxs-lookup"><span data-stu-id="5043b-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="5043b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5043b-115">Requirements</span></span>



| <span data-ttu-id="5043b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5043b-116">Requirement</span></span> | <span data-ttu-id="5043b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="5043b-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5043b-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5043b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5043b-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5043b-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5043b-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5043b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5043b-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5043b-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="5043b-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5043b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5043b-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="5043b-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5043b-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5043b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5043b-125">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5043b-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




