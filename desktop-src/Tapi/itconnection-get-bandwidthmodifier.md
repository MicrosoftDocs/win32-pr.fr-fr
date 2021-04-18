---
description: La \_ méthode obtenir BandwidthModifier obtient le modificateur de bande passante, qui est un mot alphanumérique unique qui donne la signification de la largeur de la bande passante. Les deux modificateurs définis sont CT (total de la Conférence) et AS (maximum propre à l’application).
ms.assetid: 29bf137d-e88b-437f-8bf1-824e335d47a1
title: 'ITConnection :: get_BandwidthModifier, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e278edfbdc9ae56d89547c0bcf64f90fde77baf4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526032"
---
# <a name="itconnectionget_bandwidthmodifier-method"></a><span data-ttu-id="aae6f-104">ITConnection :: \_ BandwidthModifier, méthode</span><span class="sxs-lookup"><span data-stu-id="aae6f-104">ITConnection::get\_BandwidthModifier method</span></span>

<span data-ttu-id="aae6f-105">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="aae6f-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="aae6f-106">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="aae6f-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="aae6f-107">La méthode **obtenir \_ BandwidthModifier** obtient le modificateur de bande passante, qui est un mot alphanumérique unique qui donne la signification de la largeur de la bande passante.</span><span class="sxs-lookup"><span data-stu-id="aae6f-107">The **get\_BandwidthModifier** method gets the bandwidth modifier, which is a single, alphanumeric word giving the meaning of the bandwidth figure.</span></span> <span data-ttu-id="aae6f-108">Les deux modificateurs définis sont CT (total de la Conférence) et AS (maximum propre à l’application).</span><span class="sxs-lookup"><span data-stu-id="aae6f-108">The two modifiers defined are CT (Conference Total) and AS (Application Specific Maximum).</span></span>

## <a name="syntax"></a><span data-ttu-id="aae6f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aae6f-109">Syntax</span></span>


```C++
HRESULT get_BandwidthModifier(
  [out] BSTR *ppModifier
);
```



## <a name="parameters"></a><span data-ttu-id="aae6f-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aae6f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae6f-111">*ppModifier* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aae6f-111">*ppModifier* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae6f-112">Pointeur vers un **BSTR** contenant le modificateur de bande passante.</span><span class="sxs-lookup"><span data-stu-id="aae6f-112">Pointer to a **BSTR** containing the bandwidth modifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae6f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aae6f-113">Return value</span></span>

<span data-ttu-id="aae6f-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="aae6f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="aae6f-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aae6f-115">Return code</span></span>                                                                                   | <span data-ttu-id="aae6f-116">Description</span><span class="sxs-lookup"><span data-stu-id="aae6f-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="aae6f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aae6f-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="aae6f-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="aae6f-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aae6f-120">Le paramètre *ppModifier* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="aae6f-120">The *ppModifier* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="aae6f-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aae6f-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="aae6f-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="aae6f-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="aae6f-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="aae6f-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="aae6f-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="aae6f-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="aae6f-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="aae6f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="aae6f-127">Remarks</span></span>

<span data-ttu-id="aae6f-128">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppModifier* .</span><span class="sxs-lookup"><span data-stu-id="aae6f-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppModifier* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae6f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aae6f-129">Requirements</span></span>



| <span data-ttu-id="aae6f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aae6f-130">Requirement</span></span> | <span data-ttu-id="aae6f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="aae6f-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aae6f-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="aae6f-132">TAPI version</span></span><br/> | <span data-ttu-id="aae6f-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="aae6f-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="aae6f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="aae6f-134">Header</span></span><br/>       | <dl> <span data-ttu-id="aae6f-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="aae6f-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aae6f-136">Library</span></span><br/>      | <dl> <span data-ttu-id="aae6f-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="aae6f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aae6f-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="aae6f-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aae6f-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae6f-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aae6f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae6f-141">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="aae6f-141">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

