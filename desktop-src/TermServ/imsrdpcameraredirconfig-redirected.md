---
title: IMsRdpCameraRedirConfig Redirected, propriété
description: Spécifie si l’appareil photo est redirigé.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de propriétés redirigées
- Services Bureau à distance de propriété redirigée, interface IMsRdpCameraRedirConfig
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfig, propriété redirigée
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480553"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="14568-106">IMsRdpCameraRedirConfig :: redirection, propriété</span><span class="sxs-lookup"><span data-stu-id="14568-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="14568-107">Spécifie si l’appareil photo est redirigé.</span><span class="sxs-lookup"><span data-stu-id="14568-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="14568-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="14568-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="14568-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14568-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="14568-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="14568-110">Property value</span></span>

<span data-ttu-id="14568-111">Valeur qui spécifie si l’appareil photo est redirigé.</span><span class="sxs-lookup"><span data-stu-id="14568-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="14568-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14568-112">Requirements</span></span>

| <span data-ttu-id="14568-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14568-113">Requirement</span></span> | <span data-ttu-id="14568-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="14568-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="14568-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14568-115">Minimum supported client</span></span>| <span data-ttu-id="14568-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="14568-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="14568-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="14568-117">Type library</span></span>            | <span data-ttu-id="14568-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="14568-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="14568-119">DLL</span><span class="sxs-lookup"><span data-stu-id="14568-119">DLL</span></span>                  | <span data-ttu-id="14568-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="14568-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="14568-121">IID</span><span class="sxs-lookup"><span data-stu-id="14568-121">IID</span></span>                      | <span data-ttu-id="14568-122">IID \_ IMsRdpCameraRedirConfig est défini comme 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="14568-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="14568-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14568-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14568-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="14568-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>