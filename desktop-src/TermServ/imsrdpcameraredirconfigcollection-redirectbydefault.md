---
title: IMsRdpCameraRedirConfigCollection EncodeVideo, propriété
description: Spécifie si une nouvelle caméra est redirigée par défaut.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété RedirectByDefault
- Services Bureau à distance de la propriété RedirectByDefault, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108358"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="63403-106">IMsRdpCameraRedirConfigCollection :: RedirectByDefault, propriété</span><span class="sxs-lookup"><span data-stu-id="63403-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="63403-107">Spécifie si une nouvelle caméra est redirigée par défaut.</span><span class="sxs-lookup"><span data-stu-id="63403-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="63403-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="63403-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="63403-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63403-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="63403-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="63403-110">Property value</span></span>

<span data-ttu-id="63403-111">Valeur qui indique si une nouvelle caméra est redirigée par défaut.</span><span class="sxs-lookup"><span data-stu-id="63403-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="63403-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="63403-112">Requirements</span></span>

| <span data-ttu-id="63403-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="63403-113">Requirement</span></span> | <span data-ttu-id="63403-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="63403-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="63403-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="63403-115">Minimum supported client</span></span>| <span data-ttu-id="63403-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="63403-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="63403-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="63403-117">Type library</span></span>            | <span data-ttu-id="63403-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="63403-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="63403-119">DLL</span><span class="sxs-lookup"><span data-stu-id="63403-119">DLL</span></span>                  | <span data-ttu-id="63403-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="63403-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="63403-121">IID</span><span class="sxs-lookup"><span data-stu-id="63403-121">IID</span></span>                      | <span data-ttu-id="63403-122">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="63403-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="63403-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="63403-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63403-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="63403-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>