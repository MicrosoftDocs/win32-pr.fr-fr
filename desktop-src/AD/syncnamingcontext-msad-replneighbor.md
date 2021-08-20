---
title: Méthode SyncNamingContext de la classe MSAD_ReplNeighbor
description: Appelle la fonction DsReplicaSync qui synchronise un contexte d’appellation de destination avec l’une de ses sources.
ms.assetid: 005053c4-8d9c-42f6-bae6-3ecdedd5ac2b
ms.tgt_platform: multiple
keywords:
- Active Directory de la méthode SyncNamingContext
- Active Directory de la méthode SyncNamingContext, classe MSAD_ReplNeighbor
- MSAD_ReplNeighbor de la classe Active Directory, méthode SyncNamingContext
topic_type:
- apiref
api_name:
- MSAD_ReplNeighbor.SyncNamingContext
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b96dd7363b5c2a48a6c25826d8c2752c181bc9125955b6c73d5532eb2665514
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024667"
---
# <a name="syncnamingcontext-method-of-the-msad_replneighbor-class"></a>Méthode SyncNamingContext de la \_ classe REPLNEIGHBOR MSAD

Appelle la fonction [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) qui synchronise un contexte d’appellation de destination avec l’une de ses sources.

## <a name="syntax"></a>Syntaxe


```mof
void SyncNamingContext(
  [in] uint32 Options
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Options* \[ dans\]
</dt> <dd>

Données supplémentaires qui déterminent la façon dont la méthode traite la requête. Ce paramètre peut être une combinaison des valeurs suivantes.

<dt>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>

<span id="DS_REPSYNC_ADD_REFERENCE"></span><span id="ds_repsync_add_reference"></span>**REPSYNC DS- \_ \_ Ajouter une \_ référence**


</dt> <dd>

Fait en sorte que l’agent de système d’annuaire source (DSA) vérifie que le DSA local est présent dans la liste sources répliquées-vers. Si le DSA local n’est pas présent, il est ajouté. Cela garantit que la source envoie des notifications de modification.

</dd> <dt>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>

<span id="DS_REPSYNC_ALL_SOURCES"></span><span id="ds_repsync_all_sources"></span>**\_REPSYNC \_ toutes les \_ sources DS**


</dt> <dd>

Cette valeur n’est pas prise en charge.

**Windows server 2008 R2, Windows server 2008 et Windows server 2003 :** Effectue une synchronisation à partir de toutes les sources.

</dd> <dt>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>

<span id="DS_REPSYNC_ASYNCHRONOUS_OPERATION"></span><span id="ds_repsync_asynchronous_operation"></span>**\_ \_ opération asynchrone REPSYNC \_ DS**


</dt> <dd>

Effectue cette opération de façon asynchrone.

**Windows server 2008 R2, Windows server 2008 et Windows server 2003 :** Obligatoire lors de l’utilisation de **\_ \_ toutes les \_ sources DS REPSYNC**.

</dd> <dt>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>

<span id="DS_REPSYNC_FORCE"></span><span id="ds_repsync_force"></span>**\_force REPSYNC \_ DS**


</dt> <dd>

Se synchronise même si le lien est actuellement désactivé.

</dd> <dt>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>

<span id="DS_REPSYNC_FULL"></span><span id="ds_repsync_full"></span>**\_REPSYNC DS \_ Full**


</dt> <dd>

Synchronise à partir du premier numéro de séquence de mise à jour (USN).

</dd> <dt>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>

<span id="DS_REPSYNC_INTERSITE_MESSAGING"></span><span id="ds_repsync_intersite_messaging"></span>**\_ \_ messagerie intersite REPSYNC \_ DS**


</dt> <dd>

Synchronise à l’aide d’ISM.

</dd> <dt>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>

<span id="DS_REPSYNC_NO_DISCARD"></span><span id="ds_repsync_no_discard"></span>**SERVICE d’REPSYNC de l' \_ \_ absence de \_ rejet**


</dt> <dd>

N’ignore pas cette demande de synchronisation, même si une synchronisation similaire est en attente.

</dd> <dt>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>

<span id="DS_REPSYNC_PERIODIC"></span><span id="ds_repsync_periodic"></span>**\_périodique REPSYNC \_ DS**


</dt> <dd>

Indique que cette opération est une demande de synchronisation périodique planifiée par l’administrateur.

</dd> <dt>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>

<span id="DS_REPSYNC_URGENT"></span><span id="ds_repsync_urgent"></span>**\_REPSYNC DS \_ urgent**


</dt> <dd>

Indique que cette opération est une notification d’une mise à jour marquée comme urgente.

</dd> <dt>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>

<span id="DS_REPSYNC_WRITEABLE"></span><span id="ds_repsync_writeable"></span>**\_REPSYNC DS \_ accessible en écriture**


</dt> <dd>

Indique que ce réplica est accessible en écriture. Si cet indicateur n’est pas défini, le réplica est en lecture seule.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\MicrosoftActiveDirectory racine<br/>                                               |
| MOF<br/>                      | <dl> <dt>ReplProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Replprov.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSAD \_ ReplNeighbor**](msad-replneighbor.md)
</dt> </dl>

 

 





