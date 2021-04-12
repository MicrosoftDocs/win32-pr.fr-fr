---
title: IMsRdpClientNonScriptable7 CameraRedirConfigCollection, propriété
description: Obtient la collection des appareils photo (et les configurations associées) qui sont disponibles pour la redirection.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CameraRedirConfigCollection
- Services Bureau à distance de la propriété CameraRedirConfigCollection, interface IMsRdpClientNonScriptable7
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable7, propriété CameraRedirConfigCollection
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7.CameraRedirConfigCollection
- IMsRdpClientNonScriptable7.get_CameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 817d3d73b4abbf8aa8b4126fd99ed7d11c3fff51
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104317534"
---
# <a name="imsrdpclientnonscriptable7cameraredirconfigcollection-property"></a><span data-ttu-id="eda42-106">IMsRdpClientNonScriptable7 :: CameraRedirConfigCollection, propriété</span><span class="sxs-lookup"><span data-stu-id="eda42-106">IMsRdpClientNonScriptable7::CameraRedirConfigCollection property</span></span>

<span data-ttu-id="eda42-107">Obtient la collection des appareils photo (et les configurations associées) qui sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="eda42-107">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

<span data-ttu-id="eda42-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="eda42-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eda42-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eda42-109">Syntax</span></span>


```C++
HRESULT get_CameraRedirConfigCollection(
  [out, retval] IMsRdpCameraRedirConfigCollection** ppCameraCollection
);
```

## <a name="property-value"></a><span data-ttu-id="eda42-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="eda42-110">Property value</span></span>

<span data-ttu-id="eda42-111">Un [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) qui représente la collection d’appareils photo (et les configurations associées) qui sont disponibles pour la redirection.</span><span class="sxs-lookup"><span data-stu-id="eda42-111">An [IMsRdpCameraRedirConfigCollection](imsrdpcameraredirconfigcollection.md) that represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="eda42-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eda42-112">Requirements</span></span>

| <span data-ttu-id="eda42-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eda42-113">Requirement</span></span> | <span data-ttu-id="eda42-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="eda42-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="eda42-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eda42-115">Minimum supported client</span></span>| <span data-ttu-id="eda42-116">Windows 10, version 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="eda42-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="eda42-117">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eda42-117">Type library</span></span>            | <span data-ttu-id="eda42-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="eda42-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="eda42-119">DLL</span><span class="sxs-lookup"><span data-stu-id="eda42-119">DLL</span></span>                  | <span data-ttu-id="eda42-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="eda42-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="eda42-121">IID</span><span class="sxs-lookup"><span data-stu-id="eda42-121">IID</span></span>                      | <span data-ttu-id="eda42-122">IID \_ IMsRdpClientNonScriptable7 est défini en tant que 71B4A60A-fe21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="eda42-122">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>          |

## <a name="see-also"></a><span data-ttu-id="eda42-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eda42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eda42-124">**IMsRdpClientNonScriptable7**</span><span class="sxs-lookup"><span data-stu-id="eda42-124">**IMsRdpClientNonScriptable7**</span></span>](imsrdpclientnonscriptable7.md)
</dt> </dl>