---
description: La \_ méthode obtenir TransportProtocol obtient le protocole de transport.
ms.assetid: d270d6f4-bdcf-4cf4-970b-65f0be706171
title: 'ITMedia :: get_TransportProtocol, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf2bc66a98e181674bbf6f7956579bbaa0b5a72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537334"
---
# <a name="itmediaget_transportprotocol-method"></a><span data-ttu-id="2a87d-103">ITMedia :: \_ TransportProtocol, méthode</span><span class="sxs-lookup"><span data-stu-id="2a87d-103">ITMedia::get\_TransportProtocol method</span></span>

<span data-ttu-id="2a87d-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2a87d-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="2a87d-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="2a87d-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="2a87d-106">La méthode **obtenir \_ TransportProtocol** obtient le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="2a87d-106">The **get\_TransportProtocol** method gets the transport protocol.</span></span> <span data-ttu-id="2a87d-107">Cela est spécifié en plus du format de média, de sorte que le même format de média standard peut être utilisé sur différents protocoles de transport, même lorsque le protocole réseau est le même, par exemple avec les signaux audio de TVA PCM et audio PCM RTP.</span><span class="sxs-lookup"><span data-stu-id="2a87d-107">This is specified in addition to the media format so that the same standard media format may be carried over different transport protocols even when the network protocol is the same, such as with Vat PCM audio and RTP PCM audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a87d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a87d-108">Syntax</span></span>


```C++
HRESULT get_TransportProtocol(
  [out] BSTR *ppProtocol
);
```



## <a name="parameters"></a><span data-ttu-id="2a87d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a87d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a87d-110">*ppProtocol* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2a87d-110">*ppProtocol* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a87d-111">Pointeur vers la représentation **BSTR** du protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="2a87d-111">Pointer to the **BSTR** representation of the transport protocol.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a87d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2a87d-112">Return value</span></span>

<span data-ttu-id="2a87d-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="2a87d-113">This method can return one of these values.</span></span>



| <span data-ttu-id="2a87d-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="2a87d-114">Return code</span></span>                                                                                   | <span data-ttu-id="2a87d-115">Description</span><span class="sxs-lookup"><span data-stu-id="2a87d-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="2a87d-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="2a87d-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="2a87d-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2a87d-118"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="2a87d-119">Le paramètre *ppProtocol* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="2a87d-119">The *ppProtocol* parameter is not a valid pointer.</span></span><br/>   |
| <dl> <span data-ttu-id="2a87d-120"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="2a87d-121">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="2a87d-121">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="2a87d-122"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-122"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="2a87d-123">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2a87d-123">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="2a87d-124"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-124"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="2a87d-125">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="2a87d-125">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="2a87d-126">Notes</span><span class="sxs-lookup"><span data-stu-id="2a87d-126">Remarks</span></span>

<span data-ttu-id="2a87d-127">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppProtocol* .</span><span class="sxs-lookup"><span data-stu-id="2a87d-127">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppProtocol* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a87d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a87d-128">Requirements</span></span>



| <span data-ttu-id="2a87d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2a87d-129">Requirement</span></span> | <span data-ttu-id="2a87d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="2a87d-130">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a87d-131">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="2a87d-131">TAPI version</span></span><br/> | <span data-ttu-id="2a87d-132">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="2a87d-132">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="2a87d-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="2a87d-133">Header</span></span><br/>       | <dl> <span data-ttu-id="2a87d-134"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-134"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a87d-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2a87d-135">Library</span></span><br/>      | <dl> <span data-ttu-id="2a87d-136"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-136"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="2a87d-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2a87d-137">DLL</span></span><br/>          | <dl> <span data-ttu-id="2a87d-138"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a87d-138"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a87d-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a87d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a87d-140">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="2a87d-140">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="2a87d-141">**ITMedia ::p ut \_ TransportProtocol**</span><span class="sxs-lookup"><span data-stu-id="2a87d-141">**ITMedia::put\_TransportProtocol**</span></span>](itmedia-put-transportprotocol.md)
</dt> </dl>

 

