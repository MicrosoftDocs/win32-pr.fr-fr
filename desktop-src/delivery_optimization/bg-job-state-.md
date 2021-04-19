---
title: Énumération BG_JOB_STATE (Deliveryoptimization. h)
description: L’énumération BG_JOB_STATE définit des valeurs constantes pour les différents États d’un travail.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- Énumération BG_JOB_STATE
- Énumération BG_JOB_STATE
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510735"
---
# <a name="bg_job_state-enumeration"></a>Énumération BG_JOB_STATE

L’énumération **BG_JOB_STATE** définit des valeurs constantes pour les différents États d’un travail.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**
</dt> <dd>

Spécifie que le travail se trouve dans la file d’attente et qu’il est en attente d’exécution. Si un utilisateur se déconnecte pendant le transfert de son travail, le travail passe à l’État en file d’attente.

</dd> <dt>

<span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**
</dt> <dd>

Non pris en charge.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**
</dt> <dd>

Spécifie que effectue le transfert des données pour le travail.

</dd> <dt>

<span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**
</dt> <dd>

Spécifie que le travail est suspendu (suspendu). Pour interrompre un travail, appelez la méthode [**méthode ibackgroundcopyjob :: suspend**](ibackgroundcopyjob-suspend.md) . Le travail reste suspendu jusqu’à ce que vous appeliez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md), [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md)ou [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) .

</dd> <dt>

<span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**
</dt> <dd>

Spécifie qu’une erreur irrécupérable s’est produite (le service n’est pas en mesure de transférer le fichier). Si l’erreur, telle qu’une erreur d’accès refusé, peut être corrigée, appelez la méthode [**méthode ibackgroundcopyjob :: Resume**](ibackgroundcopyjob-resume.md) une fois l’erreur corrigée. Toutefois, si l’erreur ne peut pas être corrigée, appelez la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) pour annuler le travail, ou appelez la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour accepter la partie d’une tâche de téléchargement qui a été transférée avec succès.

</dd> <dt>

<span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**
</dt> <dd>

Spécifie qu’une erreur récupérable s’est produite. Effectuez une nouvelle tentative de travaux dans l’état d’erreur temporaire en fonction de la configuration de nouvelle tentative interne. L’état du travail devient **BG_JOB_STATE_ERROR** si le travail échoue pour progresser (voir [**méthode ibackgroundcopyjob :: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).

</dd> <dt>

<span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**
</dt> <dd>

Spécifie que votre travail a été traité avec succès. Vous devez appeler la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour accuser réception de la tâche et rendre les fichiers accessibles au client.

</dd> <dt>

<span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**
</dt> <dd>

Spécifie que vous avez appelé la méthode [**méthode ibackgroundcopyjob :: Complete**](ibackgroundcopyjob-complete.md) pour confirmer que votre travail s’est terminé avec succès.

</dd> <dt>

<span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**
</dt> <dd>

Spécifie que vous avez appelé la méthode [**méthode ibackgroundcopyjob :: Cancel**](ibackgroundcopyjob-cancel.md) pour annuler le travail (supprimer la tâche de la file d’attente de transfert).

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





