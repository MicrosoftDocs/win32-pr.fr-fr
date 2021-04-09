---
description: Une table de routage distribuée (DRT) existe sous la forme d’une maille de nœuds coopérants, où chaque nœud est une instance d’une application utilisant l’API DRT.
ms.assetid: 257ad7ea-636b-45f2-b514-4a213939d107
title: À propos des tables de routage distribuées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfca9f81cc609d97584ef5a11f999722c696858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865182"
---
# <a name="about-distributed-routing-tables"></a>À propos des tables de routage distribuées

Une table de routage distribuée (DRT) existe sous la forme d’une maille de nœuds coopérants, où chaque nœud est une instance d’une application utilisant l’API DRT. Les nœuds qui publient des clés sont chargés d’aider les autres nœuds à publier et à résoudre les clés. Les nœuds peuvent également participer à un mode « résoudre uniquement », ce qui ne nécessite pas l’assistance des homologues. Le protocole DRT s’exécute sur un transport UDP/IPv6.

Nœud qui publie une génération de clé et gère une table de routage locale d’autres nœuds dans la maille. Cette table de routage est optimisée afin que le nœud puisse localiser rapidement une clé spécifique dans la maille en trouvant la clé directement dans la table de routage locale, ou en demandant à d’autres nœuds de publier des clés numériquement proches de la cible. Cette action est répétée jusqu’à ce que la clé requise soit trouvée ou que le nœud détermine qu’il n’existe pas de clé de ce type.

Les clés DRT sont des entiers non signés 256 bits. Les différences entre les clés sont définies par la différence numérique entre elles. L’espace de mémoire DRT est considéré comme circulaire. Par exemple, la première valeur de clé possible et la dernière valeur de clé possible sont considérées comme des voisins.

Dans un DRT sécurisé, les nœuds sont requis pour authentifier les clés qu’ils publient. Le mécanisme par lequel les nœuds authentifient les clés doit être défini à l’aide de l’API DRT lorsque DRT est initialisé. Pour ce faire, choisissez un fournisseur de sécurité pour DRT. Un fournisseur de sécurité est un module qui peut produire des jetons utilisés pour authentifier les clés et vérifier les jetons produits par d’autres nœuds. Il doit implémenter l’interface du fournisseur de sécurité qui est définie dans cette documentation. Le DRT de Windows 7 est fourni avec deux fournisseurs de sécurité entièrement implémentés qui peuvent être utilisés pour créer des applications Windows.

Pendant l’initialisation, une application doit également fournir à DRT un fournisseur de démarrage. Le fournisseur bootstrap est un module qui peut récupérer les points de terminaison réseau des nœuds déjà présents dans la maille DRT, et est appelé par le DRT lorsqu’un nouveau nœud est établi. À l’instar du module fournisseur de sécurité, le fournisseur bootstrap doit implémenter une interface bien définie. Le DRT de Windows 7 est fourni avec deux fournisseurs de démarrage entièrement implémentés.

Le DRT prend en compte les voisins immédiats d’une clé spéciale. Les cinq clés les plus proches numériquement plus petites et les cinq clés les plus proches numériquement supérieures à une clé publiée sont appelées un ensemble feuille. Le DRT signale les modifications apportées à l’ensemble feuille d’une clé par le biais de l’API DRT.

## <a name="drt-life-cycle-and-state-transitions"></a>Transitions d’État et de cycle de vie DRT

Une application peut initialiser une instance DRT locale à l’aide de la fonction [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen) . Cette fonction déclenche le processus d’amorçage, où l’API DRT appelle le fournisseur bootstrap pour connaître les clés et les points de terminaison réseau d’autres nœuds qui participent déjà à DRT. Si le fournisseur de démarrage réussit à localiser au moins un autre nœud, le DRT passe à l' \_ état actif DRT. Dans cet État, l’application peut rechercher les clés publiées par d’autres nœuds et peut publier les clés qui peuvent être résolues. Si le fournisseur bootstrap ne parvient pas à trouver d’autres nœuds, le DRT passe à l' \_ État autonome DRT. Le DRT reste dans l' \_ État autonome DRT et tente de se réamorcer périodiquement afin de localiser les homologues et de passer à l' \_ état actif DRT.

Un nœud peut passer à ces États à partir d’une \_ activité DRT active.

| État du cycle de vie | Conditions                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DRT \_ seul       | Le nœud local n’a pas découvert d’autres nœuds dans le DRT. Dans cet État, le nœud continue à écouter d’autres nœuds dans le DRT.<br/> Si un autre nœud rejoint le DRT, le nœud local passera à l' \_ état actif DRT. Si le réseau est défaillant, il passera à DRT \_ aucun \_ réseau. En cas d’erreur grave avec l’DRT, le nœud passera à l' \_ État d’erreur DRT.<br/> |
| DRT \_ sans \_ réseau | Lorsqu’un nœud perd la connectivité réseau, il passe à l' \_ État non \_ réseau DRT. À ce stade, l’application peut attendre la restauration de la connectivité réseau et peut fermer DRT.<br/>                                                                                                                                                                                                                    |
| \_erreur DRT     | Une erreur grave s’est produite dans le nœud local. Par exemple, si la mémoire physique de l’ordinateur local est insuffisante.<br/> Lorsqu’un nœud passe à cet État, l’application doit appeler l’API [**DrtClose**](/windows/desktop/api/drt/nf-drt-drtclose) , corriger le problème et réinitialiser le DRT avec [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).<br/>                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du API Table de routage distribué](using-the-distributed-routing-table-api.md)
</dt> <dt>

[Référence de API Table de routage distribué](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 




