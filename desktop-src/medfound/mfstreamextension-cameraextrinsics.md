---
description: Contient le extrinsics d’appareil photo pour le flux.
ms.assetid: 2236C135-BA3D-4C1B-8A39-5E23EF67425A
title: Attribut MFStreamExtension_CameraExtrinsics (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a551aaaef48100d6104804e54f7e0ddfac3f5cb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114402"
---
# <a name="mfstreamextension_cameraextrinsics-attribute"></a><span data-ttu-id="1b567-103">\_Attribut MFStreamExtension CameraExtrinsics</span><span class="sxs-lookup"><span data-stu-id="1b567-103">MFStreamExtension\_CameraExtrinsics attribute</span></span>

<span data-ttu-id="1b567-104">Contient le extrinsics d’appareil photo pour le flux.</span><span class="sxs-lookup"><span data-stu-id="1b567-104">Contains the camera extrinsics for the stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="1b567-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="1b567-105">Data type</span></span>

<span data-ttu-id="1b567-106">Tableau d’octets</span><span class="sxs-lookup"><span data-stu-id="1b567-106">Byte array</span></span>

## <a name="getset"></a><span data-ttu-id="1b567-107">Obtenir/définir</span><span class="sxs-lookup"><span data-stu-id="1b567-107">Get/set</span></span>

<span data-ttu-id="1b567-108">Pour récupérer cet attribut, appelez [**IMFMediaSourceEx :: GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span><span class="sxs-lookup"><span data-stu-id="1b567-108">To get this attribute, call [**IMFMediaSourceEx::GetStreamAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasourceex-getstreamattributes).</span></span>

## <a name="remarks"></a><span data-ttu-id="1b567-109">Notes</span><span class="sxs-lookup"><span data-stu-id="1b567-109">Remarks</span></span>

<span data-ttu-id="1b567-110">La valeur de l’attribut est un [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span><span class="sxs-lookup"><span data-stu-id="1b567-110">The value of the attribute is a [**MFCameraExtrinsics**](/windows/desktop/api/mfapi/ns-mfapi-mfcameraextrinsics).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b567-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b567-111">Requirements</span></span>



| <span data-ttu-id="1b567-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b567-112">Requirement</span></span> | <span data-ttu-id="1b567-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b567-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b567-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b567-114">Minimum supported client</span></span><br/> | <span data-ttu-id="1b567-115">Applications de \[ Bureau Windows 10 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b567-115">Windows 10 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1b567-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b567-116">Minimum supported server</span></span><br/> | <span data-ttu-id="1b567-117">Applications de bureau Windows Server 2012 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1b567-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="1b567-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b567-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b567-119"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b567-119"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




