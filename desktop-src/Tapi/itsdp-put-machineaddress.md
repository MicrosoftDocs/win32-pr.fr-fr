---
description: La \_ méthode put MachineAddress définit l’adresse de l’ordinateur hôte d’origine.
ms.assetid: f4af55b1-e20b-4fe8-a15e-a1a68d22f1b9
title: ITSdp ::p ut_MachineAddress, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec09d41cb7735383f08ce8c8983331165c54fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530008"
---
# <a name="itsdpput_machineaddress-method"></a><span data-ttu-id="2f09c-103">ITSdp ::p ut \_ MachineAddress, méthode</span><span class="sxs-lookup"><span data-stu-id="2f09c-103">ITSdp::put\_MachineAddress method</span></span>

<span data-ttu-id="2f09c-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2f09c-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2f09c-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2f09c-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2f09c-106">La méthode **put \_ MachineAddress** définit l’adresse de l’ordinateur hôte d’origine.</span><span class="sxs-lookup"><span data-stu-id="2f09c-106">The **put\_MachineAddress** method sets the machine address of the originating host.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f09c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2f09c-107">Syntax</span></span>


```C++
HRESULT put_MachineAddress(
  [in] BSTR pMachineAddress
);
```



## <a name="parameters"></a><span data-ttu-id="2f09c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f09c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f09c-109">*pMachineAddress* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2f09c-109">*pMachineAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f09c-110">Pointeur vers un **BSTR** contenant l’adresse de l’ordinateur hôte de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="2f09c-110">Pointer to a **BSTR** containing the machine address of the conference host.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f09c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f09c-111">Return value</span></span>

<span data-ttu-id="2f09c-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2f09c-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2f09c-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2f09c-113">Return code</span></span>                                                                                   | <span data-ttu-id="2f09c-114">Description</span><span class="sxs-lookup"><span data-stu-id="2f09c-114">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f09c-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2f09c-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2f09c-116">Method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="2f09c-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2f09c-118">Le paramètre *pMachineAddress* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="2f09c-118">The *pMachineAddress* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="2f09c-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2f09c-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2f09c-120">Insufficient memory exists to perform the operation.</span></span><br/>    |
| <dl> <span data-ttu-id="2f09c-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2f09c-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2f09c-122">Unspecified error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="2f09c-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2f09c-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="2f09c-124">This method is not yet implemented.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="2f09c-125">Notes</span><span class="sxs-lookup"><span data-stu-id="2f09c-125">Remarks</span></span>

<span data-ttu-id="2f09c-126">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PMachineAddress* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="2f09c-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pMachineAddress* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="2f09c-127">Le paramètre *pMachineAddress* peut être un nom DNS (« johnsmith.workinghard.Microsoft.com ») ou une adresse IP (« 10.111.222.111 »).</span><span class="sxs-lookup"><span data-stu-id="2f09c-127">The *pMachineAddress* parameter can be either a DNS name ("JohnSmith.workinghard.microsoft.com") or an IP address ("10.111.222.111").</span></span>

<span data-ttu-id="2f09c-128">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="2f09c-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="2f09c-129">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="2f09c-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f09c-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f09c-130">Requirements</span></span>



| <span data-ttu-id="2f09c-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f09c-131">Requirement</span></span> | <span data-ttu-id="2f09c-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f09c-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f09c-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2f09c-133">TAPI version</span></span><br/> | <span data-ttu-id="2f09c-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2f09c-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2f09c-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f09c-135">Header</span></span><br/>       | <dl> <span data-ttu-id="2f09c-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2f09c-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2f09c-137">Library</span></span><br/>      | <dl> <span data-ttu-id="2f09c-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2f09c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="2f09c-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="2f09c-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f09c-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f09c-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f09c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f09c-142">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="2f09c-142">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="2f09c-143">**ITSdp :: obtient \_ MachineAddress**</span><span class="sxs-lookup"><span data-stu-id="2f09c-143">**ITSdp::get\_MachineAddress**</span></span>](itsdp-get-machineaddress.md)
</dt> </dl>

 

