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
# <a name="msad_replpendingop-class"></a>MSAD \_ ReplPendingOp, classe

Représente la [**structure \_ de \_ réplication DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw) , qui décrit une tâche de réplication en cours d’exécution ou en attente d’exécution. Cette structure est retournée par la fonction [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow) .

## <a name="syntax"></a>Syntaxe

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

## <a name="members"></a>Membres

La classe **MSAD \_ ReplPendingOp** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSAD \_ ReplPendingOp** possède les propriétés suivantes.

<dl> <dt>

**DsaAddress**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’adresse réseau spécifique au transport du serveur distant associé à cette opération. **Null** s’il n’existe aucun serveur distant associé à cette opération.

</dd> <dt>

**DsaDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le chemin d’accès X. 500 du DSA associé au serveur distant qui correspond à cette opération. **Null** si aucun serveur distant ne correspond à cette opération.

</dd> <dt>

**DsaObjGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur de l’attribut [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) du DSA identifié par la propriété **DsaDN** .

</dd> <dt>

**NamingContextDN**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le chemin d’accès X. 500 du contexte d’appellation (NC) associé à cette opération.

</dd> <dt>

**NamingContextObjGuid**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’attribut [**objectGUID**](/windows/desktop/ADSchema/a-objectguid) du contexte de nommage qui est identifié par la propriété **NamingContextDN** .

</dd> <dt>

**OpStartTime**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’heure à laquelle l’opération a été démarrée. **Null** si cette opération est toujours dans la file d’attente.

</dd> <dt>

**Options**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient le jeu d’indicateurs qui fournit des données supplémentaires sur l’opération. Le contenu de ce membre est déterminé par la valeur de la propriété **optype** .

<dt>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>

<span id="DS_REPL_OP_TYPE_SYNC"></span><span id="ds_repl_op_type_sync"></span>**\_synchronisation du \_ type d’opération de RÉplication DS \_ \_**


</dt> <dd>

Contient zéro ou une combinaison d’une ou plusieurs des valeurs **DS \_ REPSYNC \_ \** _, comme défini pour le paramètre _Options * dans [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>

<span id="DS_REPL_OP_TYPE_ADD"></span><span id="ds_repl_op_type_add"></span>**Ajout d’un \_ type d’opération de réplication DS \_ \_ \_**


</dt> <dd>

Contient zéro ou une combinaison d’une ou plusieurs des valeurs de *\_ \_ \* reremplissage* des * DS, comme défini pour le paramètre _Options * dans [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>

<span id="DS_REPL_OP_TYPE_DELETE"></span><span id="ds_repl_op_type_delete"></span>**\_suppression du \_ type d’opération de RÉplication DS \_ \_**


</dt> <dd>

Contient zéro ou une combinaison d’une ou plusieurs des valeurs **DS \_ REPDEL \_ \** _, comme défini pour le paramètre _Options * dans [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>

<span id="DS_REPL_OP_TYPE_MODIFY"></span><span id="ds_repl_op_type_modify"></span>**\_modification du \_ type d’opération de RÉplication DS \_ \_**


</dt> <dd>

Contient zéro ou une combinaison d’une ou plusieurs des valeurs **DS \_ REPMOD \_ \** _, comme défini pour le paramètre _Options * dans [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya).

</dd> <dt>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>

<span id="DS_REPL_OP_TYPE_UPDATE_REFS"></span><span id="ds_repl_op_type_update_refs"></span>**\_références de \_ \_ \_ mise à jour du type \_ de service de réplication DS**


</dt> <dd>

Contient zéro ou une combinaison d’une ou plusieurs des valeurs **DS \_ REPSUPD \_ \** _, comme défini pour le paramètre _Options * dans [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa).

</dd> </dl>

</dd> <dt>

**OpType**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la valeur du [**\_ \_ \_ type de réplication DS**](/windows/desktop/api/Ntdsapi/ne-ntdsapi-ds_repl_op_type) qui indique le type d’opération représenté par cette classe.

</dd> <dt>

**PositionInQ**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la position de cette opération dans la file d’attente.

</dd> <dt>

**Priorité**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient la priorité de cette opération. Les tâches de priorité plus élevée sont exécutées en premier. La priorité est calculée par le serveur en fonction du type d’opération représenté par cette classe et des paramètres de l’opération.

</dd> <dt>

**SerialNumber**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Obtient l’ID de l’opération, qui est unique par ordinateur et par démarrage.

</dd> <dt>

**TimeEnqueued**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Obtient l’heure à laquelle cette opération a été ajoutée à la file d’attente.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\MicrosoftActiveDirectory racine<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



 

