---
title: Constantes TF_ES_ (msctf. h)
description: Les constantes suivantes sont utilisées par la méthode ITfContext RequestEditSession.
ms.assetid: 5498329f-3302-4f66-bdec-cab7db0cdc0e
topic_type:
- apiref
api_name:
- TF_ES_ASYNCDONTCARE
- TF_ES_SYNC
- TF_ES_READ
- TF_ES_READWRITE
- TF_ES_ASYNC
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa8ed96adc1d6f6d66671e91f7a70bce856663e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509548"
---
# <a name="tf_es_-constants"></a><span data-ttu-id="e19fe-103">\_ \_ \* Constantes TF es</span><span class="sxs-lookup"><span data-stu-id="e19fe-103">TF\_ES\_\* Constants</span></span>

<span data-ttu-id="e19fe-104">Les constantes suivantes sont utilisées par la méthode [ITfContext :: RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) .</span><span class="sxs-lookup"><span data-stu-id="e19fe-104">The following are constants used by the [ITfContext::RequestEditSession](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession) method.</span></span>



| <span data-ttu-id="e19fe-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="e19fe-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="e19fe-106">Description</span><span class="sxs-lookup"><span data-stu-id="e19fe-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                             |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_ES_ASYNCDONTCARE"></span><span id="tf_es_asyncdontcare"></span><dl> <span data-ttu-id="e19fe-107"><dt>**Tf \_ ES \_ ASYNCDONTCARE**</dt> <dt>(0)</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-107"><dt>**TF\_ES\_ASYNCDONTCARE**</dt> <dt>( 0 )</dt></span></span> </dl> | <span data-ttu-id="e19fe-108">La session d’édition peut se produire de façon synchrone ou asynchrone, à la discrétion du responsable.</span><span class="sxs-lookup"><span data-stu-id="e19fe-108">The edit session can occur synchronously or asynchronously, at the discretion of the manager.</span></span> <span data-ttu-id="e19fe-109">Le gestionnaire va tenter de planifier une session d’édition synchrone pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="e19fe-109">The manager will attempt to schedule a synchronous edit session for improved performance.</span></span> <span data-ttu-id="e19fe-110">Cette valeur ne peut pas être combinée avec les \_ valeurs de synchronisation TF es \_ Async ou TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="e19fe-110">This value cannot be combined with the TF\_ES\_ASYNC or TF\_ES\_SYNC values.</span></span><br/>                                                                         |
| <span id="TF_ES_SYNC"></span><span id="tf_es_sync"></span><dl> <span data-ttu-id="e19fe-111"><dt>**Tf \_ \_Synchronisation es**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-111"><dt>**TF\_ES\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                          | <span data-ttu-id="e19fe-112">La session d’édition doit être synchrone ou la demande échoue (avec TF \_ E \_ Synchronous).</span><span class="sxs-lookup"><span data-stu-id="e19fe-112">The edit session must be synchronous or the request will fail (with TF\_E\_SYNCHRONOUS).</span></span> <span data-ttu-id="e19fe-113">Cet indicateur doit être utilisé uniquement dans les situations documentées (telles que la gestion des séquences de touches) où il peut être attendu.</span><span class="sxs-lookup"><span data-stu-id="e19fe-113">This flag should only be used in documented situations (such as keystroke handling) where it can be expected to succeed.</span></span> <span data-ttu-id="e19fe-114">Dans le cas contraire, l’appel échouera probablement.</span><span class="sxs-lookup"><span data-stu-id="e19fe-114">Otherwise the call will likely fail.</span></span> <span data-ttu-id="e19fe-115">Cette valeur ne peut pas être combinée avec \_ les \_ valeurs ASYNCDONTCARE TF es ou TF \_ es \_ Async.</span><span class="sxs-lookup"><span data-stu-id="e19fe-115">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_ASYNC values.</span></span><br/> |
| <span id="TF_ES_READ"></span><span id="tf_es_read"></span><dl> <span data-ttu-id="e19fe-116"><dt>**Tf \_ ES \_ lus**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-116"><dt>**TF\_ES\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                          | <span data-ttu-id="e19fe-117">Demande l’accès en lecture seule au contexte.</span><span class="sxs-lookup"><span data-stu-id="e19fe-117">Requests read-only access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span id="TF_ES_READWRITE"></span><span id="tf_es_readwrite"></span><dl> <span data-ttu-id="e19fe-118"><dt>**Tf \_ ES \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-118"><dt>**TF\_ES\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl>           | <span data-ttu-id="e19fe-119">Demande l’accès en lecture/écriture au contexte.</span><span class="sxs-lookup"><span data-stu-id="e19fe-119">Requests read/write access to the context.</span></span><br/>                                                                                                                                                                                                                                                                                                   |
| <span id="TF_ES_ASYNC"></span><span id="tf_es_async"></span><dl> <span data-ttu-id="e19fe-120"><dt>**Tf \_ ES \_ Async**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-120"><dt>**TF\_ES\_ASYNC**</dt> <dt>( 0x8 )</dt></span></span> </dl>                       | <span data-ttu-id="e19fe-121">La session d’édition doit être asynchrone ou la demande échouera.</span><span class="sxs-lookup"><span data-stu-id="e19fe-121">The edit session must be asynchronous or the request will fail.</span></span> <span data-ttu-id="e19fe-122">Cette valeur ne peut pas être combinée avec les \_ valeurs de synchronisation TF es \_ ASYNCDONTCARE ou TF \_ es \_ .</span><span class="sxs-lookup"><span data-stu-id="e19fe-122">This value cannot be combined with the TF\_ES\_ASYNCDONTCARE or TF\_ES\_SYNC values.</span></span><br/>                                                                                                                                                                                         |



## <a name="requirements"></a><span data-ttu-id="e19fe-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e19fe-123">Requirements</span></span>



| <span data-ttu-id="e19fe-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e19fe-124">Requirement</span></span> | <span data-ttu-id="e19fe-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e19fe-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e19fe-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e19fe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e19fe-127">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e19fe-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e19fe-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e19fe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e19fe-129">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e19fe-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e19fe-130">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="e19fe-130">Redistributable</span></span><br/>          | <span data-ttu-id="e19fe-131">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="e19fe-131">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="e19fe-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="e19fe-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e19fe-133"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-133"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="e19fe-134">MIDL</span><span class="sxs-lookup"><span data-stu-id="e19fe-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e19fe-135"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e19fe-135"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e19fe-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e19fe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e19fe-137">ITfContext :: RequestEditSession</span><span class="sxs-lookup"><span data-stu-id="e19fe-137">ITfContext::RequestEditSession</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontext-requesteditsession)
</dt> </dl>

 

 





