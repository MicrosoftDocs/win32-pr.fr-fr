---
title: IMsRdpCameraRedirConfigCollection EncodingQuality, propriété
description: Spécifie la qualité d’encodage (vitesse de transmission).
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EncodingQuality
- Services Bureau à distance de la propriété EncodingQuality, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété EncodingQuality
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480537"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="512d9-106">IMsRdpCameraRedirConfigCollection :: EncodingQuality, propriété</span><span class="sxs-lookup"><span data-stu-id="512d9-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="512d9-107">Spécifie la qualité d’encodage (vitesse de transmission).</span><span class="sxs-lookup"><span data-stu-id="512d9-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="512d9-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="512d9-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="512d9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="512d9-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="512d9-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="512d9-110">Property value</span></span>

<span data-ttu-id="512d9-111">L’une des valeurs d’énumération **CameraRedirEncodingQuality** suivantes qui spécifient la qualité d’encodage (vitesse de transmission).</span><span class="sxs-lookup"><span data-stu-id="512d9-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="512d9-112">Nom du membre enum</span><span class="sxs-lookup"><span data-stu-id="512d9-112">Enum member name</span></span> | <span data-ttu-id="512d9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="512d9-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="512d9-114">encodingQualityLow</span><span class="sxs-lookup"><span data-stu-id="512d9-114">encodingQualityLow</span></span> | <span data-ttu-id="512d9-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="512d9-115">0x0000</span></span> |
| <span data-ttu-id="512d9-116">encodingQualityMedium</span><span class="sxs-lookup"><span data-stu-id="512d9-116">encodingQualityMedium</span></span> | <span data-ttu-id="512d9-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="512d9-117">0x0001</span></span> |
| <span data-ttu-id="512d9-118">encodingQualityHigh</span><span class="sxs-lookup"><span data-stu-id="512d9-118">encodingQualityHigh</span></span> | <span data-ttu-id="512d9-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="512d9-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="512d9-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="512d9-120">Requirements</span></span>

| <span data-ttu-id="512d9-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="512d9-121">Requirement</span></span> | <span data-ttu-id="512d9-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="512d9-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="512d9-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="512d9-123">Minimum supported client</span></span>| <span data-ttu-id="512d9-124">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="512d9-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="512d9-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="512d9-125">Type library</span></span>            | <span data-ttu-id="512d9-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="512d9-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="512d9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="512d9-127">DLL</span></span>                  | <span data-ttu-id="512d9-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="512d9-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="512d9-129">IID</span><span class="sxs-lookup"><span data-stu-id="512d9-129">IID</span></span>                      | <span data-ttu-id="512d9-130">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="512d9-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="512d9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="512d9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="512d9-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="512d9-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>