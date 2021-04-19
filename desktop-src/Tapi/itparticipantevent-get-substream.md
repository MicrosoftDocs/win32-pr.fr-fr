---
description: Le sous-flux d’extraction \_ obtient un pointeur vers un tableau d’interfaces ITSubStream représentant les sous-flux impliqués dans l’événement.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: 'ITParticipantEvent :: get_SubStream, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8c2944004af31adfb7256376992506eef59b40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542607"
---
# <a name="itparticipanteventget_substream-method"></a><span data-ttu-id="cde3a-103">ITParticipantEvent :: obtient la méthode de sous- \_ flux</span><span class="sxs-lookup"><span data-stu-id="cde3a-103">ITParticipantEvent::get\_SubStream method</span></span>

<span data-ttu-id="cde3a-104">\[en **savoir \_ plus** Le sous-flux ne peut pas être utilisé dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="cde3a-104">\[**get\_SubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cde3a-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="cde3a-106">Le sous- **\_ flux d’extraction** obtient un pointeur vers un tableau d’interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) représentant les sous-flux impliqués dans l’événement.</span><span class="sxs-lookup"><span data-stu-id="cde3a-106">The **get\_SubStream** gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="cde3a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cde3a-107">Syntax</span></span>


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="cde3a-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cde3a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cde3a-109">*ppSubStream* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cde3a-109">*ppSubStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cde3a-110">Pointeur vers un tableau de pointeurs [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="cde3a-110">Pointer to array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cde3a-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cde3a-111">Return value</span></span>

<span data-ttu-id="cde3a-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="cde3a-112">This method can return one of these values.</span></span>



| <span data-ttu-id="cde3a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="cde3a-113">Value</span></span>                                                                                           | <span data-ttu-id="cde3a-114">Signification</span><span class="sxs-lookup"><span data-stu-id="cde3a-114">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="cde3a-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-115"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="cde3a-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="cde3a-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cde3a-117"><dt>**\_NOitems TAPI E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-117"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="cde3a-118">Aucun sous-flux n’est associé à l’événement.</span><span class="sxs-lookup"><span data-stu-id="cde3a-118">There are no substreams associated with the event.</span></span><br/>   |
| <dl> <span data-ttu-id="cde3a-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="cde3a-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="cde3a-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="cde3a-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-121"><dt>**E\_POINTER**</dt></span></span> </dl>       | <span data-ttu-id="cde3a-122">Le paramètre *ppSubStream* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="cde3a-122">The *ppSubStream* parameter is not a valid pointer.</span></span><br/>  |



 

## <a name="requirements"></a><span data-ttu-id="cde3a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cde3a-123">Requirements</span></span>



| <span data-ttu-id="cde3a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cde3a-124">Requirement</span></span> | <span data-ttu-id="cde3a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="cde3a-125">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cde3a-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="cde3a-126">TAPI version</span></span><br/> | <span data-ttu-id="cde3a-127">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="cde3a-127">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="cde3a-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="cde3a-128">Header</span></span><br/>       | <dl> <span data-ttu-id="cde3a-129"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-129"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="cde3a-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cde3a-130">Library</span></span><br/>      | <dl> <span data-ttu-id="cde3a-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-131"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="cde3a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cde3a-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="cde3a-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cde3a-133"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="cde3a-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cde3a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde3a-135">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="cde3a-135">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="cde3a-136">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="cde3a-136">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

