---
title: Méthode IWMDRMNetReceiver ProcessLicenseResponse (wmdrmsdk. h)
description: La méthode ProcessLicenseResponse traite la réponse de licence envoyée par l’émetteur en réponse à une demande de licence.
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- Méthode ProcessLicenseResponse format Windows Media
- Méthode ProcessLicenseResponse format Windows Media, interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver Windows Media format, méthode ProcessLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538084"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="154ba-106">IWMDRMNetReceiver ::P méthode rocessLicenseResponse</span><span class="sxs-lookup"><span data-stu-id="154ba-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="154ba-107">La méthode **ProcessLicenseResponse** traite la réponse de licence envoyée par l’émetteur en réponse à une demande de licence.</span><span class="sxs-lookup"><span data-stu-id="154ba-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="154ba-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="154ba-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="154ba-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="154ba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="154ba-110">*pbLicenseResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="154ba-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="154ba-111">Réponse de la licence reçue de l’émetteur.</span><span class="sxs-lookup"><span data-stu-id="154ba-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="154ba-112">*cbLicenseResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="154ba-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="154ba-113">Taille de la réponse en octets.</span><span class="sxs-lookup"><span data-stu-id="154ba-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="154ba-114">*ppbWMDRMNetLicenseRepresentation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="154ba-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="154ba-115">Adresse d’une variable qui reçoit l’adresse de la représentation de licence interne pour la licence contenue dans le message de réponse de licence.</span><span class="sxs-lookup"><span data-stu-id="154ba-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="154ba-116">Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="154ba-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="154ba-117">Ce paramètre peut avoir la valeur **null** si la représentation de la licence n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="154ba-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="154ba-118">*pcbWMDRMNetLicenseRepresentation* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="154ba-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="154ba-119">Adresse d’une variable qui reçoit la taille de la représentation de licence.</span><span class="sxs-lookup"><span data-stu-id="154ba-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="154ba-120">Doit avoir la valeur **null** si *PpbWMDRMNetLicenseRepresentation* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="154ba-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="154ba-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="154ba-121">Return value</span></span>

<span data-ttu-id="154ba-122">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="154ba-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="154ba-123">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="154ba-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="154ba-124">Code de retour</span><span class="sxs-lookup"><span data-stu-id="154ba-124">Return code</span></span>                                                                                                | <span data-ttu-id="154ba-125">Description</span><span class="sxs-lookup"><span data-stu-id="154ba-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="154ba-126"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="154ba-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="154ba-127">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="154ba-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="154ba-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="154ba-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="154ba-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="154ba-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="154ba-130">Notes</span><span class="sxs-lookup"><span data-stu-id="154ba-130">Remarks</span></span>

<span data-ttu-id="154ba-131">La réponse de licence traitée à l’aide de cette méthode doit correspondre à la dernière demande de licence générée sur l’ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="154ba-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="154ba-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="154ba-132">Requirements</span></span>



| <span data-ttu-id="154ba-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="154ba-133">Requirement</span></span> | <span data-ttu-id="154ba-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="154ba-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="154ba-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="154ba-135">Header</span></span><br/> | <dl> <span data-ttu-id="154ba-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="154ba-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="154ba-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="154ba-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="154ba-138">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="154ba-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="154ba-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="154ba-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





