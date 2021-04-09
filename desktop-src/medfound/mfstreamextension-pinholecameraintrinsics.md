---
description: Contient les intrinsèques de l’appareil photo Pinhole pour le flux.
ms.assetid: 7E5E7C60-9C3F-406B-A7DD-A953181CD314
title: Attribut MFStreamExtension_PinholeCameraIntrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ee9ad848f0b8cc12c2496544d98b4ef17332151
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951622"
---
# <a name="mfstreamextension_pinholecameraintrinsics-attribute"></a><span data-ttu-id="35d65-103">\_Attribut MFStreamExtension PinholeCameraIntrinsics</span><span class="sxs-lookup"><span data-stu-id="35d65-103">MFStreamExtension\_PinholeCameraIntrinsics attribute</span></span>

<span data-ttu-id="35d65-104">Contient les intrinsèques de l’appareil photo Pinhole pour le flux.</span><span class="sxs-lookup"><span data-stu-id="35d65-104">Contains the pinhole camera intrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="35d65-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="35d65-105">Data type</span></span>

<span data-ttu-id="35d65-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="35d65-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="35d65-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="35d65-107">Get/set</span></span>

<span data-ttu-id="35d65-108">Pour récupérer cet attribut, appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="35d65-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="35d65-109">Notes</span><span class="sxs-lookup"><span data-stu-id="35d65-109">Remarks</span></span>

<span data-ttu-id="35d65-110">La valeur de l’attribut est un [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span><span class="sxs-lookup"><span data-stu-id="35d65-110">The value of the attribute is a [**MFPinholeCameraIntrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfpinholecameraintrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="35d65-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35d65-111">Requirements</span></span>



| <span data-ttu-id="35d65-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35d65-112">Requirement</span></span> | <span data-ttu-id="35d65-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="35d65-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="35d65-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35d65-114">Minimum supported client</span></span><br/> | <span data-ttu-id="35d65-115">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35d65-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="35d65-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35d65-116">Minimum supported server</span></span><br/> | <span data-ttu-id="35d65-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35d65-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="35d65-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="35d65-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="35d65-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="35d65-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




