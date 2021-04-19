---
description: La \_ méthode put Status définit l’état d’un participant.
ms.assetid: 8478fcf4-00b3-4b77-9859-e5a80ce24be1
title: ITParticipant ::p ut_Status, méthode (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82eadc9832105ecb0cf440b070dbff8b3fe658d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537499"
---
# <a name="itparticipantput_status-method"></a><span data-ttu-id="e8bf3-103">ITParticipant ::p \_ méthode d’État ut</span><span class="sxs-lookup"><span data-stu-id="e8bf3-103">ITParticipant::put\_Status method</span></span>

<span data-ttu-id="e8bf3-104">\[**mettre \_ L’État** ne peut pas être utilisé dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-104">\[**put\_Status** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e8bf3-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="e8bf3-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e8bf3-106">La méthode **put \_ Status** définit l’état d’un participant.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-106">The **put\_Status** method sets the status of a participant.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8bf3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8bf3-107">Syntax</span></span>


```C++
HRESULT put_Status(
  [in] ITStream     *pITStream,
  [in] VARIANT_BOOL fEnable
);
```



## <a name="parameters"></a><span data-ttu-id="e8bf3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8bf3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8bf3-109">*pITStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8bf3-109">*pITStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bf3-110">Pointeur vers l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) .</span><span class="sxs-lookup"><span data-stu-id="e8bf3-110">Pointer to [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e8bf3-111">*fEnable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8bf3-111">*fEnable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8bf3-112">VARIANTE \_ true si le participant est activé sur le flux, variant \_ false s’il doit être désactivé.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-112">VARIANT\_TRUE if the participant is enabled on the stream, VARIANT\_FALSE if it is to be disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8bf3-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8bf3-113">Return value</span></span>

<span data-ttu-id="e8bf3-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-114">This method can return one of these values.</span></span>



| <span data-ttu-id="e8bf3-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e8bf3-115">Return code</span></span>                                                                                   | <span data-ttu-id="e8bf3-116">Description</span><span class="sxs-lookup"><span data-stu-id="e8bf3-116">Description</span></span>                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8bf3-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e8bf3-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-118">Method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="e8bf3-119"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-119"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="e8bf3-120">Méthode non implémentée.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-120">Method not implemented.</span></span><br/>                                        |
| <dl> <span data-ttu-id="e8bf3-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-121"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e8bf3-122">Le paramètre *pITStream* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-122">The *pITStream* parameter is not a valid pointer.</span></span><br/>              |
| <dl> <span data-ttu-id="e8bf3-123"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e8bf3-124">Le paramètre *pITStream* ne pointe pas vers une interface valide.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-124">The *pITStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="e8bf3-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e8bf3-126">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-126">Insufficient memory exists to perform the operation.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="e8bf3-127">Notes</span><span class="sxs-lookup"><span data-stu-id="e8bf3-127">Remarks</span></span>

<span data-ttu-id="e8bf3-128">L’activation ou la désactivation de l’état d’un participant sur un flux permet à une application de désactiver un participant donné.</span><span class="sxs-lookup"><span data-stu-id="e8bf3-128">Enabling or disabling a participant's status on a stream allows an application to essentially mute a given participant.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8bf3-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8bf3-129">Requirements</span></span>



| <span data-ttu-id="e8bf3-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8bf3-130">Requirement</span></span> | <span data-ttu-id="e8bf3-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8bf3-131">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8bf3-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="e8bf3-132">TAPI version</span></span><br/> | <span data-ttu-id="e8bf3-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="e8bf3-133">Requires TAPI 3.0 or later</span></span><br/>                                                |
| <span data-ttu-id="e8bf3-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8bf3-134">Header</span></span><br/>       | <dl> <span data-ttu-id="e8bf3-135"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-135"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8bf3-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8bf3-136">Library</span></span><br/>      | <dl> <span data-ttu-id="e8bf3-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-137"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="e8bf3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e8bf3-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="e8bf3-139"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8bf3-139"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8bf3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8bf3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8bf3-141">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="e8bf3-141">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="e8bf3-142">**ITStream**</span><span class="sxs-lookup"><span data-stu-id="e8bf3-142">**ITStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[<span data-ttu-id="e8bf3-143">**afficher l' \_ État**</span><span class="sxs-lookup"><span data-stu-id="e8bf3-143">**get\_Status**</span></span>](itparticipant-get-status.md)
</dt> </dl>

 

