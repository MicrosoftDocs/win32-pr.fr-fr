---
title: Méthode IWMDRMDevice GetSyncList
description: La méthode GetSyncList récupère la liste de synchronisation de licences sur l’appareil. La synchronisation des licences permet à l’ordinateur hôte de transférer des licences mises à jour sur un appareil en fonction des critères spécifiés.
ms.assetid: 772ac03b-3339-4c5f-a8fc-1c216ec665b7
keywords:
- Méthode GetSyncList Gestionnaire de périphériques Windows Media
- Méthode GetSyncList Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetSyncList
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSyncList
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381d410bd938cb90855b182e62354d48e72f16d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535964"
---
# <a name="iwmdrmdevicegetsynclist-method"></a><span data-ttu-id="4f96e-107">IWMDRMDevice :: GetSyncList, méthode</span><span class="sxs-lookup"><span data-stu-id="4f96e-107">IWMDRMDevice::GetSyncList method</span></span>

<span data-ttu-id="4f96e-108">La méthode **GetSyncList** récupère la liste de synchronisation de licences sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="4f96e-108">The **GetSyncList** method retrieves the license synchronization list on the device.</span></span> <span data-ttu-id="4f96e-109">La synchronisation des licences permet à l’ordinateur hôte de transférer des licences mises à jour sur un appareil en fonction des critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="4f96e-109">License synchronization allows the host computer to transfer updated licenses to a device according to the specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f96e-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f96e-110">Syntax</span></span>


```C++
HRESULT GetSyncList(
  [in]  DWORD cMinCountThreshold,
  [in]  DWORD cMinHoursThreshold,
  [out] BYTE  **ppbSyncList,
  [out] DWORD *pcbSyncList
);
```



## <a name="parameters"></a><span data-ttu-id="4f96e-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f96e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f96e-112">*cMinCountThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f96e-112">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f96e-113">Seuil de nombre minimal.</span><span class="sxs-lookup"><span data-stu-id="4f96e-113">Minimum count threshold.</span></span>

</dd> <dt>

<span data-ttu-id="4f96e-114">*cMinHoursThreshold* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f96e-114">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f96e-115">Seuil d’heures minimum.</span><span class="sxs-lookup"><span data-stu-id="4f96e-115">Minimum hours threshold.</span></span>

</dd> <dt>

<span data-ttu-id="4f96e-116">*ppbSyncList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4f96e-116">*ppbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f96e-117">Liste de synchronisation de la licence récupérée.</span><span class="sxs-lookup"><span data-stu-id="4f96e-117">Retrieved license synchronization list.</span></span>

</dd> <dt>

<span data-ttu-id="4f96e-118">*pcbSyncList* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4f96e-118">*pcbSyncList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f96e-119">Taille de la liste de synchronisation de licence, en octets.</span><span class="sxs-lookup"><span data-stu-id="4f96e-119">Size of the license synchronization list, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f96e-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f96e-120">Return value</span></span>

<span data-ttu-id="4f96e-121">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="4f96e-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4f96e-122">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="4f96e-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4f96e-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="4f96e-123">Return code</span></span>                                                                          | <span data-ttu-id="4f96e-124">Description</span><span class="sxs-lookup"><span data-stu-id="4f96e-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4f96e-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4f96e-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4f96e-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f96e-126">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4f96e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f96e-127">Requirements</span></span>



| <span data-ttu-id="4f96e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f96e-128">Requirement</span></span> | <span data-ttu-id="4f96e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f96e-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f96e-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="4f96e-130">Header</span></span><br/>  | <dl> <span data-ttu-id="4f96e-131"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4f96e-131"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="4f96e-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4f96e-132">Library</span></span><br/> | <dl> <span data-ttu-id="4f96e-133"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4f96e-133"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f96e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f96e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f96e-135">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="4f96e-135">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





