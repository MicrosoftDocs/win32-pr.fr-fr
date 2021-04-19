---
description: COMREPL fait son travail en trois phases.
ms.assetid: e9ba8db6-ff6f-4e49-b91b-465e3fa77f27
title: Phases de réplication
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dc180e7864f05eb1be60262ee54dd4b71df53bd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515378"
---
# <a name="replication-phases"></a>Phases de réplication

COMREPL fait son travail en trois phases. Le processus de réplication est divisé en différentes phases pour les deux raisons suivantes :

-   Pour séparer le travail effectué afin de préparer la source à partir du travail effectué sur chaque cible
-   Pour retarder la modification de la cible jusqu’à ce que toutes les données soient acquises à partir de la source

Les phases de réplication sont les suivantes.



| Phase         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Phase de préparation | Exporte toutes les applications installées localement sur l’ordinateur source. Cette phase ne touche pas la configuration des cibles.                                                                                                                                                                                                                                                                                                                                                                                                           |
| Phase de copie    | Copie des données sur un ordinateur cible. Toutes les applications exportées sur la source sont copiées vers la cible. Il s’agit d’une opération de copie de fichiers. (Voir [gestion des fichiers](file-management.md).) Cette étape obtient également des données de l’ordinateur source qui ne sont pas encapsulées dans des fichiers d’application exportés (par exemple, les identités d’application). Ces données sont conservées en mémoire dans COMREPL. Cette phase ne touche pas la configuration des ordinateurs cibles.                                                                               |
| Phase d’installation | Installe le catalogue source sur un ordinateur cible. Lorsque cette étape est lancée, toutes les données nécessaires à la reconfiguration de la cible se trouvent dans les fichiers d’application dans le système de fichiers de la cible ou sont conservées en tant que données d’instance dans COMREPL. Cette phase va entraîner la suppression de toutes les applications installées sur la cible (à l’exception des applications décrites dans [ce qui est répliqué](what-gets-replicated.md)) avant l’installation des applications copiées à partir de la source. COMREPL s’installe simultanément sur plusieurs cibles à l’aide d’un thread d’installation par cible. |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des fichiers](file-management.md)
</dt> <dt>

[Journalisation et rapports d’erreurs](logging-and-error-reporting.md)
</dt> <dt>

[Utilisation de COMREPL](using-comrepl.md)
</dt> <dt>

[Ce qui est répliqué](what-gets-replicated.md)
</dt> </dl>

 

 



