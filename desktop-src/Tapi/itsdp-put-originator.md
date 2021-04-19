---
description: La \_ méthode put Origin définit l’expéditeur de la Conférence.
ms.assetid: b70fc584-3536-4296-bc38-e20ff6630abc
title: ITSdp ::p ut_Originator, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 506554668e697e9281dc5dc15784fa36f7429d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540960"
---
# <a name="itsdpput_originator-method"></a><span data-ttu-id="df66d-103">ITSdp ::p la \_ méthode Originator</span><span class="sxs-lookup"><span data-stu-id="df66d-103">ITSdp::put\_Originator method</span></span>

<span data-ttu-id="df66d-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="df66d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="df66d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="df66d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="df66d-106">La méthode **put \_ origin** définit l’expéditeur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="df66d-106">The **put\_Originator** method sets the conference originator.</span></span>

## <a name="syntax"></a><span data-ttu-id="df66d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df66d-107">Syntax</span></span>


```C++
HRESULT put_Originator(
  [in] BSTR pOriginator
);
```



## <a name="parameters"></a><span data-ttu-id="df66d-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df66d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df66d-109">*pOriginator* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="df66d-109">*pOriginator* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="df66d-110">Pointeur vers une représentation **BSTR** de l’expéditeur de la Conférence.</span><span class="sxs-lookup"><span data-stu-id="df66d-110">Pointer to a **BSTR** representation of the conference originator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df66d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="df66d-111">Return value</span></span>

<span data-ttu-id="df66d-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="df66d-112">This method can return one of these values.</span></span>



| <span data-ttu-id="df66d-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="df66d-113">Return code</span></span>                                                                                   | <span data-ttu-id="df66d-114">Description</span><span class="sxs-lookup"><span data-stu-id="df66d-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="df66d-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="df66d-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="df66d-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="df66d-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="df66d-118">Le paramètre *pOriginator* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="df66d-118">The *pOriginator* parameter is not a valid pointer.</span></span><br/>  |
| <dl> <span data-ttu-id="df66d-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="df66d-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="df66d-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="df66d-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="df66d-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="df66d-122">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="df66d-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="df66d-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="df66d-124">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="df66d-125">Notes</span><span class="sxs-lookup"><span data-stu-id="df66d-125">Remarks</span></span>

<span data-ttu-id="df66d-126">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *POriginator* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="df66d-126">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pOriginator* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="df66d-127">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="df66d-127">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="df66d-128">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="df66d-128">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="df66d-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df66d-129">Requirements</span></span>



| <span data-ttu-id="df66d-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df66d-130">Requirement</span></span> | <span data-ttu-id="df66d-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="df66d-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df66d-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="df66d-132">TAPI version</span></span><br/> | <span data-ttu-id="df66d-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="df66d-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="df66d-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="df66d-134">Header</span></span><br/>       | <dl> <span data-ttu-id="df66d-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="df66d-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="df66d-136">Library</span></span><br/>      | <dl> <span data-ttu-id="df66d-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="df66d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="df66d-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="df66d-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="df66d-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df66d-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df66d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df66d-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="df66d-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="df66d-142">**ITSdp :: obtient l' \_ expéditeur**</span><span class="sxs-lookup"><span data-stu-id="df66d-142">**ITSdp::get\_Originator**</span></span>](itsdp-get-originator.md)
</dt> </dl>

 

