---
description: Contient les intrinsèques de l’appareil photo Pinhole pour l’exemple.
ms.assetid: AF7EA6A0-90C5-49A8-AD68-776BF770A448
title: Attribut MFSampleExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb9e78641c0baab0e9eda3083aafaf8fe92229f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520490"
---
# <a name="mfsampleextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="e85ad-103">\_Attribut MFSampleExtension PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="e85ad-103">MFSampleExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="e85ad-104">Contient les intrinsèques de l’appareil photo Pinhole pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="e85ad-104">Contains the pinhole camera intrinsics for the sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="e85ad-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="e85ad-105">Data type</span></span>

<span data-ttu-id="e85ad-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="e85ad-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="e85ad-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="e85ad-107">Get/set</span></span>

<span data-ttu-id="e85ad-108">Pour récupérer cet attribut, appelez [**IMFAttributes :: GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span><span class="sxs-lookup"><span data-stu-id="e85ad-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="e85ad-109">Pour définir cet attribut, appelez [**IMFAttributes :: SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span><span class="sxs-lookup"><span data-stu-id="e85ad-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="applies-to"></a><span data-ttu-id="e85ad-110">S’applique à</span><span class="sxs-lookup"><span data-stu-id="e85ad-110">Applies to</span></span>

[<span data-ttu-id="e85ad-111">**IMFSample**</span><span class="sxs-lookup"><span data-stu-id="e85ad-111">**IMFSample**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a><span data-ttu-id="e85ad-112">Notes</span><span class="sxs-lookup"><span data-stu-id="e85ad-112">Remarks</span></span>

<span data-ttu-id="e85ad-113">La valeur de l’attribut est un [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="e85ad-113">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

<span data-ttu-id="e85ad-114">Cet attribut est facultatif pour prendre en charge les caméras qui ne sont pas calibrées.</span><span class="sxs-lookup"><span data-stu-id="e85ad-114">This attribute is optional to support cameras that are not calibrated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e85ad-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e85ad-115">Requirements</span></span>



| <span data-ttu-id="e85ad-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e85ad-116">Requirement</span></span> | <span data-ttu-id="e85ad-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="e85ad-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e85ad-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e85ad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e85ad-119">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e85ad-119">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e85ad-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e85ad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e85ad-121">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e85ad-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="e85ad-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="e85ad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e85ad-123"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e85ad-123"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




