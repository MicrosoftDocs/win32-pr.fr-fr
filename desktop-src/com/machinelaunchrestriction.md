---
title: MachineLaunchRestriction
description: Définit la stratégie de restriction à l’ensemble de l’ordinateur pour le lancement et l’activation de composants.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valeur de Registre MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5cd235e2dd81e596448f25adfd72ad0b16c13d2da3860eb56fb95f93ef53cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048057"
---
# <a name="machinelaunchrestriction"></a>MachineLaunchRestriction

Définit la stratégie de restriction à l’ensemble de l’ordinateur pour le lancement et l’activation de composants.

> [!Caution]  
> La modification de cette valeur affecte toutes les applications serveur COM et peut les empêcher de fonctionner correctement. Si des applications serveur COM présentent des restrictions moins strictes que les restrictions à l’niveau de l’ordinateur, la réduction des restrictions de l’ordinateur peut exposer ces applications à un accès indésirable. À l’inverse, si vous augmentez les restrictions au niveau de l’ordinateur, certaines applications serveur COM peuvent ne plus être accessibles en appelant des applications.

 

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   MachineLaunchRestriction = SECURITY_DESCRIPTOR
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur **\_ binaire de Reg** .

Les principaux qui ne reçoivent pas d’autorisations ici ne peuvent pas les obtenir, même si les autorisations sont accordées par la valeur de Registre [DefaultAccessPermission](defaultaccesspermission.md) ou par la fonction [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) .

Par défaut, les administrateurs peuvent obtenir des autorisations d’exécution et d’activation locales et à distance, et les membres du groupe tout le monde peuvent obtenir des autorisations d’activation locale et de lancement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Définition de la sécurité pour les applications COM](setting-security-for-com-applications.md)
</dt> </dl>

 

 




