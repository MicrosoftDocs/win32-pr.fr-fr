---
description: Le \_ message NEWCALL de la ligne TSPI est envoyé à la fonction de rappel LINEEVENT chaque fois qu’un nouvel appel que TAPI n’est pas arrivé sur une ligne ouverte par TAPI.
ms.assetid: 36122dfb-1ed6-459d-aa2b-69c86daaddd8
title: Message LINE_NEWCALL (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed3e7380b2f328283e5f5cad9e84f5a1d0c450dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535984"
---
# <a name="line_newcall-message"></a><span data-ttu-id="b2968-103">\_Message NEWCALL de ligne</span><span class="sxs-lookup"><span data-stu-id="b2968-103">LINE\_NEWCALL message</span></span>

<span data-ttu-id="b2968-104">Le message **\_ NEWCALL** de la ligne TSPI est envoyé à la fonction de rappel [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) chaque fois qu’un nouvel appel que TAPI n’est pas arrivé sur une ligne ouverte par TAPI.</span><span class="sxs-lookup"><span data-stu-id="b2968-104">The TSPI **LINE\_NEWCALL** message is sent to the [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) callback function whenever a new call that TAPI has not originated arrives on a line that TAPI has open.</span></span> <span data-ttu-id="b2968-105">Il doit s’agir du premier message envoyé concernant cet appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-105">This must be the first message sent regarding that call.</span></span> <span data-ttu-id="b2968-106">L’interface TAPI écrit le descripteur opaque *htCall* à l’emplacement passé par le fournisseur de services en tant que *dwParam2*.</span><span class="sxs-lookup"><span data-stu-id="b2968-106">TAPI writes the *htCall* opaque handle to the location passed by the service provider as *dwParam2*.</span></span> <span data-ttu-id="b2968-107">Cela donne au fournisseur de services la valeur *htCall* à utiliser dans les messages suivants.</span><span class="sxs-lookup"><span data-stu-id="b2968-107">This gives the service provider the *htCall* value to be used in subsequent messages.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="b2968-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b2968-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2968-109">*htLine*</span><span class="sxs-lookup"><span data-stu-id="b2968-109">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="b2968-110">Handle de l’objet opaque TAPI sur le périphérique de ligne.</span><span class="sxs-lookup"><span data-stu-id="b2968-110">The TAPI opaque object handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="b2968-111">*htCall*</span><span class="sxs-lookup"><span data-stu-id="b2968-111">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="b2968-112">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b2968-112">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="b2968-113">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="b2968-113">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="b2968-114">La ligne de valeur \_ NEWCALL.</span><span class="sxs-lookup"><span data-stu-id="b2968-114">The value LINE\_NEWCALL.</span></span>

</dd> <dt>

<span data-ttu-id="b2968-115">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="b2968-115">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="b2968-116">Handle opaque du fournisseur de services pour l’appel, de type [**HDRVCALL**](hdrvline.md).</span><span class="sxs-lookup"><span data-stu-id="b2968-116">The service provider's opaque handle for the call, of type [**HDRVCALL**](hdrvline.md).</span></span> <span data-ttu-id="b2968-117">L’interface TAPI transmet cette valeur en tant que paramètre *hdCall* pour identifier l’appel dans les procédures suivantes qu’il appelle pour fonctionner sur l’appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-117">TAPI passes this value as the *hdCall* parameter to identify the call in subsequent procedures it invokes to operate on the call.</span></span>

</dd> <dt>

<span data-ttu-id="b2968-118">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="b2968-118">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="b2968-119">Pointeur de type LPHTAPICALL pointant vers un [**HTAPICALL**](htapicall.md).</span><span class="sxs-lookup"><span data-stu-id="b2968-119">A pointer of type LPHTAPICALL pointing to a [**HTAPICALL**](htapicall.md).</span></span> <span data-ttu-id="b2968-120">L’interface TAPI écrit le descripteur TAPI opaque pour l’appel à l’emplacement indiqué.</span><span class="sxs-lookup"><span data-stu-id="b2968-120">TAPI writes the TAPI opaque handle for the call to the indicated location.</span></span> <span data-ttu-id="b2968-121">Le fournisseur de services doit enregistrer cette valeur et la passer en tant que paramètre *htCall* pour identifier l’appel dans les événements suivants qu’il signale pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-121">The service provider must save this value and pass it as the *htCall* parameter to identify the call in subsequent events it reports for the call.</span></span>

<span data-ttu-id="b2968-122">Ce paramètre peut également obtenir une valeur **null** (consultez la section Notes suivante).</span><span class="sxs-lookup"><span data-stu-id="b2968-122">This parameter can also acquire a value of **NULL** (see the following Remarks section).</span></span>

</dd> <dt>

<span data-ttu-id="b2968-123">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="b2968-123">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="b2968-124">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="b2968-124">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2968-125">Notes</span><span class="sxs-lookup"><span data-stu-id="b2968-125">Remarks</span></span>

<span data-ttu-id="b2968-126">Le fournisseur de services doit envoyer le message [**\_ CALLSTATE de ligne**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) comme message suivant pour cet appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-126">The service provider should send the [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) message as the next message for this call.</span></span> <span data-ttu-id="b2968-127">L’événement de **ligne \_ NEWCALL** est inhabituel dans le fait qu’il renvoie également une valeur au fournisseur de services.</span><span class="sxs-lookup"><span data-stu-id="b2968-127">The **LINE\_NEWCALL** event is unusual in that it also passes a value back to the service provider.</span></span>

<span data-ttu-id="b2968-128">Cette fonction signale tous les nouveaux appels provenant du fournisseur de services (entrants, sortants, initiés au téléphone, etc.) pour lesquels l’interface TAPI et le fournisseur de services n’ont pas encore échangé les descripteurs opaques.</span><span class="sxs-lookup"><span data-stu-id="b2968-128">This function reports any new calls that originate in the service provider (inbound, outbound, initiated at the phone, and so on) for which TAPI and the service provider have not yet exchanged opaque handles.</span></span> <span data-ttu-id="b2968-129">Les handles sont échangés afin que l’interface TAPI et le fournisseur de services puissent ensuite effectuer des demandes et signaler des événements impliquant l’appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-129">The handles are exchanged so that TAPI and the service provider can subsequently make requests and report events involving the call.</span></span> <span data-ttu-id="b2968-130">Étant donné que ces nouveaux appels ne sont pas nécessairement entrants, les appels peuvent être initialement dans n’importe quel État, pas nécessairement dans l’état d' *offre* .</span><span class="sxs-lookup"><span data-stu-id="b2968-130">Because these new calls are not necessarily inbound, the calls can initially be in any state, not necessarily the *offering* state.</span></span> <span data-ttu-id="b2968-131">Si le fournisseur de services démarre et découvre qu’un ou plusieurs appels sont déjà actifs sur la ligne, il en informe l’interface TAPI avec des messages **\_ NEWCALL de ligne** suivis de messages de [**\_ CALLSTATE de ligne**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) indiquant l’état actuel.</span><span class="sxs-lookup"><span data-stu-id="b2968-131">If the service provider starts and discovers that one or more calls are already active on the line, it informs TAPI of them with **LINE\_NEWCALL** messages followed by [**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) messages indicating the current state.</span></span> <span data-ttu-id="b2968-132">Un nouvel appel sortant, lancé sur le téléphone par l’utilisateur, est signalé avec un message de **ligne \_ NEWCALL** , et le message **\_ CALLSTATE** de la ligne initiale indique que l’appel était en état de **tonalité** (puis continue à partir de là).</span><span class="sxs-lookup"><span data-stu-id="b2968-132">A new outgoing call, initiated on the phone by the user, would be reported with a **LINE\_NEWCALL** message, and the initial **LINE\_CALLSTATE** message would indicate that the call was in **DIALTONE** state (and then continuing on from there).</span></span>

<span data-ttu-id="b2968-133">Si le fournisseur de services passe un grand nombre d’appels à l’interface TAPI dans un laps de temps très bref (au cours du même cycle d’interruption), l’interface TAPI peut être retardée dans le traitement de ces appels.</span><span class="sxs-lookup"><span data-stu-id="b2968-133">If the service provider passes a large number of calls to TAPI in a very short amount of time (during the same interrupt cycle), TAPI can become backlogged in processing those calls.</span></span> <span data-ttu-id="b2968-134">Dans ce cas, l’interface TAPI signale au fournisseur de services qu’il doit attendre un peu de temps avant d’envoyer d’autres appels.</span><span class="sxs-lookup"><span data-stu-id="b2968-134">When this happens, TAPI signals to the service provider to wait a short time before sending any more calls.</span></span> <span data-ttu-id="b2968-135">Il signale cela en écrivant la valeur **null** au lieu d’un [**HTAPICALL**](htapicall.md)valide, à l’emplacement désigné par le paramètre *dwParam2* de la **ligne \_ NEWCALL**.</span><span class="sxs-lookup"><span data-stu-id="b2968-135">It signals this by writing a value of **NULL**, instead of a valid [**HTAPICALL**](htapicall.md), into the location pointed to by the *dwParam2* parameter of **LINE\_NEWCALL**.</span></span> <span data-ttu-id="b2968-136">Cela indique que la tentative de traitement du handle d’appel nouvellement offert a échoué, probablement en raison d’une impossibilité temporaire d’allouer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b2968-136">This indicates that the attempt to process the newly offered call handle was not successful, most likely due to a temporary inability to allocate memory.</span></span> <span data-ttu-id="b2968-137">Le fournisseur de services peut répondre en supprimant l’appel ou en renvoyant le message de **ligne \_ NEWCALL** après un délai de planification (pendant lequel le fournisseur de services doit générer le processeur pour permettre à l’interface TAPI de traiter d’autres actions en attente).</span><span class="sxs-lookup"><span data-stu-id="b2968-137">The service provider can respond by dropping the call or by resending the **LINE\_NEWCALL** message after a scheduling delay (during which time the service provider should yield the processor to allow TAPI to process other pending actions).</span></span> <span data-ttu-id="b2968-138">Dans tous les cas, aucun autre message concernant le nouvel appel ne peut être passé à l’interface TAPI tant que le handle Exchange n’a pas réussi.</span><span class="sxs-lookup"><span data-stu-id="b2968-138">In any case, no further messages regarding the new call can be passed to TAPI until the handle exchange succeeds.</span></span> <span data-ttu-id="b2968-139">Lorsque l’emplacement désigné par *dwParam2* acquiert une valeur non **null** , le fournisseur de services sait que cette valeur est un handle [**HTAPICALL**](htapicall.md) valide pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-139">When the location pointed to by *dwParam2* acquires a non-**NULL** value, the service provider knows that this value is a valid [**HTAPICALL**](htapicall.md) handle to the call.</span></span>

<span data-ttu-id="b2968-140">Il n’y a aucun message directement correspondant au niveau de l’interface TAPI.</span><span class="sxs-lookup"><span data-stu-id="b2968-140">There is no directly corresponding message at the TAPI level.</span></span> <span data-ttu-id="b2968-141">Ce message est utilisé au niveau TSPI pour introduire de manière unique et sans ambiguïté un nouvel appel entrant à TAPI et récupérer l’identificateur opaque TAPI pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="b2968-141">This message is used at the TSPI level to uniquely and unambiguously introduce a new incoming call to TAPI and retrieve the TAPI opaque identifier for the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2968-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2968-142">Requirements</span></span>



| <span data-ttu-id="b2968-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2968-143">Requirement</span></span> | <span data-ttu-id="b2968-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2968-144">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b2968-145">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="b2968-145">TAPI version</span></span><br/> | <span data-ttu-id="b2968-146">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="b2968-146">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="b2968-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2968-147">Header</span></span><br/>       | <dl> <span data-ttu-id="b2968-148"><dt>TSPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2968-148"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2968-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2968-149">See also</span></span>

<dl> <dt>

<span data-ttu-id="b2968-150">[**CALLSTATE de ligne \_**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b2968-150">[**LINE\_CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b2968-151">**LINEEVENT**</span><span class="sxs-lookup"><span data-stu-id="b2968-151">**LINEEVENT**</span></span>](/windows/win32/api/tspi/nc-tspi-lineevent)
</dt> </dl>

 

