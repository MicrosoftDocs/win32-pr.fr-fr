---
description: Isolation des erreurs et stratégie FailFast
ms.assetid: 219c417c-a8a1-49eb-bc5a-702a16994d66
title: Isolation des erreurs et stratégie FailFast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc097a6d45f10d4ef8a8d059b1376862edd785ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523431"
---
# <a name="fault-isolation-and-failfast-policy"></a>Isolation des erreurs et stratégie FailFast

COM+ effectue une intégrité interne et des vérifications de cohérence étendues. Si COM+ rencontre une condition d’erreur interne inattendue, il met immédiatement fin au processus. Cette stratégie, appelée *FailFast*, facilite la contention des erreurs et aboutit à des systèmes plus fiables et fiables.

Prenons l’exemple d’un cas dans lequel COM+ détecte qu’une de ses structures de données est dans un état endommagé. À ce stade, la cause et l’ampleur de l’endommagement sont inconnues et, malheureusement, COM+ ne peut pas indiquer le degré de propagation des dégâts. Toutefois, même si COM+ est dans un état indéterminé, il ne s’exécute pas de manière isolée. Comme les autres dll, il est hébergé dans un environnement de processus et partage un espace d’adressage unique avec l’exécutable principal du programme et de nombreuses autres dll. Par conséquent, COM+ suppose que l’intégralité du processus a été endommagé et que le processus est immédiatement interrompu pour l’empêcher de diffuser des informations potentiellement endommagées vers d’autres processus ou, pire encore, d’autoriser la validation et la durabilité des données endommagées.

COM+ n’autorise pas les exceptions à se propager en dehors d’un contexte. Si une exception se produit lors de l’exécution dans un contexte COM+ et que l’application n’intercepte pas l’exception avant de retourner à partir du contexte, COM+ intercepte l’exception et met fin au processus. Dans ce cas, l’utilisation de la stratégie FailFast est basée sur l’hypothèse que l’exception a placé le processus dans un état indéterminé ; Il n’est pas possible de continuer le traitement.

En tant que développeur ou administrateur, vous devez examiner le journal des applications observateur d’événements pour plus d’informations sur les actions FailFast ou les erreurs d’application graves.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recherche de la source d’une erreur](finding-the-source-of-an-error.md)
</dt> <dt>

[Modification des valeurs de retour par COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interprétation des codes d’erreur](interpreting-error-codes.md)
</dt> <dt>

[Stratégies de gestion des erreurs dans COM+](strategies-for-handling-errors-in-com-.md)
</dt> <dt>

[Dépannage](troubleshooting-the-com--crm.md)
</dt> </dl>

 

 



