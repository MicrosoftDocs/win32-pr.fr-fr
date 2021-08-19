---
description: Récupère une erreur en raison d’une tâche ayant échoué.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: Méthode GetError de la classe CIM_ConcreteJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0b43d433bf9d2a3967efcc4a2e927d3bf687ebfa5ac67d7c7e34c48c34832c26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813265"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a>Méthode GetError de la \_ classe CIM ConcreteJob

Récupère une erreur en raison d’une tâche ayant échoué. Lorsque le travail est en cours d’exécution ou s’est terminé sans erreur, cette méthode ne retourne aucune instance d' [**\_ erreur CIM**](cim-error.md) . Toutefois, si la tâche a échoué en raison d’un problème interne ou parce que la tâche a été arrêtée par un client, une instance d' **\_ erreur CIM** est retournée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Erreur* \[ à\]
</dt> <dd>

Retourne une instance d' [**\_ erreur CIM**](cim-error.md) si le **OperationalStatus** sur le travail n’est pas « OK »; sinon, retourne la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite ; Sinon, retourne une erreur.

<dl> <dt>

**Opération réussie** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Erreur non spécifiée** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Échec** (4)
</dt> <dt>

**Paramètre non valide** (5)
</dt> <dt>

**Accès refusé** (6)
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

[**\_CONCRETEJOB CIM**](cim-concretejob.md)
</dt> </dl>

 

 




