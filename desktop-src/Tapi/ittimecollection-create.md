---
description: La méthode Create crée un composant ITTime.
ms.assetid: dee50454-8358-4898-b098-2de51505b658
title: 'ITTimeCollection :: Create, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df62bbc8f1ad2a24a9b80a7f5d0a25bc01f713d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525428"
---
# <a name="ittimecollectioncreate-method"></a><span data-ttu-id="2c55e-103">ITTimeCollection :: Create, méthode</span><span class="sxs-lookup"><span data-stu-id="2c55e-103">ITTimeCollection::Create method</span></span>

<span data-ttu-id="2c55e-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2c55e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2c55e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2c55e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2c55e-106">La méthode **Create** crée un composant [**ITTime**](ittime.md) .</span><span class="sxs-lookup"><span data-stu-id="2c55e-106">The **Create** method creates a new [**ITTime**](ittime.md) component.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c55e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2c55e-107">Syntax</span></span>


```C++
HRESULT Create(
  [in]  LONG   Index,
  [out] ITTime **ppTime
);
```



## <a name="parameters"></a><span data-ttu-id="2c55e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2c55e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c55e-109">*Index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2c55e-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c55e-110">Index de l’élément à créer.</span><span class="sxs-lookup"><span data-stu-id="2c55e-110">Index of the item to create.</span></span> <span data-ttu-id="2c55e-111">(Le tableau d’index est de base un.)</span><span class="sxs-lookup"><span data-stu-id="2c55e-111">(The index array is one-based.)</span></span>

</dd> <dt>

<span data-ttu-id="2c55e-112">*ppTime* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2c55e-112">*ppTime* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c55e-113">Pointeur vers le composant b créé.</span><span class="sxs-lookup"><span data-stu-id="2c55e-113">Pointer to the b component created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c55e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2c55e-114">Return value</span></span>

<span data-ttu-id="2c55e-115">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2c55e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="2c55e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c55e-116">Value</span></span>                                                                                         | <span data-ttu-id="2c55e-117">Signification</span><span class="sxs-lookup"><span data-stu-id="2c55e-117">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2c55e-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-118"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2c55e-119">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2c55e-119">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2c55e-120"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2c55e-121">Le paramètre *ppTime* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="2c55e-121">The *ppTime* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="2c55e-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="2c55e-123">Le paramètre d' *index* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="2c55e-123">The *Index* parameter is not valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="2c55e-124"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2c55e-125">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2c55e-125">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2c55e-126"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-126"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2c55e-127">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2c55e-127">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2c55e-128"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-128"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2c55e-129">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="2c55e-129">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2c55e-130">Notes</span><span class="sxs-lookup"><span data-stu-id="2c55e-130">Remarks</span></span>

<span data-ttu-id="2c55e-131">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITTime**](ittime.md) retournée par **ITTimeCollection :: Create**.</span><span class="sxs-lookup"><span data-stu-id="2c55e-131">TAPI calls the **AddRef** method on the [**ITTime**](ittime.md) interface returned by **ITTimeCollection::Create**.</span></span> <span data-ttu-id="2c55e-132">L’application doit appeler **Release** sur l’interface v pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="2c55e-132">The application must call **Release** on the v interface to free resources associated with it.</span></span>

<span data-ttu-id="2c55e-133">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="2c55e-133">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="2c55e-134">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2c55e-134">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c55e-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2c55e-135">Requirements</span></span>



| <span data-ttu-id="2c55e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2c55e-136">Requirement</span></span> | <span data-ttu-id="2c55e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="2c55e-137">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2c55e-138">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2c55e-138">TAPI version</span></span><br/> | <span data-ttu-id="2c55e-139">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2c55e-139">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2c55e-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="2c55e-140">Header</span></span><br/>       | <dl> <span data-ttu-id="2c55e-141"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-141"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c55e-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2c55e-142">Library</span></span><br/>      | <dl> <span data-ttu-id="2c55e-143"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-143"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2c55e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2c55e-144">DLL</span></span><br/>          | <dl> <span data-ttu-id="2c55e-145"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c55e-145"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c55e-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2c55e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c55e-147">**ITTimeCollection**</span><span class="sxs-lookup"><span data-stu-id="2c55e-147">**ITTimeCollection**</span></span>](ittimecollection.md)
</dt> <dt>

[<span data-ttu-id="2c55e-148">**ITTime**</span><span class="sxs-lookup"><span data-stu-id="2c55e-148">**ITTime**</span></span>](ittime.md)
</dt> </dl>

 

 




