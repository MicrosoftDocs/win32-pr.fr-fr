---
title: SRPRunningObjectChecks
description: Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valeur de Registre SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c416b5f430540282873e37c5e74ef2cccc1c564f4a5b27842ba2a49e99cc8769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129791"
---
# <a name="srprunningobjectchecks"></a>SRPRunningObjectChecks

Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   SRPRunningObjectChecks = value
```

## <a name="remarks"></a>Remarques

Il s’agit d’une valeur de **reg \_ SZ** .

Les valeurs de chaîne {N, n, NO, no} indiquent que les tentatives de connexion aux objets en cours d’exécution ne sont pas filtrées pour les niveaux de confiance SRP compatibles. Si cette valeur de Registre est définie sur une autre valeur ou n’existe pas, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance SRP moins strict que l’objet client. Par exemple, l’objet en cours d’exécution ne peut pas avoir un niveau de confiance non autorisé si l’objet client a un niveau de confiance illimité.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[SRPTrustLevel](srptrustlevel.md)
</dt> </dl>

 

 




