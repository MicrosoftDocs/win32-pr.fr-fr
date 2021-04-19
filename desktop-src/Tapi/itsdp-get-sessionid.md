---
description: La \_ méthode obtenir SessionID obtient la valeur du protocole NTP (Network Time Protocol) 32 bits qui sert d’identificateur de session. Elle est générée automatiquement lors de la création de la session.
ms.assetid: 5177f120-4b93-40bc-9481-aedf65a8dee9
title: 'ITSdp :: get_SessionId, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ad593b61f4c935a220e59383ae170569f04af54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525231"
---
# <a name="itsdpget_sessionid-method"></a><span data-ttu-id="a8054-104">ITSdp :: obtient \_ SessionID, méthode</span><span class="sxs-lookup"><span data-stu-id="a8054-104">ITSdp::get\_SessionId method</span></span>

<span data-ttu-id="a8054-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a8054-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a8054-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a8054-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a8054-107">La méthode **obtenir \_ SessionID** obtient la valeur du protocole NTP (Network Time Protocol) 32 bits qui sert d’identificateur de session.</span><span class="sxs-lookup"><span data-stu-id="a8054-107">The **get\_SessionId** method gets the 32-bit NTP (Network Time Protocol) value that serves as the session identifier.</span></span> <span data-ttu-id="a8054-108">Elle est générée automatiquement lors de la création de la session.</span><span class="sxs-lookup"><span data-stu-id="a8054-108">This is generated automatically when the session is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8054-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8054-109">Syntax</span></span>


```C++
HRESULT get_SessionId(
  [out] DOUBLE *pSessionId
);
```



## <a name="parameters"></a><span data-ttu-id="a8054-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8054-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8054-111">*pSessionId* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a8054-111">*pSessionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a8054-112">Pointeur vers l’identificateur de session.</span><span class="sxs-lookup"><span data-stu-id="a8054-112">Pointer to the session identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8054-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a8054-113">Return value</span></span>

<span data-ttu-id="a8054-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a8054-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a8054-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a8054-115">Return code</span></span>                                                                                   | <span data-ttu-id="a8054-116">Description</span><span class="sxs-lookup"><span data-stu-id="a8054-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a8054-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a8054-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a8054-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a8054-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="a8054-120">Le paramètre *pSessionId* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a8054-120">The *pSessionId* parameter is not valid.</span></span><br/>             |
| <dl> <span data-ttu-id="a8054-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a8054-122">Le paramètre *pSessionId* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a8054-122">The *pSessionId* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="a8054-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a8054-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a8054-124">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a8054-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="a8054-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a8054-126">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="a8054-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="a8054-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="a8054-128">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="a8054-129">Notes</span><span class="sxs-lookup"><span data-stu-id="a8054-129">Remarks</span></span>

<span data-ttu-id="a8054-130">La valeur de retour de cette méthode peut être **ULong**, mais Visual Basic ne prend pas en charge le type **ULong** .</span><span class="sxs-lookup"><span data-stu-id="a8054-130">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="a8054-131">Un **double** est le plus petit type suivant qui englobe la plage entière de valeurs requises.</span><span class="sxs-lookup"><span data-stu-id="a8054-131">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8054-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8054-132">Requirements</span></span>



| <span data-ttu-id="a8054-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8054-133">Requirement</span></span> | <span data-ttu-id="a8054-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8054-134">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a8054-135">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a8054-135">TAPI version</span></span><br/> | <span data-ttu-id="a8054-136">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a8054-136">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a8054-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8054-137">Header</span></span><br/>       | <dl> <span data-ttu-id="a8054-138"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-138"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8054-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a8054-139">Library</span></span><br/>      | <dl> <span data-ttu-id="a8054-140"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-140"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="a8054-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a8054-141">DLL</span></span><br/>          | <dl> <span data-ttu-id="a8054-142"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8054-142"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8054-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a8054-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8054-144">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="a8054-144">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




