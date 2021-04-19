---
title: IMsRdpCameraRedirConfigCollection BySymbolicLink, propriété
description: Retourne un objet IMsRdpCameraRedirConfig de la collection qui correspond au lien symbolique donné de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété BySymbolicLink
- Services Bureau à distance de la propriété BySymbolicLink, interface IMsRdpCameraRedirConfigCollection
- Services Bureau à distance de l’interface IMsRdpCameraRedirConfigCollection, propriété BySymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "106544533"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="50d5d-106">IMsRdpCameraRedirConfigCollection::. Propriété BySymbolicLink</span><span class="sxs-lookup"><span data-stu-id="50d5d-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="50d5d-107">Retourne un objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la collection qui correspond au lien symbolique donné de l’interface **KSCATEGORY_VIDEO_CAMERA** pour l’appareil photo.</span><span class="sxs-lookup"><span data-stu-id="50d5d-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="50d5d-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="50d5d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d5d-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50d5d-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="50d5d-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="50d5d-110">Property value</span></span>

<span data-ttu-id="50d5d-111">Objet [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) qui correspond au lien symbolique spécifié.</span><span class="sxs-lookup"><span data-stu-id="50d5d-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="50d5d-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50d5d-112">Requirements</span></span>

| <span data-ttu-id="50d5d-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50d5d-113">Requirement</span></span> | <span data-ttu-id="50d5d-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="50d5d-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="50d5d-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50d5d-115">Minimum supported client</span></span>| <span data-ttu-id="50d5d-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="50d5d-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="50d5d-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="50d5d-117">Type library</span></span>            | <span data-ttu-id="50d5d-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="50d5d-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="50d5d-119">DLL</span><span class="sxs-lookup"><span data-stu-id="50d5d-119">DLL</span></span>                  | <span data-ttu-id="50d5d-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="50d5d-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="50d5d-121">IID</span><span class="sxs-lookup"><span data-stu-id="50d5d-121">IID</span></span>                      | <span data-ttu-id="50d5d-122">IID \_ IMsRdpCameraRedirConfigCollection est défini en tant que AE45252B-aaab-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="50d5d-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="50d5d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50d5d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d5d-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="50d5d-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>