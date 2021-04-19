---
title: IMsRdpCameraRedirConfigCollection ByIndex, propriété
description: Retourne un objet IMsRdpCameraRedirConfig par son index dans la collection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ByIndex
- Services Bureau à distance de la propriété ByIndex, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106544532"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="0aa6e-106">IMsRdpCameraRedirConfigCollection :: ByIndex, propriété</span><span class="sxs-lookup"><span data-stu-id="0aa6e-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="0aa6e-107">Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) par son index dans la collection.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="0aa6e-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0aa6e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0aa6e-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="0aa6e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0aa6e-110">Property value</span></span>

<span data-ttu-id="0aa6e-111">Objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) qui correspond à l’index spécifié.</span><span class="sxs-lookup"><span data-stu-id="0aa6e-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="0aa6e-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0aa6e-112">Requirements</span></span>

| <span data-ttu-id="0aa6e-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0aa6e-113">Requirement</span></span> | <span data-ttu-id="0aa6e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="0aa6e-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="0aa6e-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0aa6e-115">Minimum supported client</span></span>| <span data-ttu-id="0aa6e-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="0aa6e-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="0aa6e-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0aa6e-117">Type library</span></span>            | <span data-ttu-id="0aa6e-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0aa6e-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="0aa6e-119">DLL</span><span class="sxs-lookup"><span data-stu-id="0aa6e-119">DLL</span></span>                  | <span data-ttu-id="0aa6e-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0aa6e-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="0aa6e-121">IID</span><span class="sxs-lookup"><span data-stu-id="0aa6e-121">IID</span></span>                      | <span data-ttu-id="0aa6e-122">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="0aa6e-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="0aa6e-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0aa6e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0aa6e-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="0aa6e-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>