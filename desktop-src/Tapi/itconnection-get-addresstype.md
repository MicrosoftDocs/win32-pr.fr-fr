---
description: La \_ méthode obtenir AddressType obtient le type d’adresse.
ms.assetid: b2ff6303-6beb-429c-ad1a-2f729749e5db
title: 'ITConnection :: get_AddressType, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d015b0b395f0219fa9a7af2ca7002f242cfaa1b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526091"
---
# <a name="itconnectionget_addresstype-method"></a><span data-ttu-id="912c8-103">ITConnection :: obtient la \_ méthode AddressType</span><span class="sxs-lookup"><span data-stu-id="912c8-103">ITConnection::get\_AddressType method</span></span>

<span data-ttu-id="912c8-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="912c8-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="912c8-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="912c8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="912c8-106">La méthode **obtenir \_ AddressType** obtient le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="912c8-106">The **get\_AddressType** method gets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="912c8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="912c8-107">Syntax</span></span>


```C++
HRESULT get_AddressType(
  [out] BSTR *ppAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="912c8-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="912c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="912c8-109">*ppAddressType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="912c8-109">*ppAddressType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="912c8-110">Pointeur vers un **BSTR** contenant le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="912c8-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="912c8-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="912c8-111">Return value</span></span>

<span data-ttu-id="912c8-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="912c8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="912c8-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="912c8-113">Return code</span></span>                                                                                   | <span data-ttu-id="912c8-114">Description</span><span class="sxs-lookup"><span data-stu-id="912c8-114">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="912c8-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="912c8-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="912c8-116">Method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="912c8-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="912c8-118">Le paramètre *ppAddressType* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="912c8-118">The *ppAddressType* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="912c8-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="912c8-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="912c8-120">Insufficient memory exists to perform the operation.</span></span><br/>  |
| <dl> <span data-ttu-id="912c8-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="912c8-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="912c8-122">Unspecified error.</span></span><br/>                                    |
| <dl> <span data-ttu-id="912c8-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="912c8-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="912c8-124">This method is not yet implemented.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="912c8-125">Notes</span><span class="sxs-lookup"><span data-stu-id="912c8-125">Remarks</span></span>

<span data-ttu-id="912c8-126">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppAddressType* .</span><span class="sxs-lookup"><span data-stu-id="912c8-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppAddressType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="912c8-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="912c8-127">Requirements</span></span>



| <span data-ttu-id="912c8-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="912c8-128">Requirement</span></span> | <span data-ttu-id="912c8-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="912c8-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="912c8-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="912c8-130">TAPI version</span></span><br/> | <span data-ttu-id="912c8-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="912c8-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="912c8-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="912c8-132">Header</span></span><br/>       | <dl> <span data-ttu-id="912c8-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="912c8-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="912c8-134">Library</span></span><br/>      | <dl> <span data-ttu-id="912c8-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="912c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="912c8-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="912c8-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="912c8-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="912c8-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="912c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912c8-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="912c8-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="912c8-140">**ITConnection ::p ut \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="912c8-140">**ITConnection::put\_AddressType**</span></span>](itconnection-put-addresstype.md)
</dt> </dl>

 

