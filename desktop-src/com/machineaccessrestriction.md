---
title: MachineAccessRestriction
description: Définit la stratégie de restriction au niveau de l’ordinateur pour l’accès aux composants.
ms.assetid: aeb37e49-6425-4058-968e-f9d00acf4fc2
keywords:
- Valeur de Registre MachineAccessRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce78aa749618b93dfe8cbe62fad5ec0e51504f4bad0067b17628ac0226c24b2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119896189"
---
# <a name="machineaccessrestriction"></a>MachineAccessRestriction

Définit la stratégie de restriction au niveau de l’ordinateur pour l’accès aux composants.

> [!Caution]  
> La modification de cette valeur affecte toutes les applications serveur COM et peut les empêcher de fonctionner correctement. Si des applications serveur COM présentent des restrictions moins strictes que les restrictions à l’niveau de l’ordinateur, la réduction des restrictions de l’ordinateur peut exposer ces applications à un accès indésirable. À l’inverse, si vous augmentez les restrictions au niveau de l’ordinateur, certaines applications serveur COM peuvent ne plus être accessibles en appelant des applications.

 

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineAccessRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **\_ binaire de Reg** .

Les principaux qui ne reçoivent pas d’autorisations ici ne peuvent pas les obtenir, même si les autorisations sont accordées par la valeur de Registre [DefaultAccessPermission](defaultaccesspermission.md) ou par la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Par défaut, les membres du groupe tout le monde peuvent obtenir des autorisations d’accès local et distant, et les utilisateurs anonymes peuvent obtenir des autorisations d’accès local.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




