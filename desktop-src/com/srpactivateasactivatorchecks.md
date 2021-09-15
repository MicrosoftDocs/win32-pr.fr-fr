---
title: SRPActivateAsActivatorChecks
description: Détermine si les niveaux de confiance de la stratégie de restriction logicielle (SRP) sont utilisés lors des activations de ActivateAsActivator.
ms.assetid: b0d616c3-1cb0-4854-a4f9-6635d61b0698
keywords:
- Valeur de Registre SRPActivateAsActivatorChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b66ae6b1c7f267f48f24441c04e95eea75e4345
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127294326"
---
# <a name="srpactivateasactivatorchecks"></a>SRPActivateAsActivatorChecks

Détermine si les niveaux de confiance de la stratégie de restriction logicielle (SRP) sont utilisés lors des activations de ActivateAsActivator.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPActivateAsActivatorChecks = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** .

Les valeurs de chaîne {N, n, NO, no} indiquent que l’objet serveur s’exécute avec le niveau de confiance SRP de l’objet client, quel que soit le niveau de confiance du SRP avec lequel il a été configuré. Si cette valeur de Registre est définie sur une autre valeur ou n’existe pas, le niveau de confiance SRP configuré pour l’objet serveur est comparé au niveau de confiance SRP de l’objet client et le niveau de confiance le plus strict est utilisé pour exécuter l’objet serveur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




