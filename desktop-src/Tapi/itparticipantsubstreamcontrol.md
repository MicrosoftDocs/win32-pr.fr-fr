---
description: L’interface ITParticipantSubStreamControl est implémentée par le MSP IPConf.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interface ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535416"
---
# <a name="itparticipantsubstreamcontrol-interface"></a><span data-ttu-id="55e70-103">Interface ITParticipantSubStreamControl</span><span class="sxs-lookup"><span data-stu-id="55e70-103">ITParticipantSubStreamControl interface</span></span>

<span data-ttu-id="55e70-104">\[**ITParticipantSubStreamControl** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="55e70-104">\[**ITParticipantSubStreamControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="55e70-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="55e70-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="55e70-106">L’interface **ITParticipantSubStreamControl** est implémentée par le MSP ipconf.</span><span class="sxs-lookup"><span data-stu-id="55e70-106">The **ITParticipantSubStreamControl** interface is implemented by the IPConf MSP.</span></span> <span data-ttu-id="55e70-107">Cette interface est exposée sur l’objet d’appel.</span><span class="sxs-lookup"><span data-stu-id="55e70-107">This interface is exposed on the call object.</span></span> <span data-ttu-id="55e70-108">Cette interface fournit des méthodes qui permettent à une application de découvrir ou de contrôler la correspondance entre le sous-flux et le participant.</span><span class="sxs-lookup"><span data-stu-id="55e70-108">This interface provides methods that allow an application to either discover or control the matching of substream to participant.</span></span> <span data-ttu-id="55e70-109">L’interface **ITParticipantSubStreamControl** est créée en appelant **QueryInterface** sur [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span><span class="sxs-lookup"><span data-stu-id="55e70-109">The **ITParticipantSubStreamControl** interface is created by calling **QueryInterface** on [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).</span></span>

## <a name="members"></a><span data-ttu-id="55e70-110">Membres</span><span class="sxs-lookup"><span data-stu-id="55e70-110">Members</span></span>

<span data-ttu-id="55e70-111">L’interface **ITParticipantSubStreamControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="55e70-111">The **ITParticipantSubStreamControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="55e70-112">**ITParticipantSubStreamControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="55e70-112">**ITParticipantSubStreamControl** also has these types of members:</span></span>

-   [<span data-ttu-id="55e70-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="55e70-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55e70-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="55e70-114">Methods</span></span>

<span data-ttu-id="55e70-115">L’interface **ITParticipantSubStreamControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="55e70-115">The **ITParticipantSubStreamControl** interface has these methods.</span></span>



| <span data-ttu-id="55e70-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="55e70-116">Method</span></span>                                                                                              | <span data-ttu-id="55e70-117">Description</span><span class="sxs-lookup"><span data-stu-id="55e70-117">Description</span></span>                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="55e70-118">**Obtient \_ ParticipantFromSubStream**</span><span class="sxs-lookup"><span data-stu-id="55e70-118">**get\_ParticipantFromSubStream**</span></span>](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | <span data-ttu-id="55e70-119">Obtient les participants associés à un sous-flux donné.</span><span class="sxs-lookup"><span data-stu-id="55e70-119">Gets participants associated with a given substream.</span></span><br/> |
| [<span data-ttu-id="55e70-120">**Obtient \_ SubStreamFromParticipant**</span><span class="sxs-lookup"><span data-stu-id="55e70-120">**get\_SubStreamFromParticipant**</span></span>](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | <span data-ttu-id="55e70-121">Obtient les sous-flux associés à un participant donné.</span><span class="sxs-lookup"><span data-stu-id="55e70-121">Gets substreams associated with a given participant.</span></span><br/> |
| [<span data-ttu-id="55e70-122">**SwitchTerminalToSubStream**</span><span class="sxs-lookup"><span data-stu-id="55e70-122">**SwitchTerminalToSubStream**</span></span>](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | <span data-ttu-id="55e70-123">Définit un participant sur un sous-flux.</span><span class="sxs-lookup"><span data-stu-id="55e70-123">Sets a participant on a substream.</span></span><br/>                   |



 

## <a name="requirements"></a><span data-ttu-id="55e70-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="55e70-124">Requirements</span></span>



| <span data-ttu-id="55e70-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="55e70-125">Requirement</span></span> | <span data-ttu-id="55e70-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="55e70-126">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55e70-127">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="55e70-127">TAPI version</span></span><br/> | <span data-ttu-id="55e70-128">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="55e70-128">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="55e70-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="55e70-129">Header</span></span><br/>       | <dl> <span data-ttu-id="55e70-130"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="55e70-130"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="55e70-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="55e70-131">Library</span></span><br/>      | <dl> <span data-ttu-id="55e70-132"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55e70-132"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="55e70-133">DLL</span><span class="sxs-lookup"><span data-stu-id="55e70-133">DLL</span></span><br/>          | <dl> <span data-ttu-id="55e70-134"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55e70-134"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="55e70-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="55e70-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55e70-136">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="55e70-136">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="55e70-137">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="55e70-137">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

