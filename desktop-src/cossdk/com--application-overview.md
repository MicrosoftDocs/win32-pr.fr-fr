---
description: Une application COM+ est l’unité principale d’administration et de sécurité pour les services de composants et se compose d’un groupe de composants COM qui exécutent généralement des fonctions associées.
ms.assetid: 82e94acb-e7ce-4423-a720-26ee65d0d7b4
title: Vue d’ensemble de l’application COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3365e0c0e7598d8f1eb2f466e8a2cea2d93edf4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013006"
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

 

 



