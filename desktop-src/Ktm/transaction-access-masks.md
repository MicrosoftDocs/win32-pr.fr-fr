---
description: KTM définit les masques d’accès aux transactions suivants à utiliser lors de l’ouverture d’une transaction.
ms.assetid: 93ef3098-b3cc-4b24-ae82-1c10d937f14f
title: Masques d’accès aux transactions (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b815bcb04a97dbd059c85c6c615a7d607bf77ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518656"
---
# <a name="transaction-access-masks"></a><span data-ttu-id="08264-103">Masques d’accès aux transactions</span><span class="sxs-lookup"><span data-stu-id="08264-103">Transaction Access Masks</span></span>

<span data-ttu-id="08264-104">KTM définit les masques d’accès aux transactions suivants à utiliser lors de l’ouverture d’une transaction.</span><span class="sxs-lookup"><span data-stu-id="08264-104">KTM defines the following transaction access masks to be used when opening a transaction.</span></span>

<dl> <dt>

<span data-ttu-id="08264-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**\_informations sur les requêtes de transaction \_**</span><span class="sxs-lookup"><span data-stu-id="08264-105"><span id="TRANSACTION_QUERY_INFORMATION"></span><span id="transaction_query_information"></span>**TRANSACTION\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-106">0x000001</span><span class="sxs-lookup"><span data-stu-id="08264-106">0x000001</span></span>
</dt> <dt>



<span data-ttu-id="08264-107">L’appelant peut interroger les informations de transaction.</span><span class="sxs-lookup"><span data-stu-id="08264-107">The caller can query transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**\_ \_ informations sur le document informatisé**</span><span class="sxs-lookup"><span data-stu-id="08264-108"><span id="TRANSACTION_SET_INFORMATION"></span><span id="transaction_set_information"></span>**TRANSACTION\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-109">0x000002</span><span class="sxs-lookup"><span data-stu-id="08264-109">0x000002</span></span>
</dt> <dt>



<span data-ttu-id="08264-110">L’appelant peut définir des informations de transaction.</span><span class="sxs-lookup"><span data-stu-id="08264-110">The caller can set transaction information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**inscription des transactions \_**</span><span class="sxs-lookup"><span data-stu-id="08264-111"><span id="TRANSACTION_ENLIST"></span><span id="transaction_enlist"></span>**TRANSACTION\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-112">0x000004</span><span class="sxs-lookup"><span data-stu-id="08264-112">0x000004</span></span>
</dt> <dt>



<span data-ttu-id="08264-113">L’appelant peut s’inscrire dans cette transaction.</span><span class="sxs-lookup"><span data-stu-id="08264-113">The caller can enlist in this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**validation de TRANSACTION \_**</span><span class="sxs-lookup"><span data-stu-id="08264-114"><span id="TRANSACTION_COMMIT"></span><span id="transaction_commit"></span>**TRANSACTION\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-115">0x000008</span><span class="sxs-lookup"><span data-stu-id="08264-115">0x000008</span></span>
</dt> <dt>



<span data-ttu-id="08264-116">L’appelant peut valider cette transaction.</span><span class="sxs-lookup"><span data-stu-id="08264-116">The caller can commit this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**restauration de TRANSACTION \_**</span><span class="sxs-lookup"><span data-stu-id="08264-117"><span id="TRANSACTION_ROLLBACK"></span><span id="transaction_rollback"></span>**TRANSACTION\_ROLLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-118">0x000010</span><span class="sxs-lookup"><span data-stu-id="08264-118">0x000010</span></span>
</dt> <dt>



<span data-ttu-id="08264-119">L’appelant peut restaurer cette transaction.</span><span class="sxs-lookup"><span data-stu-id="08264-119">The caller can roll back this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**propagation de la TRANSACTION \_**</span><span class="sxs-lookup"><span data-stu-id="08264-120"><span id="TRANSACTION_PROPAGATE"></span><span id="transaction_propagate"></span>**TRANSACTION\_PROPAGATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-121">0x000020</span><span class="sxs-lookup"><span data-stu-id="08264-121">0x000020</span></span>
</dt> <dt>



<span data-ttu-id="08264-122">L’appelant peut propager cette transaction à un gestionnaire de ressources supérieur, tel que le Distributed Transaction Coordinator (DTC).</span><span class="sxs-lookup"><span data-stu-id="08264-122">The caller can propagate this transaction to a superior resource manager, such as the Distributed Transaction Coordinator (DTC).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**\_lecture générique de la transaction \_**</span><span class="sxs-lookup"><span data-stu-id="08264-123"><span id="TRANSACTION_GENERIC_READ"></span><span id="transaction_generic_read"></span>**TRANSACTION\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-124">0x120001</span><span class="sxs-lookup"><span data-stu-id="08264-124">0x120001</span></span>
</dt> <dt>



<span data-ttu-id="08264-125">L’appelant dispose des privilèges suivants : **\_ \_ lecture des droits standard**, **\_ \_ informations sur la requête de transaction** et **synchroniser**.</span><span class="sxs-lookup"><span data-stu-id="08264-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ**, **TRANSACTION\_QUERY\_INFORMATION**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**\_écriture générique de transaction \_**</span><span class="sxs-lookup"><span data-stu-id="08264-126"><span id="TRANSACTION_GENERIC_WRITE"></span><span id="transaction_generic_write"></span>**TRANSACTION\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-127">0x12003E</span><span class="sxs-lookup"><span data-stu-id="08264-127">0x12003E</span></span>
</dt> <dt>



<span data-ttu-id="08264-128">L’appelant dispose des privilèges suivants : **\_ \_ écriture des droits standard**, **\_ \_ informations sur** le document informatisé, **\_ validation** de la transaction, **\_ inscription** des transactions, **\_ restauration** de la transaction, **\_ propagation** de la transaction et **synchronisation**.</span><span class="sxs-lookup"><span data-stu-id="08264-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ENLIST**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**\_Exécution générique de la transaction \_**</span><span class="sxs-lookup"><span data-stu-id="08264-129"><span id="TRANSACTION_GENERIC_EXECUTE"></span><span id="transaction_generic_execute"></span>**TRANSACTION\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-130">0x120018</span><span class="sxs-lookup"><span data-stu-id="08264-130">0x120018</span></span>
</dt> <dt>



<span data-ttu-id="08264-131">L’appelant dispose des privilèges suivants : **les \_ droits standard \_ s’exécutent**, la **\_ validation** de la transaction, la **\_ restauration** de la transaction et la **synchronisation**.</span><span class="sxs-lookup"><span data-stu-id="08264-131">The caller has the following privileges: **STANDARD\_RIGHTS\_EXECUTE**, **TRANSACTION\_COMMIT**, **TRANSACTION\_ROLLBACK**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**\_tout \_ accès aux transactions**</span><span class="sxs-lookup"><span data-stu-id="08264-132"><span id="TRANSACTION_ALL_ACCESS"></span><span id="transaction_all_access"></span>**TRANSACTION\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-133">0x12003F</span><span class="sxs-lookup"><span data-stu-id="08264-133">0x12003F</span></span>
</dt> <dt>



<span data-ttu-id="08264-134">L’appelant dispose des privilèges suivants : **\_ droits standard \_ requis**, **\_ \_ lecture générique de transaction**, **\_ \_ écriture générique** de transaction **et \_ \_ Exécution générique de transaction**.</span><span class="sxs-lookup"><span data-stu-id="08264-134">The caller has the following privilege: **STANDARD\_RIGHTS\_REQUIRED**, **TRANSACTION\_GENERIC\_READ**, **TRANSACTION\_GENERIC\_WRITE**, and **TRANSACTION\_GENERIC\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="08264-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**\_droits du \_ Gestionnaire de ressources de transaction \_**</span><span class="sxs-lookup"><span data-stu-id="08264-135"><span id="TRANSACTION_RESOURCE_MANAGER_RIGHTS"></span><span id="transaction_resource_manager_rights"></span>**TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="08264-136">0x120037</span><span class="sxs-lookup"><span data-stu-id="08264-136">0x120037</span></span>
</dt> <dt>



<span data-ttu-id="08264-137">L’appelant dispose des privilèges suivants : **\_ \_ lecture générique** de la transaction, **\_ \_ écriture des droits standard**, **\_ \_ informations sur** le document informatisé, **\_ restauration** de la transaction, **\_ inscription** des transactions, **\_ propagation** de la transaction et **synchroniser**.</span><span class="sxs-lookup"><span data-stu-id="08264-137">The caller has the following privileges: **TRANSACTION\_GENERIC\_READ**, **STANDARD\_RIGHTS\_WRITE**, **TRANSACTION\_SET\_INFORMATION**, **TRANSACTION\_ROLLBACK**, **TRANSACTION\_ENLIST**, **TRANSACTION\_PROPAGATE**, and **SYNCHRONIZE**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08264-138">Notes</span><span class="sxs-lookup"><span data-stu-id="08264-138">Remarks</span></span>

<span data-ttu-id="08264-139">Il est recommandé que les gestionnaires de ressources, lors de l’inscription dans une transaction, spécifient les droits du gestionnaire de ressources de transaction lors de l’ouverture d’une transaction. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="08264-139">It is recommended that resource managers, when enlisting in a transaction, specify **TRANSACTION\_RESOURCE\_MANAGER\_RIGHTS** when opening a transaction.</span></span>

## <a name="requirements"></a><span data-ttu-id="08264-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08264-140">Requirements</span></span>



| <span data-ttu-id="08264-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08264-141">Requirement</span></span> | <span data-ttu-id="08264-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="08264-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08264-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08264-143">Minimum supported client</span></span><br/> | <span data-ttu-id="08264-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08264-144">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="08264-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08264-145">Minimum supported server</span></span><br/> | <span data-ttu-id="08264-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08264-146">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="08264-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="08264-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="08264-148"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="08264-148"><dt>WinNT.h</dt></span></span> </dl> |



 

 




