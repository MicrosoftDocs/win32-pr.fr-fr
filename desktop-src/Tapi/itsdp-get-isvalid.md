---
description: La \_ méthode obtenir IsValid valide le protocole SDP (session descripteur) (SDP ; consultez le document RFC 2327) pour les valeurs de structure et de champ.
ms.assetid: a3f849ac-bda9-4937-bf3b-bce8df20cbf0
title: 'ITSdp :: get_IsValid, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88ca3cfdc1061e0a2830010ec39b2e6667c9341c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532277"
---
# <a name="itsdpget_isvalid-method"></a><span data-ttu-id="3224d-103">ITSdp :: obtient \_ IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="3224d-103">ITSdp::get\_IsValid method</span></span>

<span data-ttu-id="3224d-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="3224d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3224d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="3224d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="3224d-106">La méthode **obtenir \_ IsValid** valide le protocole SDP (session descripteur) (SDP ; consultez le document RFC 2327) pour les valeurs de structure et de champ.</span><span class="sxs-lookup"><span data-stu-id="3224d-106">The **get\_IsValid** method validates the Session Descriptor Protocol (SDP; see RFC 2327) blob for structure and field values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3224d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3224d-107">Syntax</span></span>


```C++
HRESULT get_IsValid(
  [out] VARIANT_BOOL *pfIsValid
);
```



## <a name="parameters"></a><span data-ttu-id="3224d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3224d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3224d-109">*pfIsValid* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3224d-109">*pfIsValid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3224d-110">Indique si la structure de l’objet blob est valide.</span><span class="sxs-lookup"><span data-stu-id="3224d-110">Indicates whether the blob structure is valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3224d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3224d-111">Return value</span></span>

<span data-ttu-id="3224d-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3224d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="3224d-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3224d-113">Return code</span></span>                                                                                   | <span data-ttu-id="3224d-114">Description</span><span class="sxs-lookup"><span data-stu-id="3224d-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="3224d-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3224d-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="3224d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3224d-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3224d-118">Le paramètre *pfIsValid* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3224d-118">The *pfIsValid* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="3224d-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3224d-120">Le paramètre *pfIsValid* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="3224d-120">The *pfIsValid* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="3224d-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3224d-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="3224d-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="3224d-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="3224d-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3224d-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="3224d-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="3224d-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="3224d-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="3224d-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3224d-127">Requirements</span></span>



| <span data-ttu-id="3224d-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3224d-128">Requirement</span></span> | <span data-ttu-id="3224d-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="3224d-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3224d-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="3224d-130">TAPI version</span></span><br/> | <span data-ttu-id="3224d-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="3224d-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="3224d-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="3224d-132">Header</span></span><br/>       | <dl> <span data-ttu-id="3224d-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="3224d-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3224d-134">Library</span></span><br/>      | <dl> <span data-ttu-id="3224d-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="3224d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3224d-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="3224d-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3224d-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3224d-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3224d-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3224d-139">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="3224d-139">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




