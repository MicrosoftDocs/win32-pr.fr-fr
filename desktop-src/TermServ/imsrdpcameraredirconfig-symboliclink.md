---
title: IMsRdpCameraRedirConfig SymbolicLink, propriété
description: Obtient le lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété SymbolicLink
- Services Bureau à distance de la propriété SymbolicLink, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété SymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103845658"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="35ad3-106">IMsRdpCameraRedirConfig :: SymbolicLink, propriété</span><span class="sxs-lookup"><span data-stu-id="35ad3-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="35ad3-107">Obtient le lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="35ad3-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="35ad3-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="35ad3-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ad3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35ad3-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="35ad3-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="35ad3-110">Property value</span></span>

<span data-ttu-id="35ad3-111">Lien symbolique de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="35ad3-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ad3-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ad3-112">Requirements</span></span>

| <span data-ttu-id="35ad3-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35ad3-113">Requirement</span></span> | <span data-ttu-id="35ad3-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ad3-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="35ad3-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ad3-115">Minimum supported client</span></span>| <span data-ttu-id="35ad3-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="35ad3-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="35ad3-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="35ad3-117">Type library</span></span>            | <span data-ttu-id="35ad3-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="35ad3-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="35ad3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="35ad3-119">DLL</span></span>                  | <span data-ttu-id="35ad3-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="35ad3-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="35ad3-121">IID</span><span class="sxs-lookup"><span data-stu-id="35ad3-121">IID</span></span>                      | <span data-ttu-id="35ad3-122">IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="35ad3-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="35ad3-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ad3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ad3-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="35ad3-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>