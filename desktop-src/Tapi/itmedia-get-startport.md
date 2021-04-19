---
description: La \_ méthode obtenir StartPort obtient la valeur de port 16 bits pour le premier port.
ms.assetid: 203b51ea-8e0c-47d2-b267-36a0bf3bff72
title: 'ITMedia :: get_StartPort, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c5cf50f4a8beb0a1694bd1ceaf000620c69b69
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539518"
---
# <a name="itmediaget_startport-method"></a><span data-ttu-id="c0893-103">ITMedia :: \_ StartPort, méthode</span><span class="sxs-lookup"><span data-stu-id="c0893-103">ITMedia::get\_StartPort method</span></span>

<span data-ttu-id="c0893-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="c0893-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c0893-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="c0893-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="c0893-106">La méthode **obtenir \_ StartPort** obtient la valeur de port 16 bits pour le premier port.</span><span class="sxs-lookup"><span data-stu-id="c0893-106">The **get\_StartPort** method gets the 16-bit port value for the first port.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0893-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0893-107">Syntax</span></span>


```C++
HRESULT get_StartPort(
  [out] LONG *pStartPort
);
```



## <a name="parameters"></a><span data-ttu-id="c0893-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0893-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0893-109">*pStartPort* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c0893-109">*pStartPort* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c0893-110">Valeur du premier port.</span><span class="sxs-lookup"><span data-stu-id="c0893-110">Value of the first port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0893-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0893-111">Return value</span></span>

<span data-ttu-id="c0893-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="c0893-112">This method can return one of these values.</span></span>



| <span data-ttu-id="c0893-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c0893-113">Return code</span></span>                                                                                   | <span data-ttu-id="c0893-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0893-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="c0893-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c0893-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="c0893-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c0893-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c0893-118">Le paramètre *pStartPort* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="c0893-118">The *pStartPort* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="c0893-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c0893-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="c0893-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="c0893-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="c0893-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c0893-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c0893-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="c0893-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="c0893-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="c0893-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0893-125">Requirements</span></span>



| <span data-ttu-id="c0893-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0893-126">Requirement</span></span> | <span data-ttu-id="c0893-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0893-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c0893-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="c0893-128">TAPI version</span></span><br/> | <span data-ttu-id="c0893-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="c0893-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="c0893-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0893-130">Header</span></span><br/>       | <dl> <span data-ttu-id="c0893-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0893-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0893-132">Library</span></span><br/>      | <dl> <span data-ttu-id="c0893-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="c0893-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c0893-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="c0893-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0893-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0893-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0893-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0893-137">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="c0893-137">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




