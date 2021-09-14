---
description: COMREPL est un utilitaire qui réplique le catalogue COM+ d’un ordinateur source donné sur un ou plusieurs ordinateurs cibles.
ms.assetid: 11aa7603-61f1-4af0-b6f9-81f484788052
title: L’utilitaire de réplication COMREPL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a08ecd77a679b6fc150e7a91fc0214eb829792dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127310882"
---
# <a name="the-comrepl-replication-utility"></a>L’utilitaire de réplication COMREPL

COMREPL est un utilitaire qui réplique le catalogue COM+ d’un ordinateur source donné sur un ou plusieurs ordinateurs cibles. Pensez à l’ordinateur source qui représente une « configuration principale ». COMREPL est utilisé pour répliquer cette configuration principale afin de conserver un ensemble d’ordinateurs configurés de façon identique.

L’unité de réplication est l’ensemble de la configuration COM+ sur l’ordinateur maître. Toutes les applications COM+ sur le serveur maître sont répliquées sur les ordinateurs cibles. C’est tout ou rien. En outre, toutes les applications COM+ précédemment installées sur les ordinateurs cibles, à l’exception des applications COM+ préinstallées, seront supprimées dans le cadre du processus de réplication.

COMREPL réplique uniquement les données de configuration COM+. Cela comprend les applications COM+ et les paramètres d’ordinateur spécifiques à COM+. Microsoft Internet Information Services (IIS) a un utilitaire similaire (IISSync), qui utilise COMREPL pour répliquer la configuration IIS et COM+.

Pour plus d’informations sur le lancement et l’utilisation de COMREPL, consultez les rubriques suivantes dans cette section :

-   [Utilisation de COMREPL](using-comrepl.md)
-   [Ce qui est répliqué](what-gets-replicated.md)
-   [Phases de réplication](replication-phases.md)
-   [Gestion des fichiers](file-management.md)
-   [Journalisation et rapports d’erreurs](logging-and-error-reporting.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de packages d’installation pour les applications COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Déploiement de proxys d’application](deploying-application-proxies.md)
</dt> <dt>

[Le catalogue COM+](the-com--catalog.md)
</dt> </dl>

 

 



