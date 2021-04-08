---
title: XTYP_DISCONNECT transaction (Ddeml. h)
description: La fonction de rappel échange dynamique de données (DDE) d’une application, DdeCallback, reçoit la \_ transaction de déconnexion XTYP lorsque le partenaire de l’application dans une conversation utilise la fonction DdeDisconnect pour mettre fin à la conversation.
ms.assetid: 22a9ec63-8a74-4829-ad02-d07dd0e8fa9b
keywords:
- Échange de données de transaction XTYP_DISCONNECT
topic_type:
- apiref
api_name:
- XTYP_DISCONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e73bc0446989ac572a27f394e594924573711d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740332"
---
# <a name="xtyp_disconnect-transaction"></a><span data-ttu-id="c5b17-104">XTYP \_ déconnecter la transaction</span><span class="sxs-lookup"><span data-stu-id="c5b17-104">XTYP\_DISCONNECT transaction</span></span>

<span data-ttu-id="c5b17-105">La fonction de rappel échange dynamique de données (DDE) d’une application, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction de **\_ déconnexion XTYP** lorsque le partenaire de l’application dans une conversation utilise la fonction [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) pour mettre fin à la conversation.</span><span class="sxs-lookup"><span data-stu-id="c5b17-105">An application's Dynamic Data Exchange (DDE) callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_DISCONNECT** transaction when the application's partner in a conversation uses the [**DdeDisconnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect) function to terminate the conversation.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_DISCONNECT         (0x00C0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="c5b17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c5b17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5b17-107">*uType*</span><span class="sxs-lookup"><span data-stu-id="c5b17-107">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-108">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="c5b17-108">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-109">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="c5b17-109">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-110">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5b17-110">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-111">*hconv*</span><span class="sxs-lookup"><span data-stu-id="c5b17-111">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-112">Handle vers la fin de la conversation.</span><span class="sxs-lookup"><span data-stu-id="c5b17-112">A handle to that the conversation was terminated.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-113">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="c5b17-113">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-114">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5b17-114">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-115">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="c5b17-115">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-116">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5b17-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-117">*hdata*</span><span class="sxs-lookup"><span data-stu-id="c5b17-117">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-118">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5b17-118">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-119">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="c5b17-119">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-120">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="c5b17-120">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="c5b17-121">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="c5b17-121">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="c5b17-122">Spécifie si les partenaires de la conversation sont la même instance d’application.</span><span class="sxs-lookup"><span data-stu-id="c5b17-122">Specifies whether the partners in the conversation are the same application instance.</span></span> <span data-ttu-id="c5b17-123">Si ce paramètre est égal à 1, les partenaires sont la même instance.</span><span class="sxs-lookup"><span data-stu-id="c5b17-123">If this parameter is 1, the partners are the same instance.</span></span> <span data-ttu-id="c5b17-124">Si ce paramètre a la valeur 0, les partenaires sont des instances différentes.</span><span class="sxs-lookup"><span data-stu-id="c5b17-124">If this parameter is 0, the partners are different instances.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5b17-125">Notes</span><span class="sxs-lookup"><span data-stu-id="c5b17-125">Remarks</span></span>

<span data-ttu-id="c5b17-126">Cette transaction est filtrée si l’application a spécifié l’indicateur **CBF \_ Skip \_ deconnections** dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="c5b17-126">This transaction is filtered if the application specified the **CBF\_SKIP\_DISCONNECTS** flag in the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>

<span data-ttu-id="c5b17-127">L’application peut obtenir l’état de la conversation terminée en appelant la fonction [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) lors du traitement de cette transaction.</span><span class="sxs-lookup"><span data-stu-id="c5b17-127">The application can obtain the status of the terminated conversation by calling the [**DdeQueryConvInfo**](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo) function while processing this transaction.</span></span> <span data-ttu-id="c5b17-128">Le descripteur de conversation devient non valide après le retour de la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="c5b17-128">The conversation handle becomes invalid after the callback function returns.</span></span>

<span data-ttu-id="c5b17-129">Une application ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.</span><span class="sxs-lookup"><span data-stu-id="c5b17-129">An application cannot block this transaction type; the **CBR\_BLOCK** return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5b17-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c5b17-130">Requirements</span></span>



| <span data-ttu-id="c5b17-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c5b17-131">Requirement</span></span> | <span data-ttu-id="c5b17-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="c5b17-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5b17-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5b17-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c5b17-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5b17-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c5b17-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c5b17-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c5b17-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c5b17-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="c5b17-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c5b17-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5b17-138"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5b17-138"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5b17-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b17-139">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5b17-140">**Référence**</span><span class="sxs-lookup"><span data-stu-id="c5b17-140">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="c5b17-141">**DdeDisconnect**</span><span class="sxs-lookup"><span data-stu-id="c5b17-141">**DdeDisconnect**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddedisconnect)
</dt> <dt>

[<span data-ttu-id="c5b17-142">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="c5b17-142">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="c5b17-143">**DdeQueryConvInfo**</span><span class="sxs-lookup"><span data-stu-id="c5b17-143">**DdeQueryConvInfo**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddequeryconvinfo)
</dt> <dt>

<span data-ttu-id="c5b17-144">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c5b17-144">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c5b17-145">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="c5b17-145">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

