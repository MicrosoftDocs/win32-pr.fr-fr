---
title: Classe MSAD_ReplPendingOp
description: Représente la \_ structure de \_ réplication DS, qui décrit une tâche de réplication en cours d’exécution ou en attente d’exécution.
ms.assetid: d1c101fa-ae33-48da-9b00-93fde553a4f9
ms.tgt_platform: multiple
keywords:
- MSAD_ReplPendingOp de la classe Active Directory
- MSAD_ReplPendingOp de la classe Active Directory, Description
topic_type:
- apiref
api_name:
- MSAD_ReplPendingOp
- MSAD_ReplPendingOp.SerialNumber
- MSAD_ReplPendingOp.PositionInQ
- MSAD_ReplPendingOp.OpStartTime
- MSAD_ReplPendingOp.TimeEnqueued
- MSAD_ReplPendingOp.Priority
- MSAD_ReplPendingOp.OpType
- MSAD_ReplPendingOp.Options
- MSAD_ReplPendingOp.NamingContextDN
- MSAD_ReplPendingOp.NamingContextObjGuid
- MSAD_ReplPendingOp.DsaDN
- MSAD_ReplPendingOp.DsaAddress
- MSAD_ReplPendingOp.DsaObjGuid
api_location:
- replprov.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f1c3faddac915f602104d7e5dc4e9b6bc7d6944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384680"
---
# <a name="msad_replpendingop-class"></a><span data-ttu-id="2afac-105">MSAD \_ ReplPendingOp, classe</span><span class="sxs-lookup"><span data-stu-id="2afac-105">MSAD\_ReplPendingOp class</span></span>

<span data-ttu-id="2afac-106">Représente la [**structure \_ de \_ réplication DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , qui décrit une tâche de réplication en cours d’exécution ou en attente d’exécution.</span><span class="sxs-lookup"><span data-stu-id="2afac-106">Represents the [**DS\_REPL\_OP**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) structure, which describes a replication task that is currently executing or pending execution.</span></span> <span data-ttu-id="2afac-107">Cette structure est retournée par la fonction [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .</span><span class="sxs-lookup"><span data-stu-id="2afac-107">This structure is returned by the [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afac-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2afac-108">Syntax</span></span>

``` syntax
[dynamic, provider("ReplProv1")]
class MSAD_ReplPendingOp
{
  uint32   SerialNumber;
  uint32   PositionInQ;
  datetime OpStartTime;
  datetime TimeEnqueued;
  uint32   Priority;
  uint32   OpType;
  uint32   Options;
  String   NamingContextDN;
  String   NamingContextObjGuid;
  String   DsaDN;
  String   DsaAddress;
  String   DsaObjGuid;
};
```

## <a name="members"></a><span data-ttu-id="2afac-109">Membres</span><span class="sxs-lookup"><span data-stu-id="2afac-109">Members</span></span>

<span data-ttu-id="2afac-110">La classe **MSAD \_ ReplPendingOp** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="2afac-110">The **MSAD\_ReplPendingOp** class has these types of members:</span></span>

-   [<span data-ttu-id="2afac-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2afac-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2afac-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2afac-112">Properties</span></span>

<span data-ttu-id="2afac-113">La classe **MSAD \_ ReplPendingOp** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="2afac-113">The **MSAD\_ReplPendingOp** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2afac-114">**DsaAddress**</span><span class="sxs-lookup"><span data-stu-id="2afac-114">**DsaAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-115">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2afac-115">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-116">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-117">Obtient l’adresse réseau spécifique au transport du serveur distant associé à cette opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-117">Gets the transport-specific network address of the remote server that is associated with this operation.</span></span> <span data-ttu-id="2afac-118">**Null** s’il n’existe aucun serveur distant associé à cette opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-118">**NULL** if there is no remote server that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-119">**DsaDN**</span><span class="sxs-lookup"><span data-stu-id="2afac-119">**DsaDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-120">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2afac-120">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-121">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-122">Obtient le chemin d’accès X. 500 du DSA associé au serveur distant qui correspond à cette opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-122">Gets the X.500 path of the DSA that is associated with the remote server that corresponds to this operation.</span></span> <span data-ttu-id="2afac-123">**Null** si aucun serveur distant ne correspond à cette opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-123">**NULL** if no remote server corresponds to this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-124">**DsaObjGuid**</span><span class="sxs-lookup"><span data-stu-id="2afac-124">**DsaObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2afac-125">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-127">Obtient la valeur de l’attribut [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) du DSA identifié par la propriété **DsaDN** .</span><span class="sxs-lookup"><span data-stu-id="2afac-127">Gets the value of the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the DSA that is identified by the **DsaDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-128">**NamingContextDN**</span><span class="sxs-lookup"><span data-stu-id="2afac-128">**NamingContextDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2afac-129">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-131">Obtient le chemin d’accès X. 500 du contexte d’appellation (NC) associé à cette opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-131">Gets the X.500 path of the naming context (NC) that is associated with this operation.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-132">**NamingContextObjGuid**</span><span class="sxs-lookup"><span data-stu-id="2afac-132">**NamingContextObjGuid**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-133">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="2afac-133">Data type: **String**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-134">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-135">Obtient l’attribut [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) du contexte de nommage qui est identifié par la propriété **NamingContextDN** .</span><span class="sxs-lookup"><span data-stu-id="2afac-135">Gets the [**objectGuid**](/windows/desktop/ADSchema/a-objectguid) attribute of the NC that is identified by the **NamingContextDN** property.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-136">**OpStartTime**</span><span class="sxs-lookup"><span data-stu-id="2afac-136">**OpStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-137">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2afac-137">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-138">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-139">Obtient l’heure à laquelle l’opération a été démarrée.</span><span class="sxs-lookup"><span data-stu-id="2afac-139">Gets the time when the operation was started.</span></span> <span data-ttu-id="2afac-140">**Null** si cette opération est toujours dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2afac-140">**NULL** if this operation is still in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-141">**Options**</span><span class="sxs-lookup"><span data-stu-id="2afac-141">**Options**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-142">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2afac-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-143">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-144">Obtient le jeu d’indicateurs qui fournit des données supplémentaires sur l’opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-144">Gets the set of flags that provides additional data about the operation.</span></span> <span data-ttu-id="2afac-145">Le contenu de ce membre est déterminé par la valeur de la propriété **optype** .</span><span class="sxs-lookup"><span data-stu-id="2afac-145">The contents of this member are determined by the value of the **OpType** property.</span></span>

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span data-ttu-id="2afac-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_synchronisation du \_ type d’opération de RÉplication DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2afac-146"><span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**DS\_REPL\_OP\_TYPE\_SYNC**</span></span>


</dt> <dd>

<span data-ttu-id="2afac-147">Contient zéro ou une combinaison d’une ou plusieurs des valeurs \**DS \_ REPSYNC \_ \** _, comme défini pour le paramètre _Options \* dans [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span><span class="sxs-lookup"><span data-stu-id="2afac-147">Contains zero or a combination of one or more of the **DS\_REPSYNC\_\** _ values as defined for the _Options* parameter in [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span data-ttu-id="2afac-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**Ajout d’un \_ type d’opération de réplication DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2afac-148"><span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**DS\_REPL\_OP\_TYPE\_ADD**</span></span>


</dt> <dd>

<span data-ttu-id="2afac-149">Contient zéro ou une combinaison d’une ou plusieurs des valeurs de *\_ \_ \* reremplissage* des \* DS, comme défini pour le paramètre _Options \* dans [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span><span class="sxs-lookup"><span data-stu-id="2afac-149">Contains zero or a combination of one or more of the **DS\_REPADD\_\** _ values as defined for the _Options* parameter in [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span data-ttu-id="2afac-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_suppression du \_ type d’opération de RÉplication DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2afac-150"><span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**DS\_REPL\_OP\_TYPE\_DELETE**</span></span>


</dt> <dd>

<span data-ttu-id="2afac-151">Contient zéro ou une combinaison d’une ou plusieurs des valeurs \**DS \_ REPDEL \_ \** _, comme défini pour le paramètre _Options \* dans [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span><span class="sxs-lookup"><span data-stu-id="2afac-151">Contains zero or a combination of one or more of the **DS\_REPDEL\_\** _ values as defined for the _Options* parameter in [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span data-ttu-id="2afac-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**\_modification du \_ type d’opération de RÉplication DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2afac-152"><span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**DS\_REPL\_OP\_TYPE\_MODIFY**</span></span>


</dt> <dd>

<span data-ttu-id="2afac-153">Contient zéro ou une combinaison d’une ou plusieurs des valeurs \**DS \_ REPMOD \_ \** _, comme défini pour le paramètre _Options \* dans [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span><span class="sxs-lookup"><span data-stu-id="2afac-153">Contains zero or a combination of one or more of the **DS\_REPMOD\_\** _ values as defined for the _Options* parameter in [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).</span></span>

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span data-ttu-id="2afac-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_références de \_ \_ \_ mise à jour du type \_ de service de réplication DS**</span><span class="sxs-lookup"><span data-stu-id="2afac-154"><span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**DS\_REPL\_OP\_TYPE\_UPDATE\_REFS**</span></span>


</dt> <dd>

<span data-ttu-id="2afac-155">Contient zéro ou une combinaison d’une ou plusieurs des valeurs \**DS \_ REPSUPD \_ \** _, comme défini pour le paramètre _Options \* dans [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span><span class="sxs-lookup"><span data-stu-id="2afac-155">Contains zero or a combination of one or more of the **DS\_REPSUPD\_\** _ values as defined for the _Options* parameter in [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="2afac-156">**OpType**</span><span class="sxs-lookup"><span data-stu-id="2afac-156">**OpType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-157">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2afac-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-158">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-159">Obtient la valeur du [**\_ \_ \_ type de réplication DS**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) qui indique le type d’opération représenté par cette classe.</span><span class="sxs-lookup"><span data-stu-id="2afac-159">Gets the [**DS\_REPL\_OP\_TYPE**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) value that indicates the type of operation that this class represents.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-160">**PositionInQ**</span><span class="sxs-lookup"><span data-stu-id="2afac-160">**PositionInQ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-161">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2afac-161">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-162">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-163">Obtient la position de cette opération dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2afac-163">Gets the position of this operation in the queue.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-164">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="2afac-164">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-165">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2afac-165">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-166">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-166">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-167">Obtient la priorité de cette opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-167">Gets the priority of this operation.</span></span> <span data-ttu-id="2afac-168">Les tâches de priorité plus élevée sont exécutées en premier.</span><span class="sxs-lookup"><span data-stu-id="2afac-168">Higher-priority tasks are executed first.</span></span> <span data-ttu-id="2afac-169">La priorité est calculée par le serveur en fonction du type d’opération représenté par cette classe et des paramètres de l’opération.</span><span class="sxs-lookup"><span data-stu-id="2afac-169">The priority is calculated by the server based on the type of operation that this class represents and the parameters of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-170">**SerialNumber**</span><span class="sxs-lookup"><span data-stu-id="2afac-170">**SerialNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-171">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="2afac-171">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-172">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-172">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2afac-173">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2afac-173">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="2afac-174">Obtient l’ID de l’opération, qui est unique par ordinateur et par démarrage.</span><span class="sxs-lookup"><span data-stu-id="2afac-174">Gets the ID of the operation, which is unique per-machine and per-boot.</span></span>

</dd> <dt>

<span data-ttu-id="2afac-175">**TimeEnqueued**</span><span class="sxs-lookup"><span data-stu-id="2afac-175">**TimeEnqueued**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2afac-176">Type de données : **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2afac-176">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2afac-177">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="2afac-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2afac-178">Obtient l’heure à laquelle cette opération a été ajoutée à la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="2afac-178">Gets the time at which this operation was added to the queue.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2afac-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2afac-179">Requirements</span></span>



| <span data-ttu-id="2afac-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2afac-180">Requirement</span></span> | <span data-ttu-id="2afac-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="2afac-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2afac-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afac-182">Minimum supported client</span></span><br/> | <span data-ttu-id="2afac-183">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afac-183">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2afac-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afac-184">Minimum supported server</span></span><br/> | <span data-ttu-id="2afac-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2afac-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2afac-186">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="2afac-186">Namespace</span></span><br/>                | <span data-ttu-id="2afac-187">\\MicrosoftActiveDirectory racine</span><span class="sxs-lookup"><span data-stu-id="2afac-187">Root\\MicrosoftActiveDirectory</span></span><br/>                                               |
| <span data-ttu-id="2afac-188">MOF</span><span class="sxs-lookup"><span data-stu-id="2afac-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2afac-189"><dt>ReplProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2afac-189"><dt>Replprov.mof</dt></span></span> </dl> |
| <span data-ttu-id="2afac-190">DLL</span><span class="sxs-lookup"><span data-stu-id="2afac-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2afac-191"><dt>Replprov.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2afac-191"><dt>Replprov.dll</dt></span></span> </dl> |



 

