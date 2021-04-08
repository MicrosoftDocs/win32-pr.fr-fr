---
description: KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de transactions (TM).
ms.assetid: 8f9b9d3d-e7ea-4df2-82b1-2d4c3e0766c0
title: Masques d’accès du gestionnaire de transactions (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efae6c0bac1fc2bfa117e74e38aff8d439eb2f25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864566"
---
# <a name="transaction-manager-access-masks"></a><span data-ttu-id="16504-103">Masques d’accès du gestionnaire de transactions</span><span class="sxs-lookup"><span data-stu-id="16504-103">Transaction Manager Access Masks</span></span>

<span data-ttu-id="16504-104">KTM définit les masques d’accès d’inscription suivants à utiliser lors de l’ouverture d’un gestionnaire de transactions (TM).</span><span class="sxs-lookup"><span data-stu-id="16504-104">KTM defines the following enlistment access masks to be used when opening a transaction manager (TM).</span></span>

<dl> <dt>

<span data-ttu-id="16504-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**\_informations sur les requêtes TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="16504-105"><span id="TRANSACTIONMANAGER_QUERY_INFORMATION"></span><span id="transactionmanager_query_information"></span>**TRANSACTIONMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-106">0x00001</span><span class="sxs-lookup"><span data-stu-id="16504-106">0x00001</span></span>
</dt> <dt>



<span data-ttu-id="16504-107">L’appelant peut demander des informations sur ce TM.</span><span class="sxs-lookup"><span data-stu-id="16504-107">The caller can query information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**\_informations sur l’ensemble de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="16504-108"><span id="TRANSACTIONMANAGER_SET_INFORMATION"></span><span id="transactionmanager_set_information"></span>**TRANSACTIONMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-109">0x00002</span><span class="sxs-lookup"><span data-stu-id="16504-109">0x00002</span></span>
</dt> <dt>



<span data-ttu-id="16504-110">L’appelant peut définir des informations sur ce TM.</span><span class="sxs-lookup"><span data-stu-id="16504-110">The caller can set information about this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**récupération de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="16504-111"><span id="TRANSACTIONMANAGER_RECOVER"></span><span id="transactionmanager_recover"></span>**TRANSACTIONMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-112">0x00004</span><span class="sxs-lookup"><span data-stu-id="16504-112">0x00004</span></span>
</dt> <dt>



<span data-ttu-id="16504-113">L’appelant peut récupérer ce TM.</span><span class="sxs-lookup"><span data-stu-id="16504-113">The caller can recover this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**renommer TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="16504-114"><span id="TRANSACTIONMANAGER_RENAME"></span><span id="transactionmanager_rename"></span>**TRANSACTIONMANAGER\_RENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-115">0x00008</span><span class="sxs-lookup"><span data-stu-id="16504-115">0x00008</span></span>
</dt> <dt>



<span data-ttu-id="16504-116">L’appelant peut renommer une instance de TM.</span><span class="sxs-lookup"><span data-stu-id="16504-116">The caller can rename a TM instance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER \_ créer \_ RM**</span><span class="sxs-lookup"><span data-stu-id="16504-117"><span id="TRANSACTIONMANAGER_CREATE_RM"></span><span id="transactionmanager_create_rm"></span>**TRANSACTIONMANAGER\_CREATE\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-118">0x00010</span><span class="sxs-lookup"><span data-stu-id="16504-118">0x00010</span></span>
</dt> <dt>



<span data-ttu-id="16504-119">L’appelant peut créer un gestionnaire de ressources associé à ce TM.</span><span class="sxs-lookup"><span data-stu-id="16504-119">The caller can create a resource manager that is associated with this TM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**\_transaction de liaison TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="16504-120"><span id="TRANSACTIONMANAGER_BIND_TRANSACTION"></span><span id="transactionmanager_bind_transaction"></span>**TRANSACTIONMANAGER\_BIND\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-121">0x00020</span><span class="sxs-lookup"><span data-stu-id="16504-121">0x00020</span></span>
</dt> <dt>



<span data-ttu-id="16504-122">Cette valeur est réservée.</span><span class="sxs-lookup"><span data-stu-id="16504-122">This value is reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**\_lecture générique \_ TRANSACTIONMANAGER**</span><span class="sxs-lookup"><span data-stu-id="16504-123"><span id="TRANSACTIONMANAGER_GENERIC_READ"></span><span id="transactionmanager_generic_read"></span>**TRANSACTIONMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-124">0x20001</span><span class="sxs-lookup"><span data-stu-id="16504-124">0x20001</span></span>
</dt> <dt>



<span data-ttu-id="16504-125">L’appelant dispose des privilèges suivants : **\_ droits standard \_ lecture** et **\_ \_ informations sur les requêtes TRANSACTIONMANAGER**.</span><span class="sxs-lookup"><span data-stu-id="16504-125">The caller has the following privileges: **STANDARD\_RIGHTS\_READ** and **TRANSACTIONMANAGER\_QUERY\_INFORMATION**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**\_écriture générique \_ TRANSACTIONMANAGER**</span><span class="sxs-lookup"><span data-stu-id="16504-126"><span id="TRANSACTIONMANAGER_GENERIC_WRITE"></span><span id="transactionmanager_generic_write"></span>**TRANSACTIONMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-127">0x2001E</span><span class="sxs-lookup"><span data-stu-id="16504-127">0x2001E</span></span>
</dt> <dt>



<span data-ttu-id="16504-128">L’appelant dispose des privilèges suivants : **\_ \_ écriture des droits standard**, **\_ \_ informations sur le jeu de TRANSACTIONMANAGER**, **\_ récupération de TransactionManager**, **\_ renommage** de l’ensemble de données et **TransactionManager \_ créer \_ RM**.</span><span class="sxs-lookup"><span data-stu-id="16504-128">The caller has the following privileges: **STANDARD\_RIGHTS\_WRITE**, **TRANSACTIONMANAGER\_SET\_INFORMATION**, **TRANSACTIONMANAGER\_RECOVER**, **TRANSACTIONMANAGER\_RENAME**, and **TRANSACTIONMANAGER\_CREATE\_RM**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**\_Exécution générique de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="16504-129"><span id="TRANSACTIONMANAGER_GENERIC_EXECUTE"></span><span id="transactionmanager_generic_execute"></span>**TRANSACTIONMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-130">0x20000</span><span class="sxs-lookup"><span data-stu-id="16504-130">0x20000</span></span>
</dt> <dt>



<span data-ttu-id="16504-131">L’appelant dispose des privilèges suivants : **les \_ droits standard \_ s’exécutent**.</span><span class="sxs-lookup"><span data-stu-id="16504-131">The caller has the following privilege: **STANDARD\_RIGHTS\_EXECUTE**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="16504-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**\_tout \_ accès à TRANSACTIONMANAGER**</span><span class="sxs-lookup"><span data-stu-id="16504-132"><span id="TRANSACTIONMANAGER_ALL_ACCESS"></span><span id="transactionmanager_all_access"></span>**TRANSACTIONMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="16504-133">0xF003F</span><span class="sxs-lookup"><span data-stu-id="16504-133">0xF003F</span></span>
</dt> <dt>



<span data-ttu-id="16504-134">Cette valeur définit tous les bits valides pour une valeur d’accès TM.</span><span class="sxs-lookup"><span data-stu-id="16504-134">This value sets all valid bits for a TM access value.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="16504-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16504-135">Requirements</span></span>



| <span data-ttu-id="16504-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16504-136">Requirement</span></span> | <span data-ttu-id="16504-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="16504-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16504-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16504-138">Minimum supported client</span></span><br/> | <span data-ttu-id="16504-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16504-139">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="16504-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="16504-140">Minimum supported server</span></span><br/> | <span data-ttu-id="16504-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16504-141">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="16504-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="16504-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="16504-143"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="16504-143"><dt>WinNT.h</dt></span></span> </dl> |



 

 




