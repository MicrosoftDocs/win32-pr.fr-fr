---
description: La \_ méthode obtenir NumAddresses obtient le nombre d’adresses à utiliser pour la session.
ms.assetid: c3aef5df-02e9-4c7e-99aa-8e4043798bf4
title: 'ITConnection :: get_NumAddresses, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b121275c6af8f026e7321e4fd85327e970eb78
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537432"
---
# <a name="itconnectionget_numaddresses-method"></a><span data-ttu-id="d41c3-103">ITConnection :: \_ NumAddresses, méthode</span><span class="sxs-lookup"><span data-stu-id="d41c3-103">ITConnection::get\_NumAddresses method</span></span>

<span data-ttu-id="d41c3-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="d41c3-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="d41c3-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="d41c3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="d41c3-106">La méthode **obtenir \_ NumAddresses** obtient le nombre d’adresses à utiliser pour la session.</span><span class="sxs-lookup"><span data-stu-id="d41c3-106">The **get\_NumAddresses** method gets the number of addresses to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="d41c3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d41c3-107">Syntax</span></span>


```C++
HRESULT get_NumAddresses(
  [out] LONG *pNumAddresses
);
```



## <a name="parameters"></a><span data-ttu-id="d41c3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d41c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d41c3-109">*pNumAddresses* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d41c3-109">*pNumAddresses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d41c3-110">Nombre d’adresses pour la session.</span><span class="sxs-lookup"><span data-stu-id="d41c3-110">Number of addresses for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d41c3-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d41c3-111">Return value</span></span>

<span data-ttu-id="d41c3-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d41c3-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d41c3-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d41c3-113">Return code</span></span>                                                                                   | <span data-ttu-id="d41c3-114">Description</span><span class="sxs-lookup"><span data-stu-id="d41c3-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="d41c3-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d41c3-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="d41c3-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="d41c3-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d41c3-118">Le paramètre *pNumAddresse* s n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="d41c3-118">The *pNumAddresse* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="d41c3-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d41c3-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d41c3-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="d41c3-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="d41c3-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d41c3-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d41c3-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="d41c3-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="d41c3-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="d41c3-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d41c3-125">Requirements</span></span>



| <span data-ttu-id="d41c3-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d41c3-126">Requirement</span></span> | <span data-ttu-id="d41c3-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="d41c3-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d41c3-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="d41c3-128">TAPI version</span></span><br/> | <span data-ttu-id="d41c3-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="d41c3-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="d41c3-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="d41c3-130">Header</span></span><br/>       | <dl> <span data-ttu-id="d41c3-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="d41c3-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d41c3-132">Library</span></span><br/>      | <dl> <span data-ttu-id="d41c3-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d41c3-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d41c3-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="d41c3-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d41c3-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d41c3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d41c3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d41c3-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="d41c3-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




