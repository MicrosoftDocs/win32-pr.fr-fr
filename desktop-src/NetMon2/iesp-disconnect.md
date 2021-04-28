---
description: IESP ::D méthode éconnecter-la méthode Disconnect déconnecte le NPP du réseau.
ms.assetid: 962e033d-a51c-47a2-83dc-cee1e7150ab8
title: IESP ::D méthode éconnecter (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.Disconnect
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: d0a07748781a567c889e879e2e99462d8cfb876a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110757"
---
# <a name="iespdisconnect-method"></a><span data-ttu-id="5c09d-103">IESP ::D méthode éconnecter</span><span class="sxs-lookup"><span data-stu-id="5c09d-103">IESP::Disconnect method</span></span>

<span data-ttu-id="5c09d-104">La **méthode Disconnect** déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="5c09d-104">The **Disconnect** method disconnects the NPP from the network.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c09d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c09d-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE Disconnect();
```



## <a name="parameters"></a><span data-ttu-id="5c09d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c09d-106">Parameters</span></span>

<span data-ttu-id="5c09d-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5c09d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5c09d-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5c09d-108">Return value</span></span>

<span data-ttu-id="5c09d-109">Si la méthode réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5c09d-109">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="5c09d-110">Si la méthode échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="5c09d-110">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="5c09d-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5c09d-111">Return code</span></span>                                                                                          | <span data-ttu-id="5c09d-112">Description</span><span class="sxs-lookup"><span data-stu-id="5c09d-112">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c09d-113"><dt>**\_capture NMERR**</dt></span><span class="sxs-lookup"><span data-stu-id="5c09d-113"><dt>**NMERR\_CAPTURING**</dt></span></span> </dl>      | <span data-ttu-id="5c09d-114">Le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="5c09d-114">The NPP is capturing data.</span></span> <span data-ttu-id="5c09d-115">Vous ne pouvez pas vous déconnecter du réseau pendant que la capture de données est en cours.</span><span class="sxs-lookup"><span data-stu-id="5c09d-115">You cannot disconnect from the network while data capture is in progress.</span></span><br/> |
| <dl> <span data-ttu-id="5c09d-116"><dt>**NMERR \_ non \_ connecté**</dt></span><span class="sxs-lookup"><span data-stu-id="5c09d-116"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5c09d-117">Le NPP n’est pas connecté au réseau.</span><span class="sxs-lookup"><span data-stu-id="5c09d-117">The NPP is not connected to the network.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="5c09d-118"><dt>**NMERR \_ non \_ ESP**</dt></span><span class="sxs-lookup"><span data-stu-id="5c09d-118"><dt>**NMERR\_NOT\_ESP**</dt></span></span> </dl>       | <span data-ttu-id="5c09d-119">Le NPP est connecté au réseau, mais pas avec la méthode [IESP :: Connect](iesp-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="5c09d-119">The NPP is connected to the network but not with the [IESP::Connect](iesp-connect.md) method.</span></span><br/>       |



 

## <a name="remarks"></a><span data-ttu-id="5c09d-120">Notes </span><span class="sxs-lookup"><span data-stu-id="5c09d-120">Remarks</span></span>

<span data-ttu-id="5c09d-121">Cette méthode ne peut pas être appelée lorsque le NPP capture des données.</span><span class="sxs-lookup"><span data-stu-id="5c09d-121">This method cannot be called when the NPP is capturing data.</span></span> <span data-ttu-id="5c09d-122">Vous devez appeler la méthode **IESP :: Stop** avant d’appeler **IESP ::D éconnecter**.</span><span class="sxs-lookup"><span data-stu-id="5c09d-122">You must call the **IESP::Stop** method before calling **IESP::Disconnect**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c09d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c09d-123">Requirements</span></span>



| <span data-ttu-id="5c09d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c09d-124">Requirement</span></span> | <span data-ttu-id="5c09d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c09d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c09d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c09d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5c09d-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c09d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5c09d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c09d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5c09d-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c09d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5c09d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c09d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c09d-131"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c09d-131"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5c09d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5c09d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c09d-133"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c09d-133"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c09d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5c09d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c09d-135">IESP</span><span class="sxs-lookup"><span data-stu-id="5c09d-135">IESP</span></span>](iesp.md)
</dt> <dt>

[<span data-ttu-id="5c09d-136">IESP :: Connect</span><span class="sxs-lookup"><span data-stu-id="5c09d-136">IESP::Connect</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="5c09d-137">IESP :: Stop</span><span class="sxs-lookup"><span data-stu-id="5c09d-137">IESP::Stop</span></span>](iesp-stop.md)
</dt> </dl>

 

 




