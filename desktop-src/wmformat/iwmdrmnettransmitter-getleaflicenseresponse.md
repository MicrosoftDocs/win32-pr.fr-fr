---
title: Méthode IWMDRMNetTransmitter GetLeafLicenseResponse (wmdrmsdk. h)
description: La méthode GetLeafLicenseResponse génère un message de réponse de licence feuille.
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- Méthode GetLeafLicenseResponse format Windows Media
- Méthode GetLeafLicenseResponse format Windows Media, interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter Windows Media format, méthode GetLeafLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540359"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="c7291-106">IWMDRMNetTransmitter :: GetLeafLicenseResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="c7291-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="c7291-107">La méthode **GetLeafLicenseResponse** génère un message de réponse de licence feuille.</span><span class="sxs-lookup"><span data-stu-id="c7291-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7291-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7291-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="c7291-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7291-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7291-110">*bstrKID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7291-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7291-111">Identificateur de clé encodé en base64 à utiliser pour la nouvelle licence feuille.</span><span class="sxs-lookup"><span data-stu-id="c7291-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="c7291-112">L’identificateur de clé doit être une valeur GUID générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="c7291-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="c7291-113">*pPolicy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7291-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7291-114">Pointeur vers la structure de [**\_ stratégie WMDRMNET**](wmdrmnet-policy.md) qui définit la stratégie à utiliser pour la licence feuille.</span><span class="sxs-lookup"><span data-stu-id="c7291-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="c7291-115">*ppIWMDRMEncrypt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7291-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7291-116">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) qui peut être utilisée pour chiffrer les données de la nouvelle licence feuille.</span><span class="sxs-lookup"><span data-stu-id="c7291-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="c7291-117">*ppbLicenseResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7291-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7291-118">Adresse d’une variable qui reçoit l’adresse de la réponse de licence générée.</span><span class="sxs-lookup"><span data-stu-id="c7291-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="c7291-119">Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="c7291-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="c7291-120">*pcbLicenseResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c7291-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7291-121">Adresse d’une variable qui reçoit la taille de la réponse de licence, en octets.</span><span class="sxs-lookup"><span data-stu-id="c7291-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7291-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7291-122">Return value</span></span>

<span data-ttu-id="c7291-123">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c7291-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c7291-124">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c7291-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c7291-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c7291-125">Return code</span></span>                                                                                                | <span data-ttu-id="c7291-126">Description</span><span class="sxs-lookup"><span data-stu-id="c7291-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c7291-127"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="c7291-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="c7291-128">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="c7291-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="c7291-129"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7291-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c7291-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7291-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="c7291-131">Notes</span><span class="sxs-lookup"><span data-stu-id="c7291-131">Remarks</span></span>

<span data-ttu-id="c7291-132">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c7291-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7291-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7291-133">Requirements</span></span>



| <span data-ttu-id="c7291-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7291-134">Requirement</span></span> | <span data-ttu-id="c7291-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7291-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7291-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7291-136">Header</span></span><br/> | <dl> <span data-ttu-id="c7291-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7291-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7291-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7291-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7291-139">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="c7291-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





