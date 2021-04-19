---
description: La \_ méthode put TransportProtocol définit le protocole de transport.
ms.assetid: d2f74d4a-a65d-4829-ad17-7548ef06cfeb
title: ITMedia ::p ut_TransportProtocol, méthode (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c6b4228a5d2a6ea49ae3f87b9306ea80e94fc36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545500"
---
# <a name="itmediaput_transportprotocol-method"></a><span data-ttu-id="7c6fa-103">ITMedia ::p ut \_ TransportProtocol, méthode</span><span class="sxs-lookup"><span data-stu-id="7c6fa-103">ITMedia::put\_TransportProtocol method</span></span>

<span data-ttu-id="7c6fa-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7c6fa-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7c6fa-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7c6fa-106">La méthode **put \_ TransportProtocol** définit le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-106">The **put\_TransportProtocol** method sets the transport protocol.</span></span> <span data-ttu-id="7c6fa-107">Cela est spécifié en plus du format de média, de sorte que le même format de média standard peut être utilisé sur différents protocoles de transport, même lorsque le protocole réseau est le même, par exemple avec les signaux audio de TVA PCM et audio PCM RTP.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c6fa-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c6fa-108">Syntax</span></span>


```C++
HRESULT put_TransportProtocol(
  [in] BSTR pProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="7c6fa-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c6fa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c6fa-110">*pProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7c6fa-110">*pProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c6fa-111">Pointeur vers un **BSTR** contenant le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-111">Pointer to a **BSTR** containing the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c6fa-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7c6fa-112">Return value</span></span>

<span data-ttu-id="7c6fa-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-113">This method can return one of these values.</span></span>



| <span data-ttu-id="7c6fa-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7c6fa-114">Return code</span></span>                                                                                   | <span data-ttu-id="7c6fa-115">Description</span><span class="sxs-lookup"><span data-stu-id="7c6fa-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7c6fa-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7c6fa-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7c6fa-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7c6fa-119">Le paramètre *pProtocol* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-119">The *pProtocol* parameter is not a valid pointer.</span></span><br/>    |
| <dl> <span data-ttu-id="7c6fa-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7c6fa-121">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7c6fa-122"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="7c6fa-123">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="7c6fa-124"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="7c6fa-125">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="7c6fa-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7c6fa-126">Remarks</span></span>

<span data-ttu-id="7c6fa-127">L’application doit utiliser [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) pour allouer de la mémoire pour le paramètre *PProtocol* et utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire lorsque la variable n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-127">The application must use [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) to allocate memory for the *pProtocol* parameter and use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory when the variable is no longer needed.</span></span>

<span data-ttu-id="7c6fa-128">Cette fonction peut envoyer des données sur le réseau sous une forme non chiffrée ; par conséquent, une personne malveillante sur le réseau peut être en mesure de lire les données.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-128">This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data.</span></span> <span data-ttu-id="7c6fa-129">Les risques de sécurité liés à l’envoi des données en texte clair doivent être pris en compte avant d’utiliser cette méthode.</span><span class="sxs-lookup"><span data-stu-id="7c6fa-129">The security risk of sending the data in clear text should be considered before using this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c6fa-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c6fa-130">Requirements</span></span>



| <span data-ttu-id="7c6fa-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c6fa-131">Requirement</span></span> | <span data-ttu-id="7c6fa-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c6fa-132">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c6fa-133">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7c6fa-133">TAPI version</span></span><br/> | <span data-ttu-id="7c6fa-134">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="7c6fa-134">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="7c6fa-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="7c6fa-135">Header</span></span><br/>       | <dl> <span data-ttu-id="7c6fa-136"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-136"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c6fa-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7c6fa-137">Library</span></span><br/>      | <dl> <span data-ttu-id="7c6fa-138"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-138"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="7c6fa-139">DLL</span><span class="sxs-lookup"><span data-stu-id="7c6fa-139">DLL</span></span><br/>          | <dl> <span data-ttu-id="7c6fa-140"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c6fa-140"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c6fa-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c6fa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c6fa-142">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="7c6fa-142">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="7c6fa-143">**ITMedia :: obtient \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="7c6fa-143">**ITMedia::get\_TransportProtocol**</span></span>](itmedia-get-transportprotocol.md)
</dt> </dl>

 

