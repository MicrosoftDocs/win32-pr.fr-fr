---
title: XTYP_MONITOR transaction (Ddeml. h)
description: Une fonction de rappel DDE du débogueur échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction XTYP Monitor à chaque fois qu’un événement DDE se produit dans le système.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- Échange de données de transaction XTYP_MONITOR
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384435"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="3ff32-104">XTYP \_ surveiller la transaction</span><span class="sxs-lookup"><span data-stu-id="3ff32-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="3ff32-105">Une fonction de rappel DDE du débogueur échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ Monitor** à chaque fois qu’un événement DDE se produit dans le système.</span><span class="sxs-lookup"><span data-stu-id="3ff32-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="3ff32-106">Pour recevoir cette transaction, une application doit spécifier la valeur du **\_ moniteur APPCLASS** quand elle appelle la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .</span><span class="sxs-lookup"><span data-stu-id="3ff32-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="3ff32-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3ff32-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ff32-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="3ff32-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-109">Type de transaction.</span><span class="sxs-lookup"><span data-stu-id="3ff32-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-110">*uFmt*</span><span class="sxs-lookup"><span data-stu-id="3ff32-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ff32-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-112">*hconv*</span><span class="sxs-lookup"><span data-stu-id="3ff32-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ff32-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="3ff32-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-115">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ff32-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="3ff32-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-117">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ff32-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="3ff32-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-119">Handle d’un objet DDE qui contient des informations sur l’événement DDE.</span><span class="sxs-lookup"><span data-stu-id="3ff32-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="3ff32-120">L’application doit utiliser la fonction [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) pour obtenir un pointeur vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="3ff32-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="3ff32-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-122">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="3ff32-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ff32-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="3ff32-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="3ff32-124">Événement DDE.</span><span class="sxs-lookup"><span data-stu-id="3ff32-124">The DDE event.</span></span> <span data-ttu-id="3ff32-125">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ff32-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="3ff32-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ff32-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="3ff32-127">Signification</span><span class="sxs-lookup"><span data-stu-id="3ff32-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="3ff32-128"><dt>**MF \_ RAPPELs**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="3ff32-129">Le système a envoyé une transaction à une fonction de rappel DDE.</span><span class="sxs-lookup"><span data-stu-id="3ff32-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="3ff32-130">L’objet DDE contient une structure [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) qui fournit des informations sur la transaction.</span><span class="sxs-lookup"><span data-stu-id="3ff32-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="3ff32-131"><dt>**MF \_ CONV**</dt> <dt>0x40000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="3ff32-132">Une conversation DDE a été établie ou terminée.</span><span class="sxs-lookup"><span data-stu-id="3ff32-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="3ff32-133">L’objet DDE contient une structure [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) qui fournit des informations sur la conversation.</span><span class="sxs-lookup"><span data-stu-id="3ff32-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="3ff32-134"><dt>**MF \_ Erreurs**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="3ff32-135">Une erreur DDE s’est produite.</span><span class="sxs-lookup"><span data-stu-id="3ff32-135">A DDE error occurred.</span></span> <span data-ttu-id="3ff32-136">L’objet DDE contient une structure [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) qui fournit des informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="3ff32-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="3ff32-137"><dt>**MF \_ HSZ \_ info**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="3ff32-138">Une application DDE a créé, libérée ou incrémentée le nombre d’utilisations d’un handle de chaîne, ou un descripteur de chaîne a été libéré à la suite d’un appel à la fonction [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .</span><span class="sxs-lookup"><span data-stu-id="3ff32-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="3ff32-139">L’objet DDE contient une structure [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) qui fournit des informations sur le handle de chaîne.</span><span class="sxs-lookup"><span data-stu-id="3ff32-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="3ff32-140"><dt>**MF \_ Liens**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="3ff32-141">Une application DDE a démarré ou arrêté une boucle de notification.</span><span class="sxs-lookup"><span data-stu-id="3ff32-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="3ff32-142">L’objet DDE contient une structure [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) qui fournit des informations sur la boucle de notification.</span><span class="sxs-lookup"><span data-stu-id="3ff32-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="3ff32-143"><dt>**MF \_ POSTMSGS**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="3ff32-144">Le système ou une application a publié un message DDE.</span><span class="sxs-lookup"><span data-stu-id="3ff32-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="3ff32-145">L’objet DDE contient une structure [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) qui fournit des informations sur le message.</span><span class="sxs-lookup"><span data-stu-id="3ff32-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="3ff32-146"><dt>**MF \_ SENDMSGS**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="3ff32-147">Le système ou une application a envoyé un message DDE.</span><span class="sxs-lookup"><span data-stu-id="3ff32-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="3ff32-148">L’objet DDE contient une structure [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) qui fournit des informations sur le message.</span><span class="sxs-lookup"><span data-stu-id="3ff32-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ff32-149">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3ff32-149">Return value</span></span>

<span data-ttu-id="3ff32-150">Si la fonction de rappel traite cette transaction, elle doit retourner 0.</span><span class="sxs-lookup"><span data-stu-id="3ff32-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ff32-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ff32-151">Requirements</span></span>



| <span data-ttu-id="3ff32-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ff32-152">Requirement</span></span> | <span data-ttu-id="3ff32-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ff32-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ff32-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ff32-154">Minimum supported client</span></span><br/> | <span data-ttu-id="3ff32-155">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ff32-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3ff32-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ff32-156">Minimum supported server</span></span><br/> | <span data-ttu-id="3ff32-157">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ff32-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="3ff32-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ff32-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ff32-159"><dt>Ddeml. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ff32-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ff32-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ff32-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="3ff32-161">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3ff32-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3ff32-162">**DdeAccessData**</span><span class="sxs-lookup"><span data-stu-id="3ff32-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="3ff32-163">**DdeInitialize**</span><span class="sxs-lookup"><span data-stu-id="3ff32-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="3ff32-164">**DdeUninitialize**</span><span class="sxs-lookup"><span data-stu-id="3ff32-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="3ff32-165">**MONCBSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3ff32-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="3ff32-166">**MONCONVSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3ff32-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="3ff32-167">**MONERRSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3ff32-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="3ff32-168">**MONHSZSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3ff32-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="3ff32-169">**MONLINKSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3ff32-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="3ff32-170">**MONMSGSTRUCT**</span><span class="sxs-lookup"><span data-stu-id="3ff32-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="3ff32-171">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3ff32-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ff32-172">Bibliothèque de gestion des échange dynamique de données</span><span class="sxs-lookup"><span data-stu-id="3ff32-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

