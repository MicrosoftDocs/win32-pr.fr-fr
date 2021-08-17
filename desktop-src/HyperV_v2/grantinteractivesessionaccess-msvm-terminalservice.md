---
description: Octroie l’accès à la session interactive de l’ordinateur virtuel à la liste de confiance spécifiée.
ms.assetid: 8a82170d-067b-47e5-a15f-21d6c04128d2
title: Méthode GrantInteractiveSessionAccess de la classe Msvm_TerminalService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GrantInteractiveSessionAccess
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 39fd1e77eeea7429a2ef225226b964e44f1384295dc798c1b93611f282674fb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682329"
---
# <a name="grantinteractivesessionaccess-method-of-the-msvm_terminalservice-class"></a>Méthode GrantInteractiveSessionAccess de la \_ classe TerminalService MSVM

Octroie l’accès à la session interactive de l’ordinateur virtuel à la liste de confiance spécifiée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GrantInteractiveSessionAccess(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 Trustees[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ComputerSystem* \[ dans\]
</dt> <dd>

Référence à une instance de la classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) qui représente l’ordinateur virtuel auquel l’accès sera accordé.

</dd> <dt>

*Des approbations* \[ dans\]
</dt> <dd>

Tableau de chaînes, chacune identifiant un tiers de confiance qui sera autorisé à accéder à la session interactive de l’ordinateur virtuel. les identificateurs de tiers de confiance doivent être spécifiés dans Windows format compatible SAM ou Windows format de chaîne SID.

</dd> <dt>

*Travail* \[ à\]
</dt> <dd>

Si l’opération est effectuée de façon asynchrone, cette méthode retourne 4096 et ce paramètre contient une référence à un objet dérivé de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne l’une des valeurs suivantes.

<dl> <dt>

**Terminé sans erreur** (0)
</dt> <dt>

**Non pris en charge** (1)
</dt> <dt>

**Échec** (2)
</dt> <dt>

**Délai d’expiration** (3)
</dt> <dt>

**Paramètre non valide** (4)
</dt> <dt>

**État non valide** (5)
</dt> <dt>

**Paramètres incompatibles** (6)
</dt> <dt>

**DMTF réservé** (..)
</dt> <dt>

**Paramètres de méthode activés-tâche démarrée** (4096)
</dt> <dt>

**Méthode réservée** (4097.. 32767)
</dt> <dt>

**Spécifique au fournisseur** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ TerminalService**](msvm-terminalservice.md)
</dt> </dl>

 

