---
title: IMsRdpCameraRedirConfig ParentInstanceId, propriété
description: Obtient l’ID d’instance d’appareil parent de l’appareil photo.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ParentInstanceId
- Services Bureau à distance de la propriété ParentInstanceId, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété ParentInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106515298"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="65717-106">IMsRdpCameraRedirConfig ::P propriété arentInstanceId</span><span class="sxs-lookup"><span data-stu-id="65717-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="65717-107">Obtient l’ID d’instance d’appareil parent de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="65717-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="65717-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="65717-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="65717-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65717-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="65717-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="65717-110">Property value</span></span>

<span data-ttu-id="65717-111">ID d’instance d’appareil parent de l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="65717-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="65717-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65717-112">Requirements</span></span>

| <span data-ttu-id="65717-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65717-113">Requirement</span></span> | <span data-ttu-id="65717-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="65717-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="65717-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65717-115">Minimum supported client</span></span>| <span data-ttu-id="65717-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="65717-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="65717-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="65717-117">Type library</span></span>            | <span data-ttu-id="65717-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="65717-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="65717-119">DLL</span><span class="sxs-lookup"><span data-stu-id="65717-119">DLL</span></span>                  | <span data-ttu-id="65717-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="65717-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="65717-121">IID</span><span class="sxs-lookup"><span data-stu-id="65717-121">IID</span></span>                      | <span data-ttu-id="65717-122">IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="65717-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="65717-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65717-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65717-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="65717-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>