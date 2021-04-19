---
description: La \_ méthode obtenir SessionVersion obtient 32 la valeur de protocole NTP (Network Time Protocol, ou NTP) qui sert de version de session.
ms.assetid: 39c2aef4-24e3-4ea0-8b23-dff842f9ab84
title: 'ITSdp :: get_SessionVersion, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3466844f3f21f54ec0ec76a3569e7af25e4b0143
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541556"
---
# <a name="itsdpget_sessionversion-method"></a><span data-ttu-id="7e056-103">ITSdp :: \_ SessionVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="7e056-103">ITSdp::get\_SessionVersion method</span></span>

<span data-ttu-id="7e056-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7e056-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7e056-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7e056-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7e056-106">La méthode **obtenir \_ SessionVersion** obtient 32 la valeur de protocole NTP (Network Time Protocol, ou NTP) qui sert de version de session.</span><span class="sxs-lookup"><span data-stu-id="7e056-106">The **get\_SessionVersion** method gets the 32-bit (ideally Network Time Protocol, or NTP) value that serves as the session version.</span></span> <span data-ttu-id="7e056-107">Bien qu’elle soit générée automatiquement lors de la création de la session, l’utilisateur est responsable de sa modification lors de la modification du SDP.</span><span class="sxs-lookup"><span data-stu-id="7e056-107">Although this is generated automatically when the session is created, the user is responsible for changing it when the SDP is modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e056-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e056-108">Syntax</span></span>


```C++
HRESULT get_SessionVersion(
  [out] DOUBLE *pSessionVersion
);
```



## <a name="parameters"></a><span data-ttu-id="7e056-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7e056-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e056-110">*pSessionVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7e056-110">*pSessionVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7e056-111">Pointeur vers l’identificateur de version de session.</span><span class="sxs-lookup"><span data-stu-id="7e056-111">Pointer to the session version identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e056-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7e056-112">Return value</span></span>

<span data-ttu-id="7e056-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7e056-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7e056-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7e056-114">Return code</span></span>                                                                                   | <span data-ttu-id="7e056-115">Description</span><span class="sxs-lookup"><span data-stu-id="7e056-115">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7e056-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7e056-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7e056-117">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="7e056-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="7e056-119">Le paramètre *pSessionVersion* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7e056-119">The *pSessionVersion* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="7e056-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7e056-121">Le paramètre *pSessionVersion* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="7e056-121">The *pSessionVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="7e056-122"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7e056-123">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7e056-123">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="7e056-124"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-124"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7e056-125">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7e056-125">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="7e056-126"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-126"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7e056-127">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="7e056-127">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="7e056-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7e056-128">Remarks</span></span>

<span data-ttu-id="7e056-129">La valeur de retour de cette méthode peut être **ULong**, mais Visual Basic ne prend pas en charge le type **ULong** .</span><span class="sxs-lookup"><span data-stu-id="7e056-129">The return value of this method could be **ULONG**, but Visual Basic doesn't support the **ULONG** type.</span></span> <span data-ttu-id="7e056-130">Un **double** est le plus petit type suivant qui englobe la plage entière de valeurs requises.</span><span class="sxs-lookup"><span data-stu-id="7e056-130">A **DOUBLE** is the next smallest type that encompasses the entire range of values required.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e056-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e056-131">Requirements</span></span>



| <span data-ttu-id="7e056-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e056-132">Requirement</span></span> | <span data-ttu-id="7e056-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e056-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e056-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7e056-134">TAPI version</span></span><br/> | <span data-ttu-id="7e056-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7e056-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7e056-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e056-136">Header</span></span><br/>       | <dl> <span data-ttu-id="7e056-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e056-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7e056-138">Library</span></span><br/>      | <dl> <span data-ttu-id="7e056-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7e056-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7e056-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="7e056-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e056-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e056-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e056-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e056-143">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="7e056-143">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="7e056-144">**ITSdp ::p ut \_ SessionVersion**</span><span class="sxs-lookup"><span data-stu-id="7e056-144">**ITSdp::put\_SessionVersion**</span></span>](itsdp-put-sessionversion.md)
</dt> </dl>

 

 




