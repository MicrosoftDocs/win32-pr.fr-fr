---
title: XTYP_CONNECT transaction (Ddeml. h)
description: Un client utilise la \_ transaction XTYP Connect pour établir une conversation.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Échange de données de transaction XTYP_CONNECT
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104077"
---
# <a name="xtyp_connect-transaction"></a><span data-ttu-id="2f754-104">\_Transaction XTYP Connect</span><span class="sxs-lookup"><span data-stu-id="2f754-104">XTYP\_CONNECT transaction</span></span>

<span data-ttu-id="2f754-105">Un client utilise la transaction **XTYP \_ Connect** pour établir une conversation.</span><span class="sxs-lookup"><span data-stu-id="2f754-105">A client uses the **XTYP\_CONNECT** transaction to establish a conversation.</span></span> <span data-ttu-id="2f754-106">Une fonction de rappel de serveur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction lorsqu’un client spécifie un nom de service que le serveur prend en charge (et un nom de rubrique qui n’a pas la **valeur null**) dans un appel à la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .</span><span class="sxs-lookup"><span data-stu-id="2f754-106">A Dynamic Data Exchange (DDE) server callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives this transaction when a client specifies a service name that the server supports (and a topic name that is not **NULL**) in a call to the [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) function.</span></span>


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="2f754-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2f754-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f754-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="2f754-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-109">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="2f754-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="2f754-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2f754-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="2f754-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2f754-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="2f754-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-115">Handle vers le nom de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="2f754-115">A handle to the topic name.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="2f754-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-117">Handle vers le nom du service.</span><span class="sxs-lookup"><span data-stu-id="2f754-117">A handle to the service name.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="2f754-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-119">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="2f754-119">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-120">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="2f754-120">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-121">Pointeur vers une structure [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) qui contient des informations de contexte pour la conversation.</span><span class="sxs-lookup"><span data-stu-id="2f754-121">A pointer to a [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) structure that contains context information for the conversation.</span></span> <span data-ttu-id="2f754-122">Si le client n’est pas une application DDEML, ce paramètre est 0.</span><span class="sxs-lookup"><span data-stu-id="2f754-122">If the client is not a DDEML application, this parameter is 0.</span></span>

</dd> <dt>

<span data-ttu-id="2f754-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="2f754-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="2f754-124">Spécifie si le client est la même instance d’application que le serveur.</span><span class="sxs-lookup"><span data-stu-id="2f754-124">Specifies whether the client is the same application instance as the server.</span></span> <span data-ttu-id="2f754-125">Si le paramètre est égal à 1, le client est la même instance.</span><span class="sxs-lookup"><span data-stu-id="2f754-125">If the parameter is 1, the client is the same instance.</span></span> <span data-ttu-id="2f754-126">Si le paramètre a la valeur 0, le client est une instance différente.</span><span class="sxs-lookup"><span data-stu-id="2f754-126">If the parameter is 0, the client is a different instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f754-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2f754-127">Return value</span></span>

<span data-ttu-id="2f754-128">Une fonction de rappel de serveur doit retourner la **valeur true** pour permettre au client d’établir une conversation sur la paire de noms de services et de rubriques spécifiée, ou la fonction doit retourner **false** pour refuser la conversation.</span><span class="sxs-lookup"><span data-stu-id="2f754-128">A server callback function should return **TRUE** to allow the client to establish a conversation on the specified service name and topic name pair, or the function should return **FALSE** to deny the conversation.</span></span> <span data-ttu-id="2f754-129">Si la fonction de rappel retourne la **valeur true** et qu’une conversation est correctement établie, le système transmet le descripteur de conversation au serveur en émettant une transaction [**\_ \_ Confirm XTYP Connect**](xtyp-connect-confirm.md) à la fonction de rappel du serveur (à moins que le serveur n’ait spécifié l’indicateur **CBF \_ Skip \_ Connect \_ Confirm** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).</span><span class="sxs-lookup"><span data-stu-id="2f754-129">If the callback function returns **TRUE** and a conversation is successfully established, the system passes the conversation handle to the server by issuing an [**XTYP\_CONNECT\_CONFIRM**](xtyp-connect-confirm.md) transaction to the server's callback function (unless the server specified the **CBF\_SKIP\_CONNECT\_CONFIRMS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function).</span></span>

## <a name="remarks"></a><span data-ttu-id="2f754-130">Notes</span><span class="sxs-lookup"><span data-stu-id="2f754-130">Remarks</span></span>

<span data-ttu-id="2f754-131">Cette transaction est filtrée si l’application serveur a spécifié l’indicateur **CBF \_ Fail \_ connections** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="2f754-131">This transaction is filtered if the server application specified the **CBF\_FAIL\_CONNECTIONS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="2f754-132">Un serveur ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="2f754-132">A server cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f754-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2f754-133">Requirements</span></span>



| <span data-ttu-id="2f754-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2f754-134">Requirement</span></span> | <span data-ttu-id="2f754-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="2f754-135">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f754-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f754-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f754-137">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f754-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="2f754-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2f754-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f754-139">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2f754-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="2f754-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="2f754-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f754-141"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f754-141"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f754-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2f754-142">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f754-143">**Référence**</span><span class="sxs-lookup"><span data-stu-id="2f754-143">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f754-144">**CONVCONTEXT**</span><span class="sxs-lookup"><span data-stu-id="2f754-144">**CONVCONTEXT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[<span data-ttu-id="2f754-145">**DdeConnect**</span><span class="sxs-lookup"><span data-stu-id="2f754-145">**DdeConnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[<span data-ttu-id="2f754-146">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="2f754-146">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

<span data-ttu-id="2f754-147">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="2f754-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f754-148">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="2f754-148">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

