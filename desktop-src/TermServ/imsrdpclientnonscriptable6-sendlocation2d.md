---
title: IMsRdpClientNonScriptable6 SendLocation2D, méthode
description: Envoie une valeur de latitude et de longitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendLocation2D
- Méthode SendLocation2D Services Bureau à distance, interface IMsRdpClientNonScriptable6
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6, méthode SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "103745341"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="e4360-106">IMsRdpClientNonScriptable6 :: SendLocation2D, méthode</span><span class="sxs-lookup"><span data-stu-id="e4360-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="e4360-107">Envoie une valeur de latitude et de longitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="e4360-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4360-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4360-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="e4360-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4360-109">Parameters</span></span>

<span data-ttu-id="e4360-110">*Latitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4360-110">*latitude* \[in\]</span></span>

<span data-ttu-id="e4360-111">Latitude d’un lieu géographique.</span><span class="sxs-lookup"><span data-stu-id="e4360-111">The latitude of a geographic location.</span></span> <span data-ttu-id="e4360-112">La plage valide des valeurs de latitude est comprise entre-90,0 et 90,0 degrés.</span><span class="sxs-lookup"><span data-stu-id="e4360-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="e4360-113">*longitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4360-113">*longitude* \[in\]</span></span>

<span data-ttu-id="e4360-114">Longitude d’un emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="e4360-114">The longitude of a geographic location.</span></span> <span data-ttu-id="e4360-115">La plage valide des valeurs de latitude est comprise entre-180,0 et 180,0 degrés.</span><span class="sxs-lookup"><span data-stu-id="e4360-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4360-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4360-116">Return value</span></span>

<span data-ttu-id="e4360-117">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="e4360-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4360-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4360-118">Requirements</span></span>

| <span data-ttu-id="e4360-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4360-119">Requirement</span></span> | <span data-ttu-id="e4360-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4360-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e4360-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4360-121">Minimum supported client</span></span>| <span data-ttu-id="e4360-122">Windows 10, version 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="e4360-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="e4360-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e4360-123">Type library</span></span>            | <span data-ttu-id="e4360-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e4360-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e4360-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e4360-125">DLL</span></span>                  | <span data-ttu-id="e4360-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e4360-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e4360-127">IID</span><span class="sxs-lookup"><span data-stu-id="e4360-127">IID</span></span>                      | <span data-ttu-id="e4360-128">IID \_ IMsRdpClientNonScriptable6 est défini comme 05293249-B28B-4db8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="e4360-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="e4360-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4360-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4360-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="e4360-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
