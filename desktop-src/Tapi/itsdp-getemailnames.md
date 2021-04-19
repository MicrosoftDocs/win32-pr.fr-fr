---
description: La méthode GetEmailNames obtient un tableau de noms de messagerie associés à l’objet blob de conférence.
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'ITSdp :: GetEmailNames, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f0200b5cc6ea0422f47a323cd1c57d7e0f9a5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530388"
---
# <a name="itsdpgetemailnames-method"></a><span data-ttu-id="8db82-103">ITSdp :: GetEmailNames, méthode</span><span class="sxs-lookup"><span data-stu-id="8db82-103">ITSdp::GetEmailNames method</span></span>

<span data-ttu-id="8db82-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8db82-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8db82-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8db82-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8db82-106">La méthode **GetEmailNames** obtient un tableau de noms de messagerie associés à l’objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="8db82-106">The **GetEmailNames** method gets an array of e-mail names associated with the conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="8db82-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8db82-107">Syntax</span></span>


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a><span data-ttu-id="8db82-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8db82-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8db82-109">*pAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8db82-109">*pAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db82-110">Pointeur **Variant** vers un SafeArray de **BSTR** répertoriant les adresses de messagerie.</span><span class="sxs-lookup"><span data-stu-id="8db82-110">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing e-mail addresses.</span></span>

</dd> <dt>

<span data-ttu-id="8db82-111">*pNames* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8db82-111">*pNames* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8db82-112">Pointeur de **type Variant** vers un SafeArray de noms de liste de **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="8db82-112">**VARIANT** pointer to a SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8db82-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8db82-113">Return value</span></span>

<span data-ttu-id="8db82-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8db82-114">This method can return one of these values.</span></span>



| <span data-ttu-id="8db82-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8db82-115">Return code</span></span>                                                                                   | <span data-ttu-id="8db82-116">Description</span><span class="sxs-lookup"><span data-stu-id="8db82-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8db82-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8db82-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8db82-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="8db82-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8db82-120">Le paramètre *pAddresses* ou *pNames* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="8db82-120">The *pAddresses* or *pNames* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="8db82-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8db82-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8db82-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="8db82-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8db82-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8db82-124">Unspecified error.</span></span><br/>                                             |
| <dl> <span data-ttu-id="8db82-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8db82-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="8db82-126">This method is not yet implemented.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="8db82-127">Notes</span><span class="sxs-lookup"><span data-stu-id="8db82-127">Remarks</span></span>

<span data-ttu-id="8db82-128">Les listes que *pAddresses* et *pNames* pointent sont de la même longueur.</span><span class="sxs-lookup"><span data-stu-id="8db82-128">The lists that *pAddresses* and *pNames* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="8db82-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8db82-129">Requirements</span></span>



| <span data-ttu-id="8db82-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8db82-130">Requirement</span></span> | <span data-ttu-id="8db82-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8db82-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8db82-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8db82-132">TAPI version</span></span><br/> | <span data-ttu-id="8db82-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8db82-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8db82-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="8db82-134">Header</span></span><br/>       | <dl> <span data-ttu-id="8db82-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8db82-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8db82-136">Library</span></span><br/>      | <dl> <span data-ttu-id="8db82-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8db82-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8db82-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="8db82-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8db82-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8db82-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8db82-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8db82-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="8db82-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




