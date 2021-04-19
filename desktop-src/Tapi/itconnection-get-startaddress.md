---
description: La \_ méthode obtenir STARTADDRESS obtient la première adresse à utiliser pour la session.
ms.assetid: 3c4fec19-1b7d-4052-afd8-7aaf095907d0
title: 'ITConnection :: get_StartAddress, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84266d1874e7d04acb594bcfb9d99b440b0390b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525195"
---
# <a name="itconnectionget_startaddress-method"></a><span data-ttu-id="0ba8e-103">ITConnection :: obten, \_ méthode STARTADDRESS</span><span class="sxs-lookup"><span data-stu-id="0ba8e-103">ITConnection::get\_StartAddress method</span></span>

<span data-ttu-id="0ba8e-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="0ba8e-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="0ba8e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="0ba8e-106">La méthode **obtenir \_ STARTADDRESS** obtient la première adresse à utiliser pour la session.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-106">The **get\_StartAddress** method gets the first address to be used for the session.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ba8e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ba8e-107">Syntax</span></span>


```C++
HRESULT get_StartAddress(
  [out] BSTR *ppStartAddress
);
```



## <a name="parameters"></a><span data-ttu-id="0ba8e-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ba8e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ba8e-109">*ppStartAddress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ba8e-109">*ppStartAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ba8e-110">Pointeur vers un **BSTR** contenant l’adresse de début de la session.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-110">Pointer to a **BSTR** containing the starting address for the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ba8e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ba8e-111">Return value</span></span>

<span data-ttu-id="0ba8e-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-112">This method can return one of these values.</span></span>



| <span data-ttu-id="0ba8e-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0ba8e-113">Return code</span></span>                                                                                   | <span data-ttu-id="0ba8e-114">Description</span><span class="sxs-lookup"><span data-stu-id="0ba8e-114">Description</span></span>                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="0ba8e-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="0ba8e-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-116">Method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="0ba8e-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="0ba8e-118">Le paramètre *ppStartAddress* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-118">The *ppStartAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="0ba8e-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="0ba8e-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-120">Insufficient memory exists to perform the operation.</span></span><br/>   |
| <dl> <span data-ttu-id="0ba8e-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="0ba8e-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-122">Unspecified error.</span></span><br/>                                     |
| <dl> <span data-ttu-id="0ba8e-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="0ba8e-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="0ba8e-124">This method is not yet implemented.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="0ba8e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="0ba8e-125">Remarks</span></span>

<span data-ttu-id="0ba8e-126">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppStartAddress* .</span><span class="sxs-lookup"><span data-stu-id="0ba8e-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppStartAddress* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ba8e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ba8e-127">Requirements</span></span>



| <span data-ttu-id="0ba8e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ba8e-128">Requirement</span></span> | <span data-ttu-id="0ba8e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ba8e-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ba8e-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="0ba8e-130">TAPI version</span></span><br/> | <span data-ttu-id="0ba8e-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="0ba8e-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="0ba8e-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ba8e-132">Header</span></span><br/>       | <dl> <span data-ttu-id="0ba8e-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="0ba8e-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="0ba8e-134">Library</span></span><br/>      | <dl> <span data-ttu-id="0ba8e-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="0ba8e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0ba8e-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="0ba8e-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ba8e-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ba8e-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ba8e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ba8e-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="0ba8e-139">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

