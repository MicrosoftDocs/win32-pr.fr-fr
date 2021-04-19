---
description: La méthode EnumerateStreams énumère les flux en cours avec les participants. Cette méthode est fournie pour les applications C et C++. Les applications clientes Automation, telles que celles écrites en Visual Basic, doivent utiliser la méthode d’extraction de \_ flux.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'ITParticipant :: EnumerateStreams, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526567"
---
# <a name="itparticipantenumeratestreams-method"></a><span data-ttu-id="b0cf1-105">ITParticipant :: EnumerateStreams, méthode</span><span class="sxs-lookup"><span data-stu-id="b0cf1-105">ITParticipant::EnumerateStreams method</span></span>

<span data-ttu-id="b0cf1-106">\[**EnumerateStreams** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-106">\[**EnumerateStreams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b0cf1-107">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="b0cf1-107">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b0cf1-108">La méthode **EnumerateStreams** énumère les flux en cours avec les participants.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-108">The **EnumerateStreams** method enumerates streams currently with the participants.</span></span> <span data-ttu-id="b0cf1-109">Cette méthode est fournie pour les applications C et C++.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-109">This method is provided for C and C++ applications.</span></span> <span data-ttu-id="b0cf1-110">Les applications clientes Automation, telles que celles écrites en Visual Basic, doivent utiliser la méthode d' [**extraction de \_ flux**](itparticipant-get-streams.md) .</span><span class="sxs-lookup"><span data-stu-id="b0cf1-110">Automation client applications, such as those written in Visual Basic, must use the [**get\_Streams**](itparticipant-get-streams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0cf1-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0cf1-111">Syntax</span></span>


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a><span data-ttu-id="b0cf1-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0cf1-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0cf1-113">*ppEnumStream* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b0cf1-113">*ppEnumStream* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b0cf1-114">Pointeur vers le pointeur d’interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .</span><span class="sxs-lookup"><span data-stu-id="b0cf1-114">Pointer to [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0cf1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0cf1-115">Return value</span></span>

<span data-ttu-id="b0cf1-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-116">This method can return one of these values.</span></span>



| <span data-ttu-id="b0cf1-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0cf1-117">Value</span></span>                                                                                     | <span data-ttu-id="b0cf1-118">Signification</span><span class="sxs-lookup"><span data-stu-id="b0cf1-118">Meaning</span></span>                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="b0cf1-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b0cf1-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="b0cf1-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b0cf1-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="b0cf1-121"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="b0cf1-122">Le paramètre *ppEnumStream* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-122">The *ppEnumStream* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b0cf1-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b0cf1-123">Remarks</span></span>

<span data-ttu-id="b0cf1-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) retournée par **ITParticipant :: EnumerateStreams**.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-124">TAPI calls the **AddRef** method on the [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) interface returned by **ITParticipant::EnumerateStreams**.</span></span> <span data-ttu-id="b0cf1-125">L’application doit appeler **Release** sur l’interface **IEnumStream** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="b0cf1-125">The application must call **Release** on the **IEnumStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0cf1-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0cf1-126">Requirements</span></span>



| <span data-ttu-id="b0cf1-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0cf1-127">Requirement</span></span> | <span data-ttu-id="b0cf1-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0cf1-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b0cf1-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b0cf1-129">TAPI version</span></span><br/> | <span data-ttu-id="b0cf1-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b0cf1-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="b0cf1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b0cf1-131">Header</span></span><br/>       | <dl> <span data-ttu-id="b0cf1-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0cf1-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b0cf1-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b0cf1-133">Library</span></span><br/>      | <dl> <span data-ttu-id="b0cf1-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0cf1-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="b0cf1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b0cf1-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="b0cf1-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0cf1-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0cf1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0cf1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0cf1-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="b0cf1-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="b0cf1-139">**recevoir des \_ flux**</span><span class="sxs-lookup"><span data-stu-id="b0cf1-139">**get\_Streams**</span></span>](itparticipant-get-streams.md)
</dt> <dt>

[<span data-ttu-id="b0cf1-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="b0cf1-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




