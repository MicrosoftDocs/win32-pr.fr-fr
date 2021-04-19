---
description: La méthode SetPhoneNumbers définit un tableau de numéros de téléphone associés à un objet blob de conférence.
ms.assetid: 674c08df-7e91-4f19-9d65-4bc6e7af117b
title: 'ITSdp :: SetPhoneNumbers, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec2820d8d033ac2eed9d9287c3ca52c9deb316
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524061"
---
# <a name="itsdpsetphonenumbers-method"></a><span data-ttu-id="f03df-103">ITSdp :: SetPhoneNumbers, méthode</span><span class="sxs-lookup"><span data-stu-id="f03df-103">ITSdp::SetPhoneNumbers method</span></span>

<span data-ttu-id="f03df-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f03df-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f03df-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f03df-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f03df-106">La méthode **SetPhoneNumbers** définit un tableau de numéros de téléphone associés à un objet blob de conférence.</span><span class="sxs-lookup"><span data-stu-id="f03df-106">The **SetPhoneNumbers** method sets an array of phone numbers associated with a conference blob.</span></span>

## <a name="syntax"></a><span data-ttu-id="f03df-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f03df-107">Syntax</span></span>


```C++
HRESULT SetPhoneNumbers(
  [in] VARIANT Numbers,
  [in] VARIANT Names
);
```



## <a name="parameters"></a><span data-ttu-id="f03df-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f03df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f03df-109">*Nombres* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f03df-109">*Numbers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03df-110">SAFEARRAY de **BSTR** répertoriant les numéros de téléphone.</span><span class="sxs-lookup"><span data-stu-id="f03df-110">SAFEARRAY of **BSTR** s listing phone numbers.</span></span>

</dd> <dt>

<span data-ttu-id="f03df-111">*Noms* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f03df-111">*Names* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f03df-112">SAFEARRAY de noms de liste de **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="f03df-112">SAFEARRAY of **BSTR** s listing names.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f03df-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f03df-113">Return value</span></span>

<span data-ttu-id="f03df-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f03df-114">This method can return one of these values.</span></span>



| <span data-ttu-id="f03df-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f03df-115">Return code</span></span>                                                                                   | <span data-ttu-id="f03df-116">Description</span><span class="sxs-lookup"><span data-stu-id="f03df-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f03df-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f03df-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f03df-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f03df-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="f03df-120">Le paramètre *numbers* ou *Names* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f03df-120">The *Numbers* or *Names* parameter is not valid.</span></span><br/>     |
| <dl> <span data-ttu-id="f03df-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f03df-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f03df-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="f03df-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="f03df-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f03df-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="f03df-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="f03df-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="f03df-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="f03df-127">Notes</span><span class="sxs-lookup"><span data-stu-id="f03df-127">Remarks</span></span>

<span data-ttu-id="f03df-128">Les listes dont les *nombres* et les *noms* pointent sont de la même longueur.</span><span class="sxs-lookup"><span data-stu-id="f03df-128">The lists that *Numbers* and *Names* point to are the same length.</span></span>

## <a name="requirements"></a><span data-ttu-id="f03df-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f03df-129">Requirements</span></span>



| <span data-ttu-id="f03df-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f03df-130">Requirement</span></span> | <span data-ttu-id="f03df-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="f03df-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f03df-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f03df-132">TAPI version</span></span><br/> | <span data-ttu-id="f03df-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="f03df-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="f03df-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f03df-134">Header</span></span><br/>       | <dl> <span data-ttu-id="f03df-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="f03df-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f03df-136">Library</span></span><br/>      | <dl> <span data-ttu-id="f03df-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="f03df-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f03df-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="f03df-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f03df-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f03df-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f03df-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f03df-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="f03df-141">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




