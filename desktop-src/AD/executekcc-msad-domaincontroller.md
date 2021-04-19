---
title: Méthode ExecuteKCC de la classe MSAD_DomainController
description: Appelle la fonction DsReplicaConsistencyCheck, qui appelle le vérificateur de cohérence des connaissances (KCC) pour vérifier la topologie de réplication.
ms.assetid: 958c9a15-cde2-4c74-bd4c-c2d53551cfb0
ms.tgt_platform: multiple
keywords:
- Active Directory de la méthode ExecuteKCC
- Active Directory de la méthode ExecuteKCC, classe MSAD_DomainController
- MSAD_DomainController de la classe Active Directory, méthode ExecuteKCC
topic_type:
- apiref
api_name:
- MSAD_DomainController.ExecuteKCC
api_location:
- replprov.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcce017f86042181d2e80ae3614e3fc1cbccc676
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106518091"
---
# <a name="executekcc-method-of-the-msad_domaincontroller-class"></a>Méthode ExecuteKCC de la \_ classe DOMAINCONTROLLER MSAD

Appelle la fonction [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck) , qui appelle le vérificateur de cohérence des connaissances (KCC) pour vérifier la topologie de réplication.

## <a name="syntax"></a>Syntaxe


```mof
void ExecuteKCC(
  [in] uint32 TaskID,
  [in] uint32 dwFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*TaskId* \[ dans\]
</dt> <dd>

Tâche que le KCC doit exécuter. **Service d’annuaire \_ La \_ \_ \_ topologie de mise à jour de KCC TaskID** est la seule valeur actuellement prise en charge.

</dd> <dt>

*dwFlags* \[ dans\]
</dt> <dd>

Ensemble d’indicateurs qui modifient le comportement de la méthode **ExecuteKCC** . Ce paramètre peut avoir la valeur zéro ou une combinaison d’une ou plusieurs des valeurs suivantes.

<dt>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>

<span id="DS_KCC_FLAG_ASYNC_OP"></span><span id="ds_kcc_flag_async_op"></span>**indicateur KCC des services de domaine Active Directory \_ \_ \_ asynchrone \_**


</dt> <dd>

La tâche est mise en file d’attente, puis la fonction retourne sans attendre que la tâche se termine.

</dd> <dt>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>

<span id="DS_KCC_FLAG_DAMPED"></span><span id="ds_kcc_flag_damped"></span>**\_indicateur KCC \_ DS \_ amorti**


</dt> <dd>

La tâche ne sera pas ajoutée à la file d’attente si une autre tâche en file d’attente s’exécutera bientôt.

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

[**MSAD \_ DomainController**](msad-domaincontroller.md)
</dt> </dl>

 

 





