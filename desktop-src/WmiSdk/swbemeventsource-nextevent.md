---
description: Si un événement est disponible, la méthode NextEvent de l’objet SWbemEventSource récupère l’événement à partir d’une requête d’événement.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Méthode SWbemEventSource. NextEvent (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519554"
---
# <a name="swbemeventsourcenextevent-method"></a><span data-ttu-id="7834f-103">Méthode SWbemEventSource. NextEvent</span><span class="sxs-lookup"><span data-stu-id="7834f-103">SWbemEventSource.NextEvent method</span></span>

<span data-ttu-id="7834f-104">Si un événement est disponible, la méthode **NextEvent** de l’objet [**SWbemEventSource**](swbemeventsource.md) récupère l’événement à partir d’une requête d’événement.</span><span class="sxs-lookup"><span data-stu-id="7834f-104">If an event is available, the **NextEvent** method of the [**SWbemEventSource**](swbemeventsource.md) object retrieves the event from an event query.</span></span>

<span data-ttu-id="7834f-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7834f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7834f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7834f-106">Syntax</span></span>


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7834f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7834f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7834f-108">*iTimeoutMs* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7834f-108">*iTimeoutMs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7834f-109">Nombre de millisecondes pendant lesquelles l’appel attend un événement avant de retourner une erreur de délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="7834f-109">Number of milliseconds the call waits for an event before returning a time-out error.</span></span> <span data-ttu-id="7834f-110">La valeur par défaut de ce paramètre est **wbemTimeoutInfinite** (-1), qui indique à l’appel d’attendre indéfiniment.</span><span class="sxs-lookup"><span data-stu-id="7834f-110">The default value for this parameter is **wbemTimeoutInfinite** (-1), which directs the call to wait indefinitely.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7834f-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7834f-111">Return value</span></span>

<span data-ttu-id="7834f-112">Si la méthode **NextEvent** réussit, elle retourne un objet [**SWbemObject**](swbemobject.md) qui contient l’événement demandé.</span><span class="sxs-lookup"><span data-stu-id="7834f-112">If the **NextEvent** method is successful, it returns an [**SWbemObject**](swbemobject.md) object that contains the requested event.</span></span> <span data-ttu-id="7834f-113">Si l’appel expire, l’objet retourné est **null** et une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="7834f-113">If the call times out, the returned object is **NULL** and an error is raised.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7834f-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7834f-114">Error codes</span></span>

<span data-ttu-id="7834f-115">À la fin de la méthode **NextEvent** , l’objet **Err** peut contenir le code d’erreur figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="7834f-115">Upon the completion of the **NextEvent** method, the **Err** object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7834f-116">**wbemErrTimedOut** -0x80043001</span><span class="sxs-lookup"><span data-stu-id="7834f-116">**wbemErrTimedOut** - 0x80043001</span></span>
</dt> <dd>

<span data-ttu-id="7834f-117">L’événement demandé n’est pas arrivé dans le laps de temps spécifié dans *iTimeoutMs.*</span><span class="sxs-lookup"><span data-stu-id="7834f-117">Requested event did not arrive in the amount of time specified in *iTimeoutMs.*</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7834f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7834f-118">Requirements</span></span>



| <span data-ttu-id="7834f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7834f-119">Requirement</span></span> | <span data-ttu-id="7834f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="7834f-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7834f-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7834f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7834f-122">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7834f-122">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7834f-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7834f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7834f-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7834f-124">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7834f-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7834f-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7834f-126"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7834f-126"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7834f-127">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7834f-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="7834f-128"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7834f-128"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7834f-129">DLL</span><span class="sxs-lookup"><span data-stu-id="7834f-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7834f-130"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7834f-130"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7834f-131">CLSID</span><span class="sxs-lookup"><span data-stu-id="7834f-131">CLSID</span></span><br/>                    | <span data-ttu-id="7834f-132">CLSID \_ SWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="7834f-132">CLSID\_SWbemEventSource</span></span><br/>                                                      |
| <span data-ttu-id="7834f-133">IID</span><span class="sxs-lookup"><span data-stu-id="7834f-133">IID</span></span><br/>                      | <span data-ttu-id="7834f-134">IID \_ ISWbemEventSource</span><span class="sxs-lookup"><span data-stu-id="7834f-134">IID\_ISWbemEventSource</span></span><br/>                                                       |



 

 




