---
description: Une application COM+ est l’unité principale d’administration et de sécurité pour les services de composants et se compose d’un groupe de composants COM qui exécutent généralement des fonctions associées.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Vue d’ensemble de l’application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c964d760b5ba0ef260bc9dcb0658b564a4b211075692ce6301a0445eee0eb7a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991873"
---
# <a name="com-application-overview"></a>Vue d’ensemble de l’application COM+

Une application COM+ est l’unité principale d’administration et de sécurité pour les services de composants et se compose d’un groupe de composants COM qui exécutent généralement des fonctions associées. Ces composants se composent davantage d’interfaces et de méthodes, comme indiqué dans l’illustration suivante.

![Diagramme qui affiche des interfaces et des méthodes à l’intérieur des zones, par ordre de méthode dans une interface à l’intérieur d’une application COM+.](images/487518b4-0460-4b2d-a834-c4ea57755ffd.png)

Vous pouvez utiliser l’outil d’administration Services de composants pour créer des applications COM+, ajouter des composants aux applications et définir les attributs d’une application et de ses composants.

En créant des groupes logiques de composants COM en tant qu’applications COM+, vous pouvez tirer parti des avantages suivants de COM+ :

-   Une étendue de déploiement pour les composants COM.
-   Étendue de configuration commune pour les composants COM, y compris les limites de sécurité et la mise en file d’attente.
-   Stockage d’attributs de composant non fournis par le développeur de composants (par exemple, transactions et synchronisation).
-   Les bibliothèques de liens dynamiques (dll) du composant sont chargées dans des processus (DLLHost.exe) à la demande.
-   Processus serveur managés pour héberger des composants.
-   Création et gestion des threads utilisés par les composants.
-   Accès à l’objet de contexte pour les distributeurs de ressources, ce qui permet aux ressources acquises d’être automatiquement associées au contexte. (Pour plus d’informations sur les composants COM et les contextes, consultez [contextes com+](com--contexts.md).)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Développement d’applications COM+](developing-com--applications.md)
</dt> <dt>

[Parties d’une application COM+](parts-of-a-com--application.md)
</dt> <dt>

[Types d’applications COM+](types-of-com--applications.md)
</dt> </dl>

 

 



