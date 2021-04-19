---
description: La méthode GetPhoneNumbers obtient un tableau de numéros de téléphone associés à un objet blob de conférence.
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'ITSdp :: GetPhoneNumbers, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525639"
---
# <a name="itsdpgetphonenumbers-method"></a><span data-ttu-id="ec6b9-103">ITSdp :: GetPhoneNumbers, méthode</span><span class="sxs-lookup"><span data-stu-id="ec6b9-103">ITSdp::GetPhoneNumbers method</span></span>

<span data-ttu-id="ec6b9-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ec6b9-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ec6b9-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ec6b9-106">La méthode **GetPhoneNumbers** obtient un tableau de numéros de téléphone associés à un objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-106">The **GetPhoneNumbers** method gets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec6b9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec6b9-107">Syntax</span></span>


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="ec6b9-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec6b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec6b9-109">*pNumbers* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec6b9-109">*pNumbers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec6b9-110">Pointeur de **type Variant** vers un SafeArray de **BSTR** qui répertorie les numéros de téléphone.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="ec6b9-111">*pNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ec6b9-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ec6b9-112">Pointeur de **type Variant** vers un SafeArray de noms de liste de **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec6b9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ec6b9-113">Return value</span></span>

<span data-ttu-id="ec6b9-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ec6b9-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ec6b9-115">Return code</span></span>                                                                                   | <span data-ttu-id="ec6b9-116">Description</span><span class="sxs-lookup"><span data-stu-id="ec6b9-116">Description</span></span>                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ec6b9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ec6b9-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-118">Method succeeded.</span></span><br/>                                            |
| <dl> <span data-ttu-id="ec6b9-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ec6b9-120">Le paramètre *pNumbers* ou *pNames* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-120">The *pNumbers* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="ec6b9-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ec6b9-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-122">Insufficient memory exists to perform the operation.</span></span><br/>         |
| <dl> <span data-ttu-id="ec6b9-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="ec6b9-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-124">Unspecified error.</span></span><br/>                                           |
| <dl> <span data-ttu-id="ec6b9-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="ec6b9-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-126">This method is not yet implemented.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="ec6b9-127">Notes</span><span class="sxs-lookup"><span data-stu-id="ec6b9-127">Remarks</span></span>

<span data-ttu-id="ec6b9-128">Les listes que *pNumbers* et *pNames* pointent sont de la même longueur.</span><span class="sxs-lookup"><span data-stu-id="ec6b9-128">The lists that *pNumbers* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec6b9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec6b9-129">Requirements</span></span>



| <span data-ttu-id="ec6b9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec6b9-130">Requirement</span></span> | <span data-ttu-id="ec6b9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec6b9-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ec6b9-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ec6b9-132">TAPI version</span></span><br/> | <span data-ttu-id="ec6b9-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ec6b9-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ec6b9-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec6b9-134">Header</span></span><br/>       | <dl> <span data-ttu-id="ec6b9-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec6b9-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ec6b9-136">Library</span></span><br/>      | <dl> <span data-ttu-id="ec6b9-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ec6b9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ec6b9-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="ec6b9-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec6b9-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec6b9-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec6b9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec6b9-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="ec6b9-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




