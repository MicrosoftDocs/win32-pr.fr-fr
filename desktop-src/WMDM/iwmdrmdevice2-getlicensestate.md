---
title: Méthode IWMDRMDevice2 GetLicenseState
description: La méthode GetLicenseState obtient l’état de licence.
ms.assetid: a98847f6-00ec-4211-9716-79714d7ba169
keywords:
- Méthode GetLicenseState Gestionnaire de périphériques Windows Media
- Méthode GetLicenseState Gestionnaire de périphériques Windows Media, interface IWMDRMDevice2
- Interface IWMDRMDevice2 Windows Media Gestionnaire de périphériques, méthode GetLicenseState
topic_type:
- apiref
api_name:
- IWMDRMDevice2.GetLicenseState
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d075d123ae99b26767621fb1a958cd172bc9e42c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542802"
---
# <a name="iwmdrmdevice2getlicensestate-method"></a><span data-ttu-id="ae194-106">IWMDRMDevice2 :: GetLicenseState, méthode</span><span class="sxs-lookup"><span data-stu-id="ae194-106">IWMDRMDevice2::GetLicenseState method</span></span>

<span data-ttu-id="ae194-107">La méthode **GetLicenseState** obtient l’état de licence.</span><span class="sxs-lookup"><span data-stu-id="ae194-107">The **GetLicenseState** method gets the license state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae194-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae194-108">Syntax</span></span>


```C++
HRESULT GetLicenseState(
  [in]  BYTE  *pbStateQueryData,
  [in]  DWORD cbStateQueryData,
  [out] DWORD *pdwCategory,
  [out] DWORD *pcRemainingCounts,
  [out] DWORD *pcRemainingHours,
  [out] DWORD *pdwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="ae194-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ae194-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae194-110">*pbStateQueryData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae194-110">*pbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae194-111">Pointeur vers les données interrogées de l’état de licence.</span><span class="sxs-lookup"><span data-stu-id="ae194-111">Pointer to the queried data of the license state.</span></span>

</dd> <dt>

<span data-ttu-id="ae194-112">*cbStateQueryData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ae194-112">*cbStateQueryData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ae194-113">Nombre de données interrogées.</span><span class="sxs-lookup"><span data-stu-id="ae194-113">Count of the queried data.</span></span>

</dd> <dt>

<span data-ttu-id="ae194-114">*pdwCategory* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae194-114">*pdwCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae194-115">Pointeur désignant la catégorie.</span><span class="sxs-lookup"><span data-stu-id="ae194-115">Pointer to the category.</span></span>

</dd> <dt>

<span data-ttu-id="ae194-116">*pcRemainingCounts* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae194-116">*pcRemainingCounts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae194-117">Pointeur vers les nombres restants.</span><span class="sxs-lookup"><span data-stu-id="ae194-117">Pointer to the remaining counts.</span></span>

</dd> <dt>

<span data-ttu-id="ae194-118">*pcRemainingHours* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae194-118">*pcRemainingHours* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae194-119">Pointeur vers les heures restantes.</span><span class="sxs-lookup"><span data-stu-id="ae194-119">Pointer to the remaining hours.</span></span>

</dd> <dt>

<span data-ttu-id="ae194-120">*pdwReserved* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ae194-120">*pdwReserved* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ae194-121">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="ae194-121">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae194-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ae194-122">Return value</span></span>

<span data-ttu-id="ae194-123">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ae194-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ae194-124">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ae194-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ae194-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ae194-125">Return code</span></span>                                                                          | <span data-ttu-id="ae194-126">Description</span><span class="sxs-lookup"><span data-stu-id="ae194-126">Description</span></span>                     |
|--------------------------------------------------------------------------------------|---------------------------------|
| <dl> <span data-ttu-id="ae194-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ae194-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ae194-128">La méthode est réussie.</span><span class="sxs-lookup"><span data-stu-id="ae194-128">The method succeeds.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ae194-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae194-129">Requirements</span></span>



| <span data-ttu-id="ae194-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae194-130">Requirement</span></span> | <span data-ttu-id="ae194-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae194-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ae194-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae194-132">Header</span></span><br/>  | <dl> <span data-ttu-id="ae194-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ae194-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="ae194-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae194-134">Library</span></span><br/> | <dl> <span data-ttu-id="ae194-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae194-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae194-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae194-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae194-137">**Interface IWMDRMDevice2**</span><span class="sxs-lookup"><span data-stu-id="ae194-137">**IWMDRMDevice2 Interface**</span></span>](iwmdrmdevice2.md)
</dt> </dl>

 

 





