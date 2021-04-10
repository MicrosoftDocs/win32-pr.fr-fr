---
description: Méthode permettant d’arrêter ce travail et tous les processus sous-jacents, et de supprimer toute association non résolue. Cette méthode est déconseillée ; Utilisez RequestChangeState à la place.
ms.assetid: b116631f-34b8-43ed-9c17-062b5e6058d0
title: Méthode KillJob de la classe CIM_Job
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Job.KillJob
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 967e5e8510d4456a085f393291f8c41afb5be446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951810"
---
# <a name="killjob-method-of-the-cim_job-class"></a>Méthode KillJob de la \_ classe Job CIM

Méthode permettant d’arrêter ce travail et tous les processus sous-jacents, et de supprimer toute association « non résolue ». Cette méthode est déconseillée ; Utilisez **RequestChangeState** à la place. **KillJob** est déconseillé, car il n’existe aucune distinction entre un arrêt ordonné et un arrêt immédiat. [**CIM \_ ConcreteJob**](cim-concretejob.md). **RequestStateChange**() fournit les options’Terminate’et’Kill’pour permettre cette distinction.

## <a name="syntax"></a>Syntaxe


```mof
uint32 KillJob(
  [in] boolean DeleteOnKill
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*DeleteOnKill* \[ dans\]
</dt> <dd>

Indique si le travail doit être supprimé automatiquement lors de l’arrêt. Ce paramètre est prioritaire sur la propriété **DeleteOnCompletion** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Inconnu** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Échec** (4)
</dt> <dt>

**Accès refusé** (6)
</dt> <dt>

**Introuvable** (7)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Travail CIM**](cim-job.md)
</dt> </dl>

 

 




