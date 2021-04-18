---
description: La \_ méthode obtenir des flux crée une collection de flux associés au participant actuel.
ms.assetid: 9ab05b14-8ef8-4e7f-b598-05795011e35d
title: 'ITParticipant :: get_Streams, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a920929c71e01632edcd8c4c78029b479d8b250
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526084"
---
# <a name="itparticipantget_streams-method"></a><span data-ttu-id="a63f3-103">ITParticipant :: obtient les \_ flux, méthode</span><span class="sxs-lookup"><span data-stu-id="a63f3-103">ITParticipant::get\_Streams method</span></span>

<span data-ttu-id="a63f3-104">\[en **savoir \_ plus Les flux** ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="a63f3-104">\[**get\_Streams** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a63f3-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="a63f3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a63f3-106">La méthode **obtenir des \_ flux** crée une collection de flux associés au participant actuel.</span><span class="sxs-lookup"><span data-stu-id="a63f3-106">The **get\_Streams** method creates a collection of streams associated with the current participant.</span></span> <span data-ttu-id="a63f3-107">Cette méthode est fournie pour les applications clientes Automation, telles que celles écrites en Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="a63f3-107">This method is provided for Automation client applications, such as those written in Visual Basic.</span></span> <span data-ttu-id="a63f3-108">Les applications C et C++ doivent utiliser la méthode [**EnumerateStreams**](itparticipant-enumeratestreams.md) .</span><span class="sxs-lookup"><span data-stu-id="a63f3-108">C and C++ applications must use the [**EnumerateStreams**](itparticipant-enumeratestreams.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a63f3-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a63f3-109">Syntax</span></span>


```C++
HRESULT get_Streams(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a><span data-ttu-id="a63f3-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a63f3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a63f3-111">*pVariant* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a63f3-111">*pVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a63f3-112">Pointeur vers un **Variant** contenant un [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de pointeurs d’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="a63f3-112">Pointer to **VARIANT** containing an [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) of [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a63f3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a63f3-113">Return value</span></span>

<span data-ttu-id="a63f3-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="a63f3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a63f3-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="a63f3-115">Value</span></span>                                                                                         | <span data-ttu-id="a63f3-116">Signification</span><span class="sxs-lookup"><span data-stu-id="a63f3-116">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="a63f3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a63f3-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="a63f3-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="a63f3-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a63f3-119"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="a63f3-119"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="a63f3-120">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="a63f3-120">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="a63f3-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="a63f3-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="a63f3-122">Le paramètre *pVariant* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="a63f3-122">The *pVariant* parameter is not a valid pointer.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="a63f3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="a63f3-123">Remarks</span></span>

<span data-ttu-id="a63f3-124">L’interface TAPI appelle la méthode **AddRef** sur l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) retournée par **ITParticipant :: obten \_ Streams**.</span><span class="sxs-lookup"><span data-stu-id="a63f3-124">TAPI calls the **AddRef** method on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface returned by **ITParticipant::get\_Streams**.</span></span> <span data-ttu-id="a63f3-125">L’application doit appeler **Release** sur l’interface **ITStream** pour libérer les ressources qui lui sont associées.</span><span class="sxs-lookup"><span data-stu-id="a63f3-125">The application must call **Release** on the **ITStream** interface to free resources associated with it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a63f3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a63f3-126">Requirements</span></span>



| <span data-ttu-id="a63f3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a63f3-127">Requirement</span></span> | <span data-ttu-id="a63f3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a63f3-128">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a63f3-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="a63f3-129">TAPI version</span></span><br/> | <span data-ttu-id="a63f3-130">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="a63f3-130">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="a63f3-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="a63f3-131">Header</span></span><br/>       | <dl> <span data-ttu-id="a63f3-132"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="a63f3-132"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a63f3-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a63f3-133">Library</span></span><br/>      | <dl> <span data-ttu-id="a63f3-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a63f3-134"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="a63f3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="a63f3-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="a63f3-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a63f3-136"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a63f3-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a63f3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a63f3-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="a63f3-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="a63f3-139">**EnumerateStreams**</span><span class="sxs-lookup"><span data-stu-id="a63f3-139">**EnumerateStreams**</span></span>](itparticipant-enumeratestreams.md)
</dt> <dt>

[<span data-ttu-id="a63f3-140">**IEnumStream**</span><span class="sxs-lookup"><span data-stu-id="a63f3-140">**IEnumStream**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> <dt>

[<span data-ttu-id="a63f3-141">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="a63f3-141">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[<span data-ttu-id="a63f3-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="a63f3-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> </dl>

 

