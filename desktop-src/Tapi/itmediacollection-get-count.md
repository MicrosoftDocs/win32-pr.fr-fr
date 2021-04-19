---
description: La \_ méthode obtenir le nombre obtient le nombre de médias dans la session.
ms.assetid: 9d085a34-9a49-4447-8d11-56d71a2a3592
title: 'ITMediaCollection :: get_Count, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1f5a4fb6d7f1b942f37aae1356c7b49e0e60f77
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539975"
---
# <a name="itmediacollectionget_count-method"></a><span data-ttu-id="8e680-103">ITMediaCollection :: obten, \_ méthode Count</span><span class="sxs-lookup"><span data-stu-id="8e680-103">ITMediaCollection::get\_Count method</span></span>

<span data-ttu-id="8e680-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="8e680-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="8e680-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="8e680-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="8e680-106">La méthode **obtenir le \_ nombre** obtient le nombre de médias dans la session.</span><span class="sxs-lookup"><span data-stu-id="8e680-106">The **get\_Count** method gets the number of media in the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e680-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8e680-107">Syntax</span></span>


```C++
HRESULT get_Count(
  [out] LONG *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="8e680-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8e680-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e680-109">*pval* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8e680-109">*pVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e680-110">Nombre de médias dans la session.</span><span class="sxs-lookup"><span data-stu-id="8e680-110">Count of media in the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e680-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8e680-111">Return value</span></span>

<span data-ttu-id="8e680-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="8e680-112">This method can return one of these values.</span></span>



| <span data-ttu-id="8e680-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="8e680-113">Return code</span></span>                                                                                   | <span data-ttu-id="8e680-114">Description</span><span class="sxs-lookup"><span data-stu-id="8e680-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="8e680-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="8e680-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="8e680-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8e680-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="8e680-118">Le paramètre *pval* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="8e680-118">The *pVal* parameter is not a valid pointer.</span></span><br/>         |
| <dl> <span data-ttu-id="8e680-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="8e680-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="8e680-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="8e680-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="8e680-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8e680-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8e680-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="8e680-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="8e680-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="8e680-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8e680-125">Requirements</span></span>



| <span data-ttu-id="8e680-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8e680-126">Requirement</span></span> | <span data-ttu-id="8e680-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="8e680-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8e680-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="8e680-128">TAPI version</span></span><br/> | <span data-ttu-id="8e680-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="8e680-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="8e680-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="8e680-130">Header</span></span><br/>       | <dl> <span data-ttu-id="8e680-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e680-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8e680-132">Library</span></span><br/>      | <dl> <span data-ttu-id="8e680-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="8e680-134">DLL</span><span class="sxs-lookup"><span data-stu-id="8e680-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="8e680-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e680-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e680-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8e680-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e680-137">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="8e680-137">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> </dl>

 

 




