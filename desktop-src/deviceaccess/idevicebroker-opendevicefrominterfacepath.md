---
title: Méthode IDeviceBroker OpenDeviceFromInterfacePath
description: Tente d’ouvrir une instance d’interface d’appareil pour le compte d’un client. IID 8604b268-34A6-4b1A-A59F-CDBD8379FD98.
ms.assetid: 5ADDB994-3AAB-49B2-8B83-F71883AFD854
keywords:
- Méthode OpenDeviceFromInterfacePath API Broker d’accès du périphérique
- Méthode OpenDeviceFromInterfacePath API Broker d’accès du périphérique, interface IDeviceBroker
- API Broker d’accès du périphérique de l’interface IDeviceBroker, méthode OpenDeviceFromInterfacePath
topic_type:
- apiref
api_name:
- IDeviceBroker.OpenDeviceFromInterfacePath
api_type:
- COM
ms.topic: article
ms.date: 02/11/2020
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5363600455ee1ba5c1c86cb12690afd242f68118
ms.sourcegitcommit: 01a4383738056cf3de4f45f36d98ef73d4dc694d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104381453"
---
# <a name="idevicebrokeropendevicefrominterfacepath-method"></a><span data-ttu-id="2e454-107">IDeviceBroker :: OpenDeviceFromInterfacePath, méthode</span><span class="sxs-lookup"><span data-stu-id="2e454-107">IDeviceBroker::OpenDeviceFromInterfacePath method</span></span>

> [!Important]  
> <span data-ttu-id="2e454-108">Ces interfaces ne sont pas prises en charge et ne doivent pas être utilisées.</span><span class="sxs-lookup"><span data-stu-id="2e454-108">These interfaces are not supported and should not be used.</span></span> <span data-ttu-id="2e454-109">Utilisez plutôt les API dans la [référence de programmation C++ de l’API d’accès à l’appareil](device-access-api-c---programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="2e454-109">Use the APIs in the [Device Access API C++ Programming Reference](device-access-api-c---programming-reference.md) instead.</span></span>

<span data-ttu-id="2e454-110">Tente d’ouvrir une instance d’interface d’appareil pour le compte d’un client.</span><span class="sxs-lookup"><span data-stu-id="2e454-110">Attempts to open a device interface instance on behalf of a client.</span></span> <span data-ttu-id="2e454-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span><span class="sxs-lookup"><span data-stu-id="2e454-111">IID = 8604b268-34A6-4b1A-A59F-CDBD8379FD98.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e454-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2e454-112">Syntax</span></span>

```C++
HRESULT OpenDeviceFromInterfacePath(
  [in]  PCWSTR pszDeviceInterfacePath,
  [in]  DWORD  desiredAccess,
  [in]  DWORD  shareMode,
  [in]  DWORD  flagsAndAttributes,
  [out] Handle *phDevice
);
```

## <a name="parameters"></a><span data-ttu-id="2e454-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e454-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e454-114">*pszDeviceInterfacePath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e454-114">*pszDeviceInterfacePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e454-115">Instance d’interface d’appareil à ouvrir.</span><span class="sxs-lookup"><span data-stu-id="2e454-115">Device interface instance to open.</span></span>

</dd> <dt>

<span data-ttu-id="2e454-116">*desiredAccess* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e454-116">*desiredAccess* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e454-117">Accès souhaité à passer à Open.</span><span class="sxs-lookup"><span data-stu-id="2e454-117">Desired access to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="2e454-118">*shareMode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e454-118">*shareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e454-119">Mode de partage à passer à l’ouverture.</span><span class="sxs-lookup"><span data-stu-id="2e454-119">Share mode to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="2e454-120">*flagsAndAttributes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2e454-120">*flagsAndAttributes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e454-121">Indicateurs et attributs à passer à Open.</span><span class="sxs-lookup"><span data-stu-id="2e454-121">Flags and attributes to be passed to open.</span></span>

</dd> <dt>

<span data-ttu-id="2e454-122">*\* phDevice* \[\]</span><span class="sxs-lookup"><span data-stu-id="2e454-122">*\*phDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e454-123">Handle résultant si la tentative d’ouverture a réussi.</span><span class="sxs-lookup"><span data-stu-id="2e454-123">Resulting handle if open was successful.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e454-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2e454-124">Return value</span></span>

<span data-ttu-id="2e454-125">Si cette fonction est réussie, elle retourne S_OK.</span><span class="sxs-lookup"><span data-stu-id="2e454-125">If this function succeeds, it returns S_OK.</span></span> <span data-ttu-id="2e454-126">Sinon, elle retourne un code d’erreur HRESULT.</span><span class="sxs-lookup"><span data-stu-id="2e454-126">Otherwise, it returns an HRESULT error code.</span></span>
