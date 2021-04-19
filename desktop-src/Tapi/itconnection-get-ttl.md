---
description: La \_ méthode obtenir TTL obtient l’étendue de la durée de vie (TTL) pour les transmissions sur les adresses.
ms.assetid: ea3c22d8-476e-4b4b-98c6-f1075e704f3d
title: 'ITConnection :: get_Ttl, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88f4810eeefc19647e6ed5601b3a6b88870f1e9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533003"
---
# <a name="itconnectionget_ttl-method"></a><span data-ttu-id="02db2-103">ITConnection :: obtient la \_ méthode TTL</span><span class="sxs-lookup"><span data-stu-id="02db2-103">ITConnection::get\_Ttl method</span></span>

<span data-ttu-id="02db2-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="02db2-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="02db2-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="02db2-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="02db2-106">La méthode **obtenir \_ TTL** obtient l’étendue de la [*durée de*](t-tapgloss.md) vie (TTL) pour les transmissions sur les adresses.</span><span class="sxs-lookup"><span data-stu-id="02db2-106">The **get\_Ttl** method gets the [*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="02db2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02db2-107">Syntax</span></span>


```C++
HRESULT get_Ttl(
  [out] unsigned char *pTtl
);
```



## <a name="parameters"></a><span data-ttu-id="02db2-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02db2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02db2-109">*pTtl* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02db2-109">*pTtl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02db2-110">Étendue de la durée de vie.</span><span class="sxs-lookup"><span data-stu-id="02db2-110">TTL scope.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02db2-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02db2-111">Return value</span></span>

<span data-ttu-id="02db2-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="02db2-112">This method can return one of these values.</span></span>



| <span data-ttu-id="02db2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-113">Value</span></span>                                                                                         | <span data-ttu-id="02db2-114">Signification</span><span class="sxs-lookup"><span data-stu-id="02db2-114">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="02db2-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="02db2-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="02db2-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="02db2-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="02db2-118">Le paramètre *pTtl* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="02db2-118">The *pTtl* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="02db2-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="02db2-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="02db2-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="02db2-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="02db2-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="02db2-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="02db2-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="02db2-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="02db2-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="02db2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02db2-125">Requirements</span></span>



| <span data-ttu-id="02db2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02db2-126">Requirement</span></span> | <span data-ttu-id="02db2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="02db2-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02db2-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="02db2-128">TAPI version</span></span><br/> | <span data-ttu-id="02db2-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="02db2-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="02db2-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="02db2-130">Header</span></span><br/>       | <dl> <span data-ttu-id="02db2-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="02db2-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="02db2-132">Library</span></span><br/>      | <dl> <span data-ttu-id="02db2-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="02db2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="02db2-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="02db2-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02db2-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02db2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02db2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02db2-137">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="02db2-137">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 




