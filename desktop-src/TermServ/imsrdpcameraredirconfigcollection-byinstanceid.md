---
title: IMsRdpCameraRedirConfigCollection ByInstanceId, propriété
description: Retourne un objet IMsRdpCameraRedirConfig de la collection qui correspond à l’ID d’instance spécifié.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ByInstanceId
- Services Bureau à distance de la propriété ByInstanceId, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480528"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="a7ac1-106">IMsRdpCameraRedirConfigCollection :: ByInstanceId, propriété</span><span class="sxs-lookup"><span data-stu-id="a7ac1-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="a7ac1-107">Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond à l’ID d’instance spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="a7ac1-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7ac1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7ac1-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="a7ac1-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="a7ac1-110">Property value</span></span>

<span data-ttu-id="a7ac1-111">Objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) qui correspond à l’ID d’instance spécifié.</span><span class="sxs-lookup"><span data-stu-id="a7ac1-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ac1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7ac1-112">Requirements</span></span>

| <span data-ttu-id="a7ac1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7ac1-113">Requirement</span></span> | <span data-ttu-id="a7ac1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7ac1-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="a7ac1-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7ac1-115">Minimum supported client</span></span>| <span data-ttu-id="a7ac1-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="a7ac1-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="a7ac1-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="a7ac1-117">Type library</span></span>            | <span data-ttu-id="a7ac1-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a7ac1-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="a7ac1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ac1-119">DLL</span></span>                  | <span data-ttu-id="a7ac1-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="a7ac1-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="a7ac1-121">IID</span><span class="sxs-lookup"><span data-stu-id="a7ac1-121">IID</span></span>                      | <span data-ttu-id="a7ac1-122">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="a7ac1-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="a7ac1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7ac1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ac1-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="a7ac1-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>