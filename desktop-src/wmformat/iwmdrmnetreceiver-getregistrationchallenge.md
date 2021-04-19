---
title: Méthode IWMDRMNetReceiver GetRegistrationChallenge (wmdrmsdk. h)
description: La méthode GetRegistrationChallenge génère un message de stimulation d’inscription Windows Media DRM pour les périphériques réseau.
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- Méthode GetRegistrationChallenge format Windows Media
- Méthode GetRegistrationChallenge format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode GetRegistrationChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521691"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="b4f69-106">IWMDRMNetReceiver :: GetRegistrationChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="b4f69-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="b4f69-107">La méthode **GetRegistrationChallenge** génère un message de stimulation d’inscription Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="b4f69-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4f69-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4f69-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="b4f69-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4f69-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4f69-110">*ppbRegistrationChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4f69-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f69-111">Adresse d’un pointeur qui reçoit l’adresse de la stimulation générée.</span><span class="sxs-lookup"><span data-stu-id="b4f69-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="b4f69-112">Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="b4f69-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="b4f69-113">*pcbRegistrationChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b4f69-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4f69-114">Adresse d’une variable qui reçoit la taille de la demande d’inscription en octets.</span><span class="sxs-lookup"><span data-stu-id="b4f69-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4f69-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4f69-115">Return value</span></span>

<span data-ttu-id="b4f69-116">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b4f69-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b4f69-117">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b4f69-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b4f69-118">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4f69-118">Return code</span></span>                                                                          | <span data-ttu-id="b4f69-119">Description</span><span class="sxs-lookup"><span data-stu-id="b4f69-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b4f69-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4f69-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b4f69-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4f69-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4f69-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b4f69-122">Remarks</span></span>

<span data-ttu-id="b4f69-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b4f69-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4f69-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4f69-124">Requirements</span></span>



| <span data-ttu-id="b4f69-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4f69-125">Requirement</span></span> | <span data-ttu-id="b4f69-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4f69-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4f69-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4f69-127">Header</span></span><br/> | <dl> <span data-ttu-id="b4f69-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4f69-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4f69-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4f69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4f69-130">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="b4f69-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="b4f69-131">**IWMDRMNetReceiver ::P rocessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="b4f69-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





