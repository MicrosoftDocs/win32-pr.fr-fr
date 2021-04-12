---
title: IMsRdpClientNonScriptable6 SendLocation3D, méthode
description: Envoie une valeur de latitude, de longitude et d’altitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SendLocation3D
- Méthode SendLocation3D Services Bureau à distance, interface IMsRdpClientNonScriptable6
- Services Bureau à distance de l’interface IMsRdpClientNonScriptable6, méthode SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104480521"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a><span data-ttu-id="36cd0-106">IMsRdpClientNonScriptable6 :: SendLocation3D, méthode</span><span class="sxs-lookup"><span data-stu-id="36cd0-106">IMsRdpClientNonScriptable6::SendLocation3D method</span></span>

<span data-ttu-id="36cd0-107">Envoie une valeur de latitude, de longitude et d’altitude au serveur afin que l’emplacement géographique du client puisse être reflété dans la session à distance.</span><span class="sxs-lookup"><span data-stu-id="36cd0-107">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="36cd0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36cd0-108">Syntax</span></span>

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a><span data-ttu-id="36cd0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="36cd0-109">Parameters</span></span>

<span data-ttu-id="36cd0-110">*Latitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36cd0-110">*latitude* \[in\]</span></span>

<span data-ttu-id="36cd0-111">Latitude d’un lieu géographique.</span><span class="sxs-lookup"><span data-stu-id="36cd0-111">The latitude of a geographic location.</span></span> <span data-ttu-id="36cd0-112">La plage valide des valeurs de latitude est comprise entre-90,0 et 90,0 degrés.</span><span class="sxs-lookup"><span data-stu-id="36cd0-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="36cd0-113">*longitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36cd0-113">*longitude* \[in\]</span></span>

<span data-ttu-id="36cd0-114">Longitude d’un emplacement géographique.</span><span class="sxs-lookup"><span data-stu-id="36cd0-114">The longitude of a geographic location.</span></span> <span data-ttu-id="36cd0-115">La plage valide des valeurs de latitude est comprise entre-180,0 et 180,0 degrés.</span><span class="sxs-lookup"><span data-stu-id="36cd0-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

<span data-ttu-id="36cd0-116">*altitude* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="36cd0-116">*altitude* \[in\]</span></span>

<span data-ttu-id="36cd0-117">Altitude d’un emplacement géographique en mètres.</span><span class="sxs-lookup"><span data-stu-id="36cd0-117">The altitude of a geographic location in meters.</span></span>

## <a name="return-value"></a><span data-ttu-id="36cd0-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="36cd0-118">Return value</span></span>

<span data-ttu-id="36cd0-119">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="36cd0-119">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="36cd0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36cd0-120">Requirements</span></span>

| <span data-ttu-id="36cd0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36cd0-121">Requirement</span></span> | <span data-ttu-id="36cd0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="36cd0-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="36cd0-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36cd0-123">Minimum supported client</span></span>| <span data-ttu-id="36cd0-124">Windows 10, version 1709 (build 16299)</span><span class="sxs-lookup"><span data-stu-id="36cd0-124">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="36cd0-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="36cd0-125">Type library</span></span>            | <span data-ttu-id="36cd0-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="36cd0-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="36cd0-127">DLL</span><span class="sxs-lookup"><span data-stu-id="36cd0-127">DLL</span></span>                  | <span data-ttu-id="36cd0-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="36cd0-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="36cd0-129">IID</span><span class="sxs-lookup"><span data-stu-id="36cd0-129">IID</span></span>                      | <span data-ttu-id="36cd0-130">IID \_ IMsRdpClientNonScriptable6 est défini comme 05293249-B28B-4db8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="36cd0-130">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="36cd0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36cd0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36cd0-132">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="36cd0-132">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
