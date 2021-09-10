---
title: MachineLaunchRestriction
description: Définit la stratégie de restriction à l’ensemble de l’ordinateur pour le lancement et l’activation de composants.
ms.assetid: 274e3d08-1f38-4179-b7e7-b218d6e184ee
keywords:
- Valeur de Registre MachineLaunchRestriction COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14dfcfe5535871c6b5b0fe310c94b920c522f05a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363524"
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

 

 




