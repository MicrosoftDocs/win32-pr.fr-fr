---
description: La méthode SwitchTerminalToSubStream définit un terminal sur le sous-flux du participant.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'ITParticipantSubStreamControl :: SwitchTerminalToSubStream, méthode (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540098"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a><span data-ttu-id="ea490-103">ITParticipantSubStreamControl :: SwitchTerminalToSubStream, méthode</span><span class="sxs-lookup"><span data-stu-id="ea490-103">ITParticipantSubStreamControl::SwitchTerminalToSubStream method</span></span>

<span data-ttu-id="ea490-104">\[**SwitchTerminalToSubStream** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ea490-104">\[**SwitchTerminalToSubStream** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ea490-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ea490-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ea490-106">La méthode **SwitchTerminalToSubStream** définit un terminal sur le sous-flux du participant.</span><span class="sxs-lookup"><span data-stu-id="ea490-106">The **SwitchTerminalToSubStream** method sets a terminal to the participant substream.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea490-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea490-107">Syntax</span></span>


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a><span data-ttu-id="ea490-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea490-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea490-109">*pITTerminal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea490-109">*pITTerminal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea490-110">Pointeur vers l’interface [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .</span><span class="sxs-lookup"><span data-stu-id="ea490-110">Pointer to [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ea490-111">*pITSubStream* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea490-111">*pITSubStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea490-112">Pointeur vers l’interface [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .</span><span class="sxs-lookup"><span data-stu-id="ea490-112">Pointer to [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea490-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea490-113">Return value</span></span>

<span data-ttu-id="ea490-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="ea490-114">This method can return one of these values.</span></span>



| <span data-ttu-id="ea490-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="ea490-115">Return code</span></span>                                                                                     | <span data-ttu-id="ea490-116">Description</span><span class="sxs-lookup"><span data-stu-id="ea490-116">Description</span></span>                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea490-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-117"><dt>**S\_OK**</dt></span></span> </dl>            | <span data-ttu-id="ea490-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="ea490-118">Method succeeded.</span></span><br/>                                                                       |
| <dl> <span data-ttu-id="ea490-119"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-119"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>    | <span data-ttu-id="ea490-120">Impossible d’accéder aux informations sur le participant pour le flux.</span><span class="sxs-lookup"><span data-stu-id="ea490-120">Participant information for the stream could not be accessed.</span></span><br/>                           |
| <dl> <span data-ttu-id="ea490-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl>    | <span data-ttu-id="ea490-122">Le paramètre *pParticipant* ou *pITSubStream* ne pointe pas vers une interface valide.</span><span class="sxs-lookup"><span data-stu-id="ea490-122">The *pParticipant* or the *pITSubStream* parameter does not point to a valid interface.</span></span><br/> |
| <dl> <span data-ttu-id="ea490-123"><dt>**\_NOitems TAPI E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-123"><dt>**TAPI\_E\_NOITEMS**</dt></span></span> </dl> | <span data-ttu-id="ea490-124">Le sous-flux n’est pas prêt.</span><span class="sxs-lookup"><span data-stu-id="ea490-124">The substream is not ready.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="ea490-125"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>   | <span data-ttu-id="ea490-126">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="ea490-126">Insufficient memory exists to perform the operation.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="ea490-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea490-127">Requirements</span></span>



| <span data-ttu-id="ea490-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea490-128">Requirement</span></span> | <span data-ttu-id="ea490-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea490-129">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ea490-130">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ea490-130">TAPI version</span></span><br/> | <span data-ttu-id="ea490-131">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ea490-131">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ea490-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea490-132">Header</span></span><br/>       | <dl> <span data-ttu-id="ea490-133"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-133"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="ea490-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea490-134">Library</span></span><br/>      | <dl> <span data-ttu-id="ea490-135"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-135"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ea490-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ea490-136">DLL</span></span><br/>          | <dl> <span data-ttu-id="ea490-137"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea490-137"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ea490-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea490-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea490-139">**ITParticipantSubStreamControl**</span><span class="sxs-lookup"><span data-stu-id="ea490-139">**ITParticipantSubStreamControl**</span></span>](itparticipantsubstreamcontrol.md)
</dt> <dt>

[<span data-ttu-id="ea490-140">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="ea490-140">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="ea490-141">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="ea490-141">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="ea490-142">**ITTerminal**</span><span class="sxs-lookup"><span data-stu-id="ea490-142">**ITTerminal**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

