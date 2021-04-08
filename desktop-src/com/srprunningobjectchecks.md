---
title: SRPRunningObjectChecks
description: Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valeur de Registre SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672486"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Notes

Il s’agit d’une valeur de **reg \_ SZ** .

Les valeurs de chaîne {N, n, NO, no} indiquent que les tentatives de connexion aux objets en cours d’exécution ne sont pas filtrées pour les niveaux de confiance SRP compatibles. Si cette valeur de Registre est définie sur une autre valeur ou n’existe pas, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance SRP moins strict que l’objet client. Par exemple, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance non autorisé si l’objet client a un niveau de confiance illimité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




