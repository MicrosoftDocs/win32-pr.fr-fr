---
title: IMsRdpCameraRedirConfig DeviceExists property
description: Spécifie si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DeviceExists
- Services Bureau à distance de la propriété DeviceExists, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété DeviceExists
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480561"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="52d4a-106">IMsRdpCameraRedirConfig ::D propriété eviceExists</span><span class="sxs-lookup"><span data-stu-id="52d4a-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="52d4a-107">Spécifie si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).</span><span class="sxs-lookup"><span data-stu-id="52d4a-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="52d4a-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="52d4a-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="52d4a-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52d4a-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="52d4a-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="52d4a-110">Property value</span></span>

<span data-ttu-id="52d4a-111">Valeur qui indique si le périphérique de l’appareil photo existe actuellement (c’est-à-dire que l’appareil photo est connecté).</span><span class="sxs-lookup"><span data-stu-id="52d4a-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="52d4a-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52d4a-112">Requirements</span></span>

| <span data-ttu-id="52d4a-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52d4a-113">Requirement</span></span> | <span data-ttu-id="52d4a-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="52d4a-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="52d4a-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52d4a-115">Minimum supported client</span></span>| <span data-ttu-id="52d4a-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="52d4a-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="52d4a-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="52d4a-117">Type library</span></span>            | <span data-ttu-id="52d4a-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="52d4a-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="52d4a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="52d4a-119">DLL</span></span>                  | <span data-ttu-id="52d4a-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="52d4a-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="52d4a-121">IID</span><span class="sxs-lookup"><span data-stu-id="52d4a-121">IID</span></span>                      | <span data-ttu-id="52d4a-122">IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="52d4a-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="52d4a-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52d4a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52d4a-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="52d4a-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>