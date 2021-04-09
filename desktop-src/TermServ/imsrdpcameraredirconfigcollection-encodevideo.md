---
title: IMsRdpCameraRedirConfigCollection EncodeVideo, propriété
description: Spécifie si le flux vidéo est au format H. 264 encodé.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété EncodeVideo
- Services Bureau à distance de la propriété EncodeVideo, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété EncodeVideo
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108359"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="ca6c1-106">IMsRdpCameraRedirConfigCollection :: EncodeVideo, propriété</span><span class="sxs-lookup"><span data-stu-id="ca6c1-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="ca6c1-107">Spécifie si le flux vidéo est au format H. 264 encodé.</span><span class="sxs-lookup"><span data-stu-id="ca6c1-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="ca6c1-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ca6c1-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca6c1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca6c1-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="ca6c1-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ca6c1-110">Property value</span></span>

<span data-ttu-id="ca6c1-111">Valeur qui indique si le flux vidéo est ou non encodé en H. 264.</span><span class="sxs-lookup"><span data-stu-id="ca6c1-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca6c1-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca6c1-112">Requirements</span></span>

| <span data-ttu-id="ca6c1-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca6c1-113">Requirement</span></span> | <span data-ttu-id="ca6c1-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca6c1-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="ca6c1-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca6c1-115">Minimum supported client</span></span>| <span data-ttu-id="ca6c1-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="ca6c1-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="ca6c1-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ca6c1-117">Type library</span></span>            | <span data-ttu-id="ca6c1-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ca6c1-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="ca6c1-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ca6c1-119">DLL</span></span>                  | <span data-ttu-id="ca6c1-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ca6c1-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="ca6c1-121">IID</span><span class="sxs-lookup"><span data-stu-id="ca6c1-121">IID</span></span>                      | <span data-ttu-id="ca6c1-122">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="ca6c1-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="ca6c1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca6c1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca6c1-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="ca6c1-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>