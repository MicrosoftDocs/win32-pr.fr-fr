---
description: La \_ méthode obtenir MachineAddress obtient l’adresse de l’ordinateur hôte d’origine.
ms.assetid: 8a67cc9f-f9fc-4ec3-86f9-ffe34d075830
title: 'ITSdp :: get_MachineAddress, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34968efa16f04cba8f99dbc0dc42b0cf4995a43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526031"
---
# <a name="itsdpget_machineaddress-method"></a><span data-ttu-id="539ee-103">ITSdp :: \_ MachineAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="539ee-103">ITSdp::get\_MachineAddress method</span></span>

<span data-ttu-id="539ee-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="539ee-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="539ee-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="539ee-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="539ee-106">La méthode **obtenir \_ MachineAddress** obtient l’adresse de l’ordinateur hôte d’origine.</span><span class="sxs-lookup"><span data-stu-id="539ee-106">The **get\_MachineAddress** method gets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="539ee-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="539ee-107">Syntax</span></span>


```C++
HRESULT get_MachineAddress(
  [out] BSTR *ppMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="539ee-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="539ee-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="539ee-109">*ppMachineAddress* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="539ee-109">*ppMachineAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="539ee-110">Pointeur vers un **BSTR** contenant l’adresse de l’ordinateur hôte de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="539ee-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="539ee-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="539ee-111">Return value</span></span>

<span data-ttu-id="539ee-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="539ee-112">This method can return one of these values.</span></span>



| <span data-ttu-id="539ee-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="539ee-113">Return code</span></span>                                                                                   | <span data-ttu-id="539ee-114">Description</span><span class="sxs-lookup"><span data-stu-id="539ee-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="539ee-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="539ee-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="539ee-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="539ee-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="539ee-118">Le paramètre *ppMachineAddres* s n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="539ee-118">The *ppMachineAddres* s parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="539ee-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="539ee-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="539ee-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="539ee-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="539ee-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="539ee-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="539ee-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="539ee-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="539ee-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="539ee-125">Notes</span><span class="sxs-lookup"><span data-stu-id="539ee-125">Remarks</span></span>

<span data-ttu-id="539ee-126">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppMachineAddress* .</span><span class="sxs-lookup"><span data-stu-id="539ee-126">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppMachineAddress* parameter.</span></span>

<span data-ttu-id="539ee-127">Le paramètre *ppMachineAddress* peut être retourné sous la forme d’un nom DNS (« johnsmith.workinghard.Microsoft.com ») ou d’une adresse IP (« 10.111.222.111 »).</span><span class="sxs-lookup"><span data-stu-id="539ee-127">The *ppMachineAddress* parameter can be returned as either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

## <a name="requirements"></a><span data-ttu-id="539ee-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="539ee-128">Requirements</span></span>



| <span data-ttu-id="539ee-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="539ee-129">Requirement</span></span> | <span data-ttu-id="539ee-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="539ee-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="539ee-131">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="539ee-131">TAPI version</span></span><br/> | <span data-ttu-id="539ee-132">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="539ee-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="539ee-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="539ee-133">Header</span></span><br/>       | <dl> <span data-ttu-id="539ee-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="539ee-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="539ee-135">Library</span></span><br/>      | <dl> <span data-ttu-id="539ee-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="539ee-137">DLL</span><span class="sxs-lookup"><span data-stu-id="539ee-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="539ee-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="539ee-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="539ee-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="539ee-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="539ee-140">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="539ee-140">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="539ee-141">**ITSdp ::p ut \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="539ee-141">**ITSdp::put\_MachineAddress**</span></span>](itsdp-put-machineaddress.md)
</dt> </dl>

 

