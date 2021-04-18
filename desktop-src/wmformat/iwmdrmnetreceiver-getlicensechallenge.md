---
title: Méthode IWMDRMNetReceiver GetLicenseChallenge (wmdrmsdk. h)
description: La méthode GetLicenseChallenge génère un défi de licence Windows Media DRM pour les périphériques réseau qui peut être envoyé à un émetteur lors de la demande de contenu protégé.
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- Méthode GetLicenseChallenge format Windows Media
- Méthode GetLicenseChallenge format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode GetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540200"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="dc925-106">IWMDRMNetReceiver :: GetLicenseChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="dc925-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="dc925-107">La méthode **GetLicenseChallenge** génère un défi de licence Windows Media DRM pour les périphériques réseau qui peut être envoyé à un émetteur lors de la demande de contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="dc925-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc925-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc925-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="dc925-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc925-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc925-110">*bstrAction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc925-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc925-111">Action pour laquelle générer la stimulation.</span><span class="sxs-lookup"><span data-stu-id="dc925-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="dc925-112">*ppbLicenseChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dc925-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc925-113">Adresse d’un pointeur défini sur l’adresse de la stimulation générée.</span><span class="sxs-lookup"><span data-stu-id="dc925-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="dc925-114">Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="dc925-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="dc925-115">*pcbLicenseChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dc925-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc925-116">Adresse d’une variable qui reçoit la taille de la demande de licence en octets.</span><span class="sxs-lookup"><span data-stu-id="dc925-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc925-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc925-117">Return value</span></span>

<span data-ttu-id="dc925-118">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dc925-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dc925-119">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dc925-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dc925-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dc925-120">Return code</span></span>                                                                          | <span data-ttu-id="dc925-121">Description</span><span class="sxs-lookup"><span data-stu-id="dc925-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dc925-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dc925-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dc925-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="dc925-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dc925-124">Notes</span><span class="sxs-lookup"><span data-stu-id="dc925-124">Remarks</span></span>

<span data-ttu-id="dc925-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dc925-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc925-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc925-126">Requirements</span></span>



| <span data-ttu-id="dc925-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc925-127">Requirement</span></span> | <span data-ttu-id="dc925-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc925-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dc925-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc925-129">Header</span></span><br/> | <dl> <span data-ttu-id="dc925-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc925-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc925-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dc925-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc925-132">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="dc925-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="dc925-133">**IWMDRMNetReceiver ::P rocessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="dc925-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





