---
description: La \_ méthode obtenir ProtocolVersion obtient la version du protocole 2327 SDP (session descripteur).
ms.assetid: 7c62357c-427f-40f9-a9d2-c4e1a8400e97
title: 'ITSdp :: get_ProtocolVersion, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 652c6c3d6723a10cfe474376cf8b9f1342321db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532607"
---
# <a name="itsdpget_protocolversion-method"></a><span data-ttu-id="71b58-103">ITSdp :: \_ ProtocolVersion, méthode</span><span class="sxs-lookup"><span data-stu-id="71b58-103">ITSdp::get\_ProtocolVersion method</span></span>

<span data-ttu-id="71b58-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="71b58-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="71b58-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="71b58-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="71b58-106">La méthode **obtenir \_ ProtocolVersion** obtient la version du protocole 2327 SDP (session descripteur).</span><span class="sxs-lookup"><span data-stu-id="71b58-106">The **get\_ProtocolVersion** method gets the Session Descriptor Protocol (SDP; see RFC 2327) protocol version.</span></span>

## <a name="syntax"></a><span data-ttu-id="71b58-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71b58-107">Syntax</span></span>


```C++
HRESULT get_ProtocolVersion(
  [out] unsigned char *pProtocolVersion
);
```



## <a name="parameters"></a><span data-ttu-id="71b58-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71b58-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71b58-109">*pProtocolVersion* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="71b58-109">*pProtocolVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71b58-110">Pointeur désignant la version du protocole.</span><span class="sxs-lookup"><span data-stu-id="71b58-110">Pointer to the protocol version.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71b58-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="71b58-111">Return value</span></span>

<span data-ttu-id="71b58-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="71b58-112">This method can return one of these values.</span></span>



| <span data-ttu-id="71b58-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="71b58-113">Return code</span></span>                                                                                   | <span data-ttu-id="71b58-114">Description</span><span class="sxs-lookup"><span data-stu-id="71b58-114">Description</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <span data-ttu-id="71b58-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="71b58-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="71b58-116">Method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="71b58-117"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-117"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="71b58-118">Le paramètre *pProtocolVersion* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="71b58-118">The *pProtocolVersion* parameter is not a valid pointer.</span></span><br/> |
| <dl> <span data-ttu-id="71b58-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="71b58-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="71b58-120">Insufficient memory exists to perform the operation.</span></span><br/>     |
| <dl> <span data-ttu-id="71b58-121"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-121"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="71b58-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="71b58-122">Unspecified error.</span></span><br/>                                       |
| <dl> <span data-ttu-id="71b58-123"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-123"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="71b58-124">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="71b58-124">This method is not yet implemented.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="71b58-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="71b58-125">Requirements</span></span>



| <span data-ttu-id="71b58-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="71b58-126">Requirement</span></span> | <span data-ttu-id="71b58-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="71b58-127">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71b58-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="71b58-128">TAPI version</span></span><br/> | <span data-ttu-id="71b58-129">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="71b58-129">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="71b58-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="71b58-130">Header</span></span><br/>       | <dl> <span data-ttu-id="71b58-131"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-131"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="71b58-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="71b58-132">Library</span></span><br/>      | <dl> <span data-ttu-id="71b58-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-133"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="71b58-134">DLL</span><span class="sxs-lookup"><span data-stu-id="71b58-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="71b58-135"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71b58-135"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71b58-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="71b58-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71b58-137">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="71b58-137">**ITSdp**</span></span>](itsdp.md)
</dt> </dl>

 

 




