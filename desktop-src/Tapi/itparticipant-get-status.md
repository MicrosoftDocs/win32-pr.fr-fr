---
description: La \_ méthode d’état d’extraction renvoie une variante \_ booléenne indiquant l’état du participant.
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'ITParticipant :: get_Status, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524009"
---
# <a name="itparticipantget_status-method"></a><span data-ttu-id="251c0-103">ITParticipant :: obtient l' \_ État, méthode</span><span class="sxs-lookup"><span data-stu-id="251c0-103">ITParticipant::get\_Status method</span></span>

<span data-ttu-id="251c0-104">\[en **savoir \_ plus L’État** ne peut pas être utilisé dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="251c0-104">\[**get\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="251c0-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="251c0-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="251c0-106">La méthode d' **\_ État d’extraction** renvoie une variante \_ booléenne indiquant l’état du participant.</span><span class="sxs-lookup"><span data-stu-id="251c0-106">The **get\_Status** method returns a VARIANT\_BOOL indicating participant status.</span></span>

## <a name="syntax"></a><span data-ttu-id="251c0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="251c0-107">Syntax</span></span>


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="251c0-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="251c0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="251c0-109">*pITStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="251c0-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="251c0-110">Pointeur vers l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="251c0-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="251c0-111">*pStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="251c0-111">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="251c0-112">VARIANTE \_ true si le participant est activé sur le flux, variant \_ false s’il est désactivé.</span><span class="sxs-lookup"><span data-stu-id="251c0-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="251c0-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="251c0-113">Return value</span></span>

<span data-ttu-id="251c0-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="251c0-114">This method can return one of these values.</span></span>



| <span data-ttu-id="251c0-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="251c0-115">Return code</span></span>                                                                                   | <span data-ttu-id="251c0-116">Description</span><span class="sxs-lookup"><span data-stu-id="251c0-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="251c0-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="251c0-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="251c0-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="251c0-119"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="251c0-120">Méthode non implémentée.</span><span class="sxs-lookup"><span data-stu-id="251c0-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="251c0-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="251c0-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="251c0-122">Insufficient memory exists to perform the operation.</span></span><br/>           |
| <dl> <span data-ttu-id="251c0-123"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="251c0-124">Le paramètre *pITStream* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="251c0-124">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="251c0-125"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="251c0-126">Le paramètre *pITStream* ne pointe pas vers une interface valide.</span><span class="sxs-lookup"><span data-stu-id="251c0-126">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="251c0-127">Notes</span><span class="sxs-lookup"><span data-stu-id="251c0-127">Remarks</span></span>

<span data-ttu-id="251c0-128">L’activation ou la désactivation de l’état d’un participant sur un flux permet à une application de désactiver un participant donné.</span><span class="sxs-lookup"><span data-stu-id="251c0-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="251c0-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="251c0-129">Requirements</span></span>



| <span data-ttu-id="251c0-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="251c0-130">Requirement</span></span> | <span data-ttu-id="251c0-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="251c0-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="251c0-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="251c0-132">TAPI version</span></span><br/> | <span data-ttu-id="251c0-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="251c0-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="251c0-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="251c0-134">Header</span></span><br/>       | <dl> <span data-ttu-id="251c0-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="251c0-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="251c0-136">Library</span></span><br/>      | <dl> <span data-ttu-id="251c0-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="251c0-138">DLL</span><span class="sxs-lookup"><span data-stu-id="251c0-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="251c0-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="251c0-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="251c0-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="251c0-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="251c0-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="251c0-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="251c0-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="251c0-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="251c0-143">**Placer l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="251c0-143">**put\_Status**</span></span>](itparticipant-put-status.md)
</dt> </dl>

 

