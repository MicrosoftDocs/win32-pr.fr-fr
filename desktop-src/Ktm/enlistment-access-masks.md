---
description: KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture des enlistes.
ms.assetid: 93773eb7-141a-49f3-9306-ffbda2f4ab9f
title: Masques d’accès d’inscription (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63e4ebd67f93368215ebcdcd362595d0341adb52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524467"
---
# <a name="enlistment-access-masks"></a><span data-ttu-id="161df-103">Masques d’accès d’inscription</span><span class="sxs-lookup"><span data-stu-id="161df-103">Enlistment Access Masks</span></span>

<span data-ttu-id="161df-104">KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture des enlistes.</span><span class="sxs-lookup"><span data-stu-id="161df-104">KTM defines the following enlistment access masks to be used when opening enlistments.</span></span>

<dl> <dt>

<span data-ttu-id="161df-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**\_informations sur la requête d’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-105"><span id="ENLISTMENT_QUERY_INFORMATION"></span><span id="enlistment_query_information"></span>**ENLISTMENT\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="161df-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="161df-107">L’appelant peut interroger KTM pour obtenir des informations sur l’inscription.</span><span class="sxs-lookup"><span data-stu-id="161df-107">The caller can query KTM for information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**\_informations sur l’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-108"><span id="ENLISTMENT_SET_INFORMATION"></span><span id="enlistment_set_information"></span>**ENLISTMENT\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="161df-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="161df-110">L’appelant peut définir des informations sur l’inscription.</span><span class="sxs-lookup"><span data-stu-id="161df-110">The caller can set information about the enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**récupération de l’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-111"><span id="ENLISTMENT_RECOVER"></span><span id="enlistment_recover"></span>**ENLISTMENT\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="161df-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="161df-113">L’appelant peut récupérer une inscription.</span><span class="sxs-lookup"><span data-stu-id="161df-113">The caller can recover an enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**droits d’inscription \_ subordonnés \_**</span><span class="sxs-lookup"><span data-stu-id="161df-114"><span id="ENLISTMENT_SUBORDINATE_RIGHTS"></span><span id="enlistment_subordinate_rights"></span>**ENLISTMENT\_SUBORDINATE\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="161df-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="161df-116">L’appelant peut effectuer les actions effectuées par un gestionnaire de ressources pour le compte de la transaction.</span><span class="sxs-lookup"><span data-stu-id="161df-116">The caller can complete actions that a resource manager does on behalf of the transaction.</span></span> <span data-ttu-id="161df-117">Voici une liste d’actions :</span><span class="sxs-lookup"><span data-stu-id="161df-117">The following is a list of actions:</span></span>

-   [<span data-ttu-id="161df-118">**CommitComplete**</span><span class="sxs-lookup"><span data-stu-id="161df-118">**CommitComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [<span data-ttu-id="161df-119">**PrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="161df-119">**PrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [<span data-ttu-id="161df-120">**PrePrepareComplete**</span><span class="sxs-lookup"><span data-stu-id="161df-120">**PrePrepareComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)
-   [<span data-ttu-id="161df-121">**RollbackComplete**</span><span class="sxs-lookup"><span data-stu-id="161df-121">**RollbackComplete**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)
-   [<span data-ttu-id="161df-122">**ReadOnlyEnlistment**</span><span class="sxs-lookup"><span data-stu-id="161df-122">**ReadOnlyEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)
-   [<span data-ttu-id="161df-123">**RollbackEnlistment**</span><span class="sxs-lookup"><span data-stu-id="161df-123">**RollbackEnlistment**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   [<span data-ttu-id="161df-124">**SinglePhaseReject**</span><span class="sxs-lookup"><span data-stu-id="161df-124">**SinglePhaseReject**</span></span>](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**\_droits supérieurs d’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-125"><span id="ENLISTMENT_SUPERIOR_RIGHTS"></span><span id="enlistment_superior_rights"></span>**ENLISTMENT\_SUPERIOR\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-126">0x00010</span><span class="sxs-lookup"><span data-stu-id="161df-126">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="161df-127">L’appelant peut s’inscrire dans la transaction en tant que gestionnaire de transactions supérieur.</span><span class="sxs-lookup"><span data-stu-id="161df-127">The caller can enlist in the transaction as a superior transaction manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**\_lecture générique d’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-128"><span id="ENLISTMENT_GENERIC_READ"></span><span id="enlistment_generic_read"></span>**ENLISTMENT\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-129">0x20001</span><span class="sxs-lookup"><span data-stu-id="161df-129">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="161df-130">L’appelant dispose des privilèges suivants : **informations standard \_ \_ sur les requêtes** de **\_ \_ lecture** et d’inscription.</span><span class="sxs-lookup"><span data-stu-id="161df-130">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **ENLISTMENT\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**\_écriture générique d’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-131"><span id="ENLISTMENT_GENERIC_WRITE"></span><span id="enlistment_generic_write"></span>**ENLISTMENT\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-132">0x2001E</span><span class="sxs-lookup"><span data-stu-id="161df-132">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="161df-133">L’appelant dispose des privilèges suivants : **l' \_ \_ écriture des droits standard**, les **\_ \_ informations du jeu d’inscription** et la **\_ récupération** de l’inscription.</span><span class="sxs-lookup"><span data-stu-id="161df-133">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **ENLISTMENT\_SET\_INFORMATION**, and **ENLISTMENT\_RECOVER**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**\_Exécution générique d’inscription \_**</span><span class="sxs-lookup"><span data-stu-id="161df-134"><span id="ENLISTMENT_GENERIC_EXECUTE"></span><span id="enlistment_generic_execute"></span>**ENLISTMENT\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-135">0x2001C</span><span class="sxs-lookup"><span data-stu-id="161df-135">0x2001C</span></span>
</dt> <dt>



<span data-ttu-id="161df-136">L’appelant dispose des privilèges suivants : autorisations **standard, \_ \_ exécution** de **\_ récupération d’inscription** et **\_ \_ droits subordonnés d’inscription**.</span><span class="sxs-lookup"><span data-stu-id="161df-136">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **ENLISTMENT\_RECOVER**, and **ENLISTMENT\_SUBORDINATE\_RIGHTS**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="161df-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**INSCRIPTION de \_ tous les \_ accès**</span><span class="sxs-lookup"><span data-stu-id="161df-137"><span id="ENLISTMENT_ALL_ACCESS"></span><span id="enlistment_all_access"></span>**ENLISTMENT\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="161df-138">0xF001F</span><span class="sxs-lookup"><span data-stu-id="161df-138">0xF001F</span></span>
</dt> <dt>



<span data-ttu-id="161df-139">Cette valeur définit tous les bits valides pour une valeur d’accès d’inscription.</span><span class="sxs-lookup"><span data-stu-id="161df-139">This value sets all valid bits for an enlistment access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="161df-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="161df-140">Requirements</span></span>



| <span data-ttu-id="161df-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="161df-141">Requirement</span></span> | <span data-ttu-id="161df-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="161df-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="161df-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="161df-143">Minimum supported client</span></span><br/> | <span data-ttu-id="161df-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="161df-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="161df-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="161df-145">Minimum supported server</span></span><br/> | <span data-ttu-id="161df-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="161df-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="161df-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="161df-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="161df-148"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="161df-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




