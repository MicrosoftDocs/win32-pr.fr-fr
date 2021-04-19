---
description: Le \_ message de réponse de ligne TAPI est envoyé pour signaler les résultats des appels de fonction qui se sont terminés de façon asynchrone.
ms.assetid: 5d98ed8b-b75e-49f8-aba3-c6eee89e91c1
title: Message LINE_REPLY (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed963a777a5073b0182e809eec83fb7f904768e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542762"
---
# <a name="line_reply-message"></a><span data-ttu-id="00ee3-103">Message de réponse de ligne \_</span><span class="sxs-lookup"><span data-stu-id="00ee3-103">LINE\_REPLY message</span></span>

<span data-ttu-id="00ee3-104">Le message **de \_ réponse de ligne** TAPI est envoyé pour signaler les résultats des appels de fonction qui se sont terminés de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="00ee3-104">The TAPI **LINE\_REPLY** message is sent to report the results of function calls that completed asynchronously.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="00ee3-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00ee3-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00ee3-106">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="00ee3-106">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="00ee3-107">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="00ee3-107">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="00ee3-108">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="00ee3-108">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="00ee3-109">Retourne l’instance de rappel de l’application.</span><span class="sxs-lookup"><span data-stu-id="00ee3-109">Returns the application's callback instance.</span></span>

</dd> <dt>

<span data-ttu-id="00ee3-110">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="00ee3-110">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="00ee3-111">Identificateur de demande pour lequel il s’agit de la réponse.</span><span class="sxs-lookup"><span data-stu-id="00ee3-111">The request identifier for which this is the reply.</span></span>

</dd> <dt>

<span data-ttu-id="00ee3-112">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="00ee3-112">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="00ee3-113">Indication de réussite ou d’erreur.</span><span class="sxs-lookup"><span data-stu-id="00ee3-113">The success or error indication.</span></span> <span data-ttu-id="00ee3-114">L’application doit effectuer un cast de ce paramètre en LONG.</span><span class="sxs-lookup"><span data-stu-id="00ee3-114">The application should cast this parameter into a LONG.</span></span> <span data-ttu-id="00ee3-115">Zéro indique une réussite ; un nombre négatif indique une erreur.</span><span class="sxs-lookup"><span data-stu-id="00ee3-115">Zero indicates success; a negative number indicates an error.</span></span>

</dd> <dt>

<span data-ttu-id="00ee3-116">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="00ee3-116">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="00ee3-117">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="00ee3-117">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00ee3-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="00ee3-118">Return value</span></span>

<span data-ttu-id="00ee3-119">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="00ee3-119">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="00ee3-120">Notes</span><span class="sxs-lookup"><span data-stu-id="00ee3-120">Remarks</span></span>

<span data-ttu-id="00ee3-121">Les fonctions qui exécutent de façon asynchrone renvoient une valeur d’identificateur de demande positive à l’application.</span><span class="sxs-lookup"><span data-stu-id="00ee3-121">Functions that operate asynchronously return a positive request identifier value to the application.</span></span> <span data-ttu-id="00ee3-122">Cet identificateur de demande est retourné avec le message de réponse pour identifier la demande qui a été effectuée.</span><span class="sxs-lookup"><span data-stu-id="00ee3-122">This request identifier is returned with the reply message to identify the request that was completed.</span></span> <span data-ttu-id="00ee3-123">L’autre paramètre du message **de \_ réponse** à la ligne comporte l’indication de réussite ou d’échec.</span><span class="sxs-lookup"><span data-stu-id="00ee3-123">The other parameter for the **LINE\_REPLY** message carries the success or failure indication.</span></span> <span data-ttu-id="00ee3-124">Les erreurs possibles sont les mêmes que celles définies par la fonction correspondante.</span><span class="sxs-lookup"><span data-stu-id="00ee3-124">Possible errors are the same as those defined by the corresponding function.</span></span> <span data-ttu-id="00ee3-125">Ce message ne peut pas être désactivé.</span><span class="sxs-lookup"><span data-stu-id="00ee3-125">This message cannot be disabled.</span></span>

<span data-ttu-id="00ee3-126">Dans certains cas, une application peut ne pas recevoir le message de **\_ réponse de ligne** correspondant à un appel à une fonction asynchrone.</span><span class="sxs-lookup"><span data-stu-id="00ee3-126">In some cases, an application may fail to receive the **LINE\_REPLY** message corresponding to a call to an asynchronous function.</span></span> <span data-ttu-id="00ee3-127">Cela se produit si la poignée d’appel correspondante est désallouée avant la réception du message.</span><span class="sxs-lookup"><span data-stu-id="00ee3-127">This occurs if the corresponding call handle is deallocated before the message has been received.</span></span>

> [!Note]  
> <span data-ttu-id="00ee3-128">Lorsqu’une application appelle une opération asynchrone qui écrit des données dans la mémoire de l’application, l’application doit conserver cette mémoire disponible pour l’écriture jusqu’à la réception d’un message de **\_ réponse** de ligne ou de [**\_ GATHERDIGITS de ligne**](line-gatherdigits.md) .</span><span class="sxs-lookup"><span data-stu-id="00ee3-128">When an application invokes any asynchronous operation that writes data back into application memory, the application must keep that memory available for writing until a **LINE\_REPLY** or [**LINE\_GATHERDIGITS**](line-gatherdigits.md) message is received.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="00ee3-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00ee3-129">Requirements</span></span>



| <span data-ttu-id="00ee3-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00ee3-130">Requirement</span></span> | <span data-ttu-id="00ee3-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="00ee3-131">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="00ee3-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="00ee3-132">TAPI version</span></span><br/> | <span data-ttu-id="00ee3-133">Nécessite TAPI 2,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="00ee3-133">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="00ee3-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="00ee3-134">Header</span></span><br/>       | <dl> <span data-ttu-id="00ee3-135"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="00ee3-135"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00ee3-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00ee3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00ee3-137">**GATHERDIGITS de ligne \_**</span><span class="sxs-lookup"><span data-stu-id="00ee3-137">**LINE\_GATHERDIGITS**</span></span>](line-gatherdigits.md)
</dt> </dl>

 

 




