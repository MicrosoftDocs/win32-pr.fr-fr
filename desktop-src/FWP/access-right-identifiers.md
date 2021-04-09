---
title: Identificateurs des droits d’accès (Fwpmu. h)
description: La plateforme de filtrage Windows (WFP) utilise les droits d’accès Win32 standard, ainsi qu’un ensemble de droits d’accès spécifiques à WFP intégrés à la plateforme de filtrage.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af182a087ade590e278bd3dd1d2bb1a64b5c598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942799"
---
# <a name="access-right-identifiers"></a><span data-ttu-id="8deaf-103">Identificateurs des droits d’accès</span><span class="sxs-lookup"><span data-stu-id="8deaf-103">Access Right Identifiers</span></span>

<span data-ttu-id="8deaf-104">La plateforme de filtrage Windows (WFP) utilise les [droits d’accès Win32 standard](/windows/desktop/SecAuthZ/standard-access-rights) , ainsi qu’un ensemble de droits d’accès spécifiques à WFP intégrés à la plateforme de filtrage.</span><span class="sxs-lookup"><span data-stu-id="8deaf-104">Windows Filtering Platform (WFP) uses the [standard Win32 access rights](/windows/desktop/SecAuthZ/standard-access-rights) plus a set of WFP-specific access rights built into the filtering platform.</span></span> <span data-ttu-id="8deaf-105">Ces droits d’accès sont utilisés pour sécuriser les objets en mode utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="8deaf-105">These access rights are used to secure objects in user mode only.</span></span> <span data-ttu-id="8deaf-106">Les appelants en mode noyau contournent toutes les vérifications d’accès.</span><span class="sxs-lookup"><span data-stu-id="8deaf-106">Kernel-mode callers bypass all access checks.</span></span>

<span data-ttu-id="8deaf-107">Les identificateurs de droits d’accès spécifiques à WFP sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="8deaf-107">WFP specific access right identifiers are as follows.</span></span>

<dl> <dt>

<span data-ttu-id="8deaf-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**</span><span class="sxs-lookup"><span data-stu-id="8deaf-108"><span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM\_ACTRL\_ADD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-109">Ajoutez un objet au moteur de filtrage de base (BFE).</span><span class="sxs-lookup"><span data-stu-id="8deaf-109">Add an object to the Base Filtering Engine (BFE).</span></span> <span data-ttu-id="8deaf-110">Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .</span><span class="sxs-lookup"><span data-stu-id="8deaf-110">This access right is needed in order to call [**Fwpm\*Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Ajouter un \_ lien**</span><span class="sxs-lookup"><span data-stu-id="8deaf-111"><span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM\_ACTRL\_ADD\_LINK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-112">Ajoutez un objet référencé via un lien.</span><span class="sxs-lookup"><span data-stu-id="8deaf-112">Add an object referenced through a link.</span></span> <span data-ttu-id="8deaf-113">Par exemple, ce droit d’accès est nécessaire pour les légendes référencées par le biais de GUID.</span><span class="sxs-lookup"><span data-stu-id="8deaf-113">For example, this access right is needed for callouts referenced through GUIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="8deaf-114"><span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM\_ACTRL\_BEGIN\_READ\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-115">Commencez une transaction en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8deaf-115">Begin a read-only transaction.</span></span> <span data-ttu-id="8deaf-116">Ce droit d’accès est nécessaire pour appeler [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span><span class="sxs-lookup"><span data-stu-id="8deaf-116">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**</span><span class="sxs-lookup"><span data-stu-id="8deaf-117"><span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM\_ACTRL\_BEGIN\_WRITE\_TXN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-118">Commencer une transaction en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8deaf-118">Begin a read/write transaction.</span></span> <span data-ttu-id="8deaf-119">Ce droit d’accès est nécessaire pour appeler [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) pour une transaction en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="8deaf-119">This access right is needed in order to call [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) for a read/write transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classification FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="8deaf-120"><span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**FWPM\_ACTRL\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-121">Classer l’appel de procédure distante (RPC).</span><span class="sxs-lookup"><span data-stu-id="8deaf-121">Classify Remote Procedure Call (RPC).</span></span> <span data-ttu-id="8deaf-122">Ce droit d’accès est requis par le runtime RPC afin d’appliquer les filtres RPC.</span><span class="sxs-lookup"><span data-stu-id="8deaf-122">This access right is needed by the RPC run-time in order to enforce RPC filters.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL, \_ énumération**</span><span class="sxs-lookup"><span data-stu-id="8deaf-123"><span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM\_ACTRL\_ENUM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-124">Énumérer.</span><span class="sxs-lookup"><span data-stu-id="8deaf-124">Enumerate.</span></span> <span data-ttu-id="8deaf-125">Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) .</span><span class="sxs-lookup"><span data-stu-id="8deaf-125">This access right is needed in order to call [**Fwpm\*CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) functions.</span></span> <span data-ttu-id="8deaf-126">Pour énumérer un objet, l’appelant a également besoin \_ \_ d’un accès en lecture FWPM ACTRL à l’objet.</span><span class="sxs-lookup"><span data-stu-id="8deaf-126">To enumerate an object, the caller also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**</span><span class="sxs-lookup"><span data-stu-id="8deaf-127"><span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM\_ACTRL\_OPEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-128">Ouvrez une session sur le moteur de filtre.</span><span class="sxs-lookup"><span data-stu-id="8deaf-128">Open a session to the filter engine.</span></span> <span data-ttu-id="8deaf-129">Ce droit d’accès est nécessaire pour appeler [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span><span class="sxs-lookup"><span data-stu-id="8deaf-129">This access right is needed in order to call [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lecture**</span><span class="sxs-lookup"><span data-stu-id="8deaf-130"><span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM\_ACTRL\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-131">Lecture.</span><span class="sxs-lookup"><span data-stu-id="8deaf-131">Read.</span></span> <span data-ttu-id="8deaf-132">Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) et [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .</span><span class="sxs-lookup"><span data-stu-id="8deaf-132">This access right is needed in order to call [**Fwpm\*GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) and [**Fwpm\*GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) functions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_statistiques de \_ lecture FWPM ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="8deaf-133"><span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**FWPM\_ACTRL\_READ\_STATS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-134">Lire les statistiques.</span><span class="sxs-lookup"><span data-stu-id="8deaf-134">Read statistics.</span></span> <span data-ttu-id="8deaf-135">Ce droit d’accès est nécessaire pour appeler [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) et [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span><span class="sxs-lookup"><span data-stu-id="8deaf-135">This access right is needed in order to call [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) and [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**abonnement à FWPM \_ ACTRL \_**</span><span class="sxs-lookup"><span data-stu-id="8deaf-136"><span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**FWPM\_ACTRL\_SUBSCRIBE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-137">Abonnez-vous.</span><span class="sxs-lookup"><span data-stu-id="8deaf-137">Subscribe.</span></span> <span data-ttu-id="8deaf-138">Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) .</span><span class="sxs-lookup"><span data-stu-id="8deaf-138">This access right is needed in order to call [**Fwpm\*SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) functions.</span></span> <span data-ttu-id="8deaf-139">Pour recevoir une notification pour un objet, un abonné a également besoin d’un \_ \_ accès en lecture FWPM ACTRL à l’objet.</span><span class="sxs-lookup"><span data-stu-id="8deaf-139">To receive a notification for an object, a subscriber also needs FWPM\_ACTRL\_READ access to the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**</span><span class="sxs-lookup"><span data-stu-id="8deaf-140"><span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM\_ACTRL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-141">Options du moteur d’écriture.</span><span class="sxs-lookup"><span data-stu-id="8deaf-141">Write engine options.</span></span> <span data-ttu-id="8deaf-142">Ce droit d’accès est nécessaire pour appeler [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span><span class="sxs-lookup"><span data-stu-id="8deaf-142">This access right is needed in order to call [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_lecture générique \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="8deaf-143"><span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**FWPM\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-144">\_droits standard \_ lire \| FWPM \_ ACTRL \_ Démarrer \_ lire \_ TXN \| FWPM \_ ACTRL \_ classer \| FWPM \_ ACTRL \_ ouvrir \| FWPM \_ ACTRL \_ lire \| FWPM ACTRL \_ lire les \_ \_ statistiques</span><span class="sxs-lookup"><span data-stu-id="8deaf-144">STANDARD\_RIGHTS\_READ \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_Exécution générique \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="8deaf-145"><span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**FWPM\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-146">\_droits standard \_ exécuter \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ subscribe</span><span class="sxs-lookup"><span data-stu-id="8deaf-146">STANDARD\_RIGHTS\_EXECUTE \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_SUBSCRIBE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_écriture générique \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="8deaf-147"><span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**FWPM\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-148">droits d’écriture de la \_ \_ \| suppression \| FWPM \_ ACTRL \_ Add \| FWPM \_ ACTRL \_ Ajouter un \_ lien \| FWPM \_ ACTRL \_ commencer l' \_ écriture TXN FWPM \_ \| \_ ACTRL \_ écrire</span><span class="sxs-lookup"><span data-stu-id="8deaf-148">STANDARD\_RIGHTS\_WRITE \| DELETE \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="8deaf-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ générique \_ tout**</span><span class="sxs-lookup"><span data-stu-id="8deaf-149"><span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM\_GENERIC\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8deaf-150">\_droits standard \_ requis \| FWPM \_ ACTRL \_ Add \| FWPM \_ ACTRL \_ Add \_ Link \| FWPM \_ ACTRL \_ Begin \_ Read \_ TXN FWPM ACTRL \| \_ \_ Begin \_ Write \_ TXN \| FWPM \_ ACTRL \_ classifie FWPM \| \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ lecture FWPM ACTRL lire les \| \_ \_ \_ statistiques \| FWPM \_ ACTRL \_ s’abonner FWPM \| \_ ACTRL \_ Write</span><span class="sxs-lookup"><span data-stu-id="8deaf-150">STANDARD\_RIGHTS\_REQUIRED \| FWPM\_ACTRL\_ADD \| FWPM\_ACTRL\_ADD\_LINK \| FWPM\_ACTRL\_BEGIN\_READ\_TXN \| FWPM\_ACTRL\_BEGIN\_WRITE\_TXN \| FWPM\_ACTRL\_CLASSIFY \| FWPM\_ACTRL\_ENUM \| FWPM\_ACTRL\_OPEN \| FWPM\_ACTRL\_READ \| FWPM\_ACTRL\_READ\_STATS \| FWPM\_ACTRL\_SUBSCRIBE \| FWPM\_ACTRL\_WRITE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8deaf-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8deaf-151">Requirements</span></span>



| <span data-ttu-id="8deaf-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8deaf-152">Requirement</span></span> | <span data-ttu-id="8deaf-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="8deaf-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8deaf-154">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8deaf-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8deaf-155">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8deaf-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8deaf-156">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8deaf-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8deaf-157">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8deaf-157">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8deaf-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="8deaf-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="8deaf-159"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="8deaf-159"><dt>Fwpmu.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8deaf-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8deaf-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8deaf-161">Modèle de Access Control de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="8deaf-161">Windows Filtering Platform Access Control Model</span></span>](access-control.md)
</dt> <dt>

[<span data-ttu-id="8deaf-162">Droits d’accès standard</span><span class="sxs-lookup"><span data-stu-id="8deaf-162">Standard Access Rights</span></span>](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

