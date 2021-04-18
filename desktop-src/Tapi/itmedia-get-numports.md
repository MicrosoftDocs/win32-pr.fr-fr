---
description: La \_ méthode obtenir NumPorts obtient le nombre de ports nécessaires pour la session. La session utilise le nombre spécifié de ports à partir de la valeur retournée par \_ StartPort.
ms.assetid: 9ebdcf51-e095-4173-97d6-7754560abfb5
title: 'ITMedia :: get_NumPorts, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc223ddd5d210d2c1d440c52ca4201ccd6334b08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540093"
---
# <a name="itmediaget_numports-method"></a><span data-ttu-id="1b6e9-104">ITMedia :: \_ NumPorts, méthode</span><span class="sxs-lookup"><span data-stu-id="1b6e9-104">ITMedia::get\_NumPorts method</span></span>

<span data-ttu-id="1b6e9-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="1b6e9-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="1b6e9-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="1b6e9-107">La méthode **obtenir \_ NumPorts** obtient le nombre de ports nécessaires pour la session.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-107">The **get\_NumPorts** method gets the number of ports needed for the session.</span></span> <span data-ttu-id="1b6e9-108">La session utilise le nombre spécifié de ports à partir de la valeur retournée par [**\_ StartPort**](itmedia-get-startport.md).</span><span class="sxs-lookup"><span data-stu-id="1b6e9-108">The session uses the specified number of ports starting from the value returned by [**get\_StartPort**](itmedia-get-startport.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1b6e9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1b6e9-109">Syntax</span></span>


```C++
HRESULT get_NumPorts(
  [out] LONG *pNumPorts
);
```



## <a name="parameters"></a><span data-ttu-id="1b6e9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b6e9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b6e9-111">*pNumPorts* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1b6e9-111">*pNumPorts* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b6e9-112">Pointeur vers le nombre de ports.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-112">Pointer to the number of ports.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b6e9-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1b6e9-113">Return value</span></span>

<span data-ttu-id="1b6e9-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-114">This method can return one of these values.</span></span>



| <span data-ttu-id="1b6e9-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="1b6e9-115">Return code</span></span>                                                                                   | <span data-ttu-id="1b6e9-116">Description</span><span class="sxs-lookup"><span data-stu-id="1b6e9-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="1b6e9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="1b6e9-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="1b6e9-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="1b6e9-120">Le paramètre *pNumPorts* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-120">The *pNumPorts* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="1b6e9-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="1b6e9-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="1b6e9-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="1b6e9-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="1b6e9-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="1b6e9-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="1b6e9-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="1b6e9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b6e9-127">Requirements</span></span>



| <span data-ttu-id="1b6e9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1b6e9-128">Requirement</span></span> | <span data-ttu-id="1b6e9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="1b6e9-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1b6e9-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="1b6e9-130">TAPI version</span></span><br/> | <span data-ttu-id="1b6e9-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="1b6e9-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="1b6e9-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="1b6e9-132">Header</span></span><br/>       | <dl> <span data-ttu-id="1b6e9-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b6e9-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1b6e9-134">Library</span></span><br/>      | <dl> <span data-ttu-id="1b6e9-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="1b6e9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1b6e9-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="1b6e9-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b6e9-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b6e9-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b6e9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b6e9-139">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="1b6e9-139">**ITMedia**</span></span>](itmedia.md)
</dt> </dl>

 

 




