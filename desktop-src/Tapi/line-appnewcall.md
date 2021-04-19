---
description: Le \_ message APPNEWCALL de ligne TAPI est envoyé pour informer une application lorsqu’un nouveau handle d’appel a été créé spontanément en son nom.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Message LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542686"
---
# <a name="line_appnewcall-message"></a><span data-ttu-id="57c38-103">\_Message APPNEWCALL de ligne</span><span class="sxs-lookup"><span data-stu-id="57c38-103">LINE\_APPNEWCALL message</span></span>

<span data-ttu-id="57c38-104">Le message **\_ APPNEWCALL de ligne** TAPI est envoyé pour informer une application lorsqu’un nouveau handle d’appel a été créé spontanément en son nom (à l’exception d’un appel d’API de l’application, auquel cas le handle aurait été retourné via un paramètre de pointeur transmis à la fonction).</span><span class="sxs-lookup"><span data-stu-id="57c38-104">The TAPI **LINE\_APPNEWCALL** message is sent to inform an application when a new call handle has been spontaneously created on its behalf (other than through an API call from the application, in which case the handle would have been returned through a pointer parameter passed into the function).</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="57c38-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57c38-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57c38-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="57c38-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="57c38-107">Handle de l’application sur le périphérique de ligne sur lequel l’appel a été créé.</span><span class="sxs-lookup"><span data-stu-id="57c38-107">The application's handle to the line device on which the call has been created.</span></span>

</dd> <dt>

<span data-ttu-id="57c38-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="57c38-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="57c38-109">Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.</span><span class="sxs-lookup"><span data-stu-id="57c38-109">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="57c38-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="57c38-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="57c38-111">Identificateur de l’adresse sur la ligne sur laquelle l’appel s’affiche.</span><span class="sxs-lookup"><span data-stu-id="57c38-111">Identifier of the address on the line on which the call appears.</span></span> <span data-ttu-id="57c38-112">Un identificateur d’adresse est associé de manière permanente à une adresse ; l’identificateur reste constant entre les mises à niveau du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="57c38-112">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="57c38-113">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="57c38-113">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="57c38-114">Handle de l’application vers le nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="57c38-114">The application's handle to the new call.</span></span>

</dd> <dt>

<span data-ttu-id="57c38-115">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="57c38-115">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="57c38-116">Privilège des applications au nouvel appel (LINECALLPRIVILEGE \_ owner ou LINECALLPRIVILEGE \_ Monitor).</span><span class="sxs-lookup"><span data-stu-id="57c38-116">The applications privilege to the new call (LINECALLPRIVILEGE\_OWNER or LINECALLPRIVILEGE\_MONITOR).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57c38-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="57c38-117">Return value</span></span>

<span data-ttu-id="57c38-118">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="57c38-118">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="57c38-119">Notes</span><span class="sxs-lookup"><span data-stu-id="57c38-119">Remarks</span></span>

<span data-ttu-id="57c38-120">Les applications prenant en charge TAPI version 2,0 ou ultérieure reçoivent un message de **ligne \_ APPNEWCALL** chaque fois que l’application reçoit spontanément un handle vers un nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="57c38-120">Applications supporting TAPI version 2.0 or later are sent a **LINE\_APPNEWCALL** message whenever the application is spontaneously given a handle to a new call.</span></span> <span data-ttu-id="57c38-121">Étant donné que le message comprend les paramètres *hLine* et *dwAddressID* sur lesquels l’appel existe, l’application peut facilement créer un nouvel objet d’appel dans le contexte approprié.</span><span class="sxs-lookup"><span data-stu-id="57c38-121">Because the message includes the *hLine* and *dwAddressID* parameters on which the call exists, the application can readily create a new call object in the correct context.</span></span> <span data-ttu-id="57c38-122">Le message de **ligne \_ APPNEWCALL** est toujours immédiatement suivi d’un message de [**ligne \_ CALLSTATE**](line-callstate.md) indiquant l’état initial de l’appel.</span><span class="sxs-lookup"><span data-stu-id="57c38-122">The **LINE\_APPNEWCALL** message is always immediately followed by a [**LINE\_CALLSTATE**](line-callstate.md) message indicating the initial state of the call.</span></span>

<span data-ttu-id="57c38-123">Les applications plus anciennes (qui ont négocié une version d’API antérieure à 2,0) sont envoyées uniquement à un message [**\_ CALLSTATE de ligne**](line-callstate.md) , comme indiqué dans les versions précédentes de l’API.</span><span class="sxs-lookup"><span data-stu-id="57c38-123">Older applications (that negotiated an API version earlier than 2.0) are sent only a [**LINE\_CALLSTATE**](line-callstate.md) message, as documented in previous versions of the API.</span></span> <span data-ttu-id="57c38-124">De telles applications créeraient un nouvel objet d’appel lors de la réception d’un message [**\_ CALLSTATE de ligne**](line-callstate.md) dont *dwParam3* a une valeur différente de zéro et qui contient un handle d’appel non connu actuellement par l’application.</span><span class="sxs-lookup"><span data-stu-id="57c38-124">Such applications would create a new call object upon receiving a [**LINE\_CALLSTATE**](line-callstate.md) message that has *dwParam3* set to a nonzero value and containing a call handle not presently known by the application.</span></span> <span data-ttu-id="57c38-125">Les inconvénients sont que (a) l’application doit appeler [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) pour déterminer les paramètres *hLine* et *dwAddressID* associés à l’appel. (b) l’application doit analyser tous les handles d’appel connus pour déterminer que l’appel est un nouvel appel ; et (c) c’est possible, dans certaines conditions, pour que l’application considère qu’elle reçoit un nouveau descripteur d’appel alors qu’en réalité elle vient de libérer son handle à l’appel (par exemple, l’application vient de libérer un handle d’appel, mais un message de [**ligne \_ CALLSTATE**](line-callstate.md) indiquant à l’application la propriété de l’appel en raison d’un [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) d’une autre application était déjà dans la file d’attente de messages TAPI</span><span class="sxs-lookup"><span data-stu-id="57c38-125">The disadvantages are that (a) the application must call [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) to determine the *hLine* and *dwAddressID* parameters associated with the call; (b) the application must scan all known call handles to determine that the call is a new call; and (c) it is possible, under certain conditions, for the application to think it is receiving a new call handle when in reality it has just deallocated its handle to the call (for example, the application has just deallocated a call handle, but a [**LINE\_CALLSTATE**](line-callstate.md) message giving the application ownership of the call due to a [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) from another application was already in the application's TAPI message queue).</span></span>

## <a name="requirements"></a><span data-ttu-id="57c38-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57c38-126">Requirements</span></span>



| <span data-ttu-id="57c38-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57c38-127">Requirement</span></span> | <span data-ttu-id="57c38-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="57c38-128">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="57c38-129">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="57c38-129">TAPI version</span></span><br/> | <span data-ttu-id="57c38-130">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="57c38-130">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="57c38-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="57c38-131">Header</span></span><br/>       | <dl> <span data-ttu-id="57c38-132"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="57c38-132"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57c38-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57c38-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57c38-134">**CALLSTATE de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="57c38-134">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="57c38-135">**lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="57c38-135">**lineGetCallInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[<span data-ttu-id="57c38-136">**lineHandoff**</span><span class="sxs-lookup"><span data-stu-id="57c38-136">**lineHandoff**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




