---
title: Méthode IWMDRMNetTransmitter GetRootLicenseResponse (wmdrmsdk. h)
description: La méthode GetRootLicenseResponse génère un message de réponse de licence racine.
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- Méthode GetRootLicenseResponse format Windows Media
- Méthode GetRootLicenseResponse format Windows Media, interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter Windows Media format, méthode GetRootLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542549"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="7bfbf-106">IWMDRMNetTransmitter :: GetRootLicenseResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="7bfbf-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="7bfbf-107">La méthode **GetRootLicenseResponse** génère un message de réponse de licence racine.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bfbf-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bfbf-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="7bfbf-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bfbf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bfbf-110">*bstrKID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bfbf-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bfbf-111">Identificateur de clé encodé en base64 à utiliser pour la nouvelle licence racine.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="7bfbf-112">L’identificateur de clé doit être une valeur GUID générée de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="7bfbf-113">*ppbLicenseResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7bfbf-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bfbf-114">Adresse d’une variable qui reçoit l’adresse de la réponse de licence générée.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="7bfbf-115">Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="7bfbf-116">*pcbLicenseResponse* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7bfbf-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bfbf-117">Adresse d’une variable qui reçoit la taille de la réponse de licence, en octets.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bfbf-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7bfbf-118">Return value</span></span>

<span data-ttu-id="7bfbf-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7bfbf-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7bfbf-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7bfbf-121">Return code</span></span>                                                                                                | <span data-ttu-id="7bfbf-122">Description</span><span class="sxs-lookup"><span data-stu-id="7bfbf-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="7bfbf-123"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="7bfbf-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="7bfbf-124">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="7bfbf-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7bfbf-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="7bfbf-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="7bfbf-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="7bfbf-127">Notes</span><span class="sxs-lookup"><span data-stu-id="7bfbf-127">Remarks</span></span>

<span data-ttu-id="7bfbf-128">La licence racine générée est créée à l’aide des informations des données de demande de licence, qui sont traitées pour l’interface en appelant [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span><span class="sxs-lookup"><span data-stu-id="7bfbf-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="7bfbf-129">La licence racine est utilisée dans la génération de licences feuille, ce qui est accompli en appelant la méthode [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="7bfbf-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="7bfbf-130">L’interface **IWMDRMNetTransmitter** conserve une copie de la licence racine pour cette utilisation.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="7bfbf-131">La licence racine créée par l’appel de cette méthode n’a aucune stratégie et est configurée de sorte qu’elle ne puisse pas être rendue persistante sur l’appareil de réception.</span><span class="sxs-lookup"><span data-stu-id="7bfbf-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bfbf-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bfbf-132">Requirements</span></span>



| <span data-ttu-id="7bfbf-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bfbf-133">Requirement</span></span> | <span data-ttu-id="7bfbf-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bfbf-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bfbf-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bfbf-135">Header</span></span><br/> | <dl> <span data-ttu-id="7bfbf-136"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bfbf-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bfbf-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7bfbf-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bfbf-138">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="7bfbf-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





