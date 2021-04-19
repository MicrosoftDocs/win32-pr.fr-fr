---
description: La méthode SetAddressInfo définit les informations d’adresse.
ms.assetid: 100b96af-e6ba-4496-9978-4df133e1c2b5
title: 'ITConnection :: SetAddressInfo, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae181911527c22639c8c2da3038c0377734fd1da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543597"
---
# <a name="itconnectionsetaddressinfo-method"></a><span data-ttu-id="85ce7-103">ITConnection :: SetAddressInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="85ce7-103">ITConnection::SetAddressInfo method</span></span>

<span data-ttu-id="85ce7-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="85ce7-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="85ce7-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="85ce7-106">La méthode **SetAddressInfo** définit les informations d’adresse.</span><span class="sxs-lookup"><span data-stu-id="85ce7-106">The **SetAddressInfo** method sets the address information.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ce7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85ce7-107">Syntax</span></span>


```C++
HRESULT SetAddressInfo(
  [in] BSTR          pStartAddress,
  [in] LONG          NumAddresses,
  [in] unsigned char Ttl
);
```



## <a name="parameters"></a><span data-ttu-id="85ce7-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85ce7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ce7-109">*pStartAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-109">*pStartAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-110">Pointeur vers un **BSTR** contenant l’adresse de début.</span><span class="sxs-lookup"><span data-stu-id="85ce7-110">Pointer to a **BSTR** containing the start address.</span></span>

</dd> <dt>

<span data-ttu-id="85ce7-111">*NumAddresses* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-111">*NumAddresses* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-112">Nombre d’adresses à utiliser pour la session.</span><span class="sxs-lookup"><span data-stu-id="85ce7-112">Number of addresses to be used for the session.</span></span>

</dd> <dt>

<span data-ttu-id="85ce7-113">*TTL* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="85ce7-113">*Ttl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ce7-114">étendue de la [*durée*](t-tapgloss.md) de vie (TTL) pour les transmissions sur les adresses.</span><span class="sxs-lookup"><span data-stu-id="85ce7-114">[*time to live*](t-tapgloss.md) (TTL) scope for transmissions on the addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ce7-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85ce7-115">Return value</span></span>

<span data-ttu-id="85ce7-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="85ce7-116">This method can return one of these values.</span></span>



| <span data-ttu-id="85ce7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="85ce7-117">Value</span></span>                                                                                         | <span data-ttu-id="85ce7-118">Signification</span><span class="sxs-lookup"><span data-stu-id="85ce7-118">Meaning</span></span>                                                                          |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85ce7-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="85ce7-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="85ce7-120">Method succeeded.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="85ce7-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="85ce7-122">Le paramètre *pStartAddress*, *NumAddresses* ou *TTL* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="85ce7-122">The *pStartAddress*, *NumAddresses*, or *Ttl* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="85ce7-123"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="85ce7-124">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="85ce7-124">Insufficient memory exists to perform the operation.</span></span><br/>                  |
| <dl> <span data-ttu-id="85ce7-125"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-125"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="85ce7-126">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="85ce7-126">Unspecified error.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="85ce7-127"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="85ce7-128">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="85ce7-128">This method is not yet implemented.</span></span><br/>                                   |



 

## <a name="remarks"></a><span data-ttu-id="85ce7-129">Notes</span><span class="sxs-lookup"><span data-stu-id="85ce7-129">Remarks</span></span>

<span data-ttu-id="85ce7-130">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PStartAddress* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="85ce7-130">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pStartAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ce7-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85ce7-131">Requirements</span></span>



| <span data-ttu-id="85ce7-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85ce7-132">Requirement</span></span> | <span data-ttu-id="85ce7-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="85ce7-133">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85ce7-134">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="85ce7-134">TAPI version</span></span><br/> | <span data-ttu-id="85ce7-135">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="85ce7-135">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="85ce7-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="85ce7-136">Header</span></span><br/>       | <dl> <span data-ttu-id="85ce7-137"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-137"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="85ce7-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85ce7-138">Library</span></span><br/>      | <dl> <span data-ttu-id="85ce7-139"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-139"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="85ce7-140">DLL</span><span class="sxs-lookup"><span data-stu-id="85ce7-140">DLL</span></span><br/>          | <dl> <span data-ttu-id="85ce7-141"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85ce7-141"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ce7-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85ce7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ce7-143">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="85ce7-143">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

