---
title: SRPRunningObjectChecks
description: Détermine si les tentatives de connexion aux objets en cours d’exécution sont filtrées pour les niveaux de confiance de stratégie de restriction logicielle (SRP) compatibles.
ms.assetid: ab5e74f0-d167-4fb2-af1b-03704039e87c
keywords:
- Valeur de Registre SRPRunningObjectChecks COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ad307856bcfdd30cfaa6c731551ac6570d2bec6
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363500"
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

 

 




