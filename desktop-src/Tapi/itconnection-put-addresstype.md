---
description: La \_ méthode put AddressType définit le type d’adresse.
ms.assetid: 73c64904-925c-4a35-a8f9-88b196b59b1e
title: ITConnection ::p ut_AddressType, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb9bc9b83a71f78a68b6efc2fa73c259c4afe9e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535926"
---
# <a name="itconnectionput_addresstype-method"></a><span data-ttu-id="dd664-103">ITConnection ::p UT, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="dd664-103">ITConnection::put\_AddressType method</span></span>

<span data-ttu-id="dd664-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="dd664-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="dd664-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="dd664-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="dd664-106">La méthode **put \_ AddressType** définit le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="dd664-106">The **put\_AddressType** method sets the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd664-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd664-107">Syntax</span></span>


```C++
HRESULT put_AddressType(
  [in] BSTR pAddressType
);
```



## <a name="parameters"></a><span data-ttu-id="dd664-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd664-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd664-109">*pAddressType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dd664-109">*pAddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd664-110">Pointeur vers un **BSTR** contenant le type d’adresse.</span><span class="sxs-lookup"><span data-stu-id="dd664-110">Pointer to a **BSTR** containing the address type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd664-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dd664-111">Return value</span></span>

<span data-ttu-id="dd664-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="dd664-112">This method can return one of these values.</span></span>



| <span data-ttu-id="dd664-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dd664-113">Return code</span></span>                                                                                   | <span data-ttu-id="dd664-114">Description</span><span class="sxs-lookup"><span data-stu-id="dd664-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="dd664-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="dd664-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="dd664-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="dd664-117"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-117"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="dd664-118">Le paramètre *pAddressType* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="dd664-118">The *pAddressType* parameter is not valid.</span></span><br/>           |
| <dl> <span data-ttu-id="dd664-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="dd664-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="dd664-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="dd664-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="dd664-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="dd664-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="dd664-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="dd664-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="dd664-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="dd664-125">Notes</span><span class="sxs-lookup"><span data-stu-id="dd664-125">Remarks</span></span>

<span data-ttu-id="dd664-126">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PAddressType* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="dd664-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pAddressType* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd664-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd664-127">Requirements</span></span>



| <span data-ttu-id="dd664-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd664-128">Requirement</span></span> | <span data-ttu-id="dd664-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd664-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dd664-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="dd664-130">TAPI version</span></span><br/> | <span data-ttu-id="dd664-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="dd664-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="dd664-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd664-132">Header</span></span><br/>       | <dl> <span data-ttu-id="dd664-133"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-133"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="dd664-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dd664-134">Library</span></span><br/>      | <dl> <span data-ttu-id="dd664-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="dd664-136">DLL</span><span class="sxs-lookup"><span data-stu-id="dd664-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="dd664-137"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd664-137"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd664-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd664-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd664-139">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="dd664-139">**ITConnection**</span></span>](itconnection.md)
</dt> <dt>

[<span data-ttu-id="dd664-140">**ITConnection :: obtient \_ AddressType**</span><span class="sxs-lookup"><span data-stu-id="dd664-140">**ITConnection::get\_AddressType**</span></span>](itconnection-get-addresstype.md)
</dt> </dl>

 

