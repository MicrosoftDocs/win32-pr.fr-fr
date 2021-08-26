---
description: COM+ fournit un modèle objet d’administration qui expose toutes les fonctionnalités de l’outil d’administration Services de composants, lui-même un serveur frontal graphique écrit par-dessus les objets d’administration.
ms.assetid: f302eb02-2ef5-42ee-a18f-59f7e60b38df
title: Automatisation de l’administration COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cb7370c3b1a90324b612108e9ec1ef17c7030d3372d303da74ced95298ab02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029839"
---
# <a name="automating-com-administration"></a>Automatisation de l’administration COM+

COM+ fournit un modèle objet d’administration qui expose toutes les fonctionnalités de l’outil d’administration Services de composants, lui-même un serveur frontal graphique écrit par-dessus les objets d’administration. Vous pouvez utiliser ces objets, fournis par la bibliothèque administration des services de composants (comadmin), pour automatiser toutes les tâches de l’administration des services et applications COM+.

Les objets comadmin vous permettent de lire et d’écrire des informations qui sont stockées sur le catalogue COM+, le magasin de données sous-jacent qui contient toutes les données de configuration COM+.

Vous pouvez utiliser ces objets pour effectuer les opérations suivantes :

-   Créez et configurez des applications COM+.
-   Installez et exportez les applications COM+ existantes.
-   Gérer les applications COM+ installées.
-   Gérez et configurez les services.
-   Administrer à distance les services de composants sur un autre ordinateur.

vous pouvez utiliser les objets comadmins de scriptable avec n’importe quel langage compatible Automation, tel que Microsoft Visual Basic et Visual Basic Script. Vous pouvez développer des scripts légers ou des outils d’administration à usage général. Vous pouvez par exemple effectuer les opérations suivantes :

-   Écrire des scripts pour effectuer des tâches d’administration courantes.
-   Écrivez des scripts pour automatiser les processus dans le développement d’applications COM+.
-   Développez des outils à usage général pour l’administration et la surveillance des services de composants.
-   Développez des exécutables d’installation pour installer et déployer votre application COM+.

La bibliothèque comadmin offre une compatibilité descendante avec la bibliothèque d’administration MTS 2,0. La plupart des codes d’administration MTS 2,0 existants continuent de fonctionner, bien qu’avec quelques exceptions. (Voir [bibliothèque d’administration MTS](mts-administration-library.md).)

Pour automatiser efficacement l’administration, vous devez être familiarisé avec les tâches d’administration telles qu’elles sont effectuées avec l’outil d’administration Services de composants.

Pour obtenir une description complète des objets comadmin et des interfaces correspondantes, consultez la documentation de référence COM+ pour les classes et les interfaces suivantes :

-   [**COMAdminCatalog**](comadmincatalog.md)
-   [**COMAdminCatalogCollection**](comadmincatalogcollection.md)
-   [**COMAdminCatalogObject**](comadmincatalogobject.md)
-   [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
-   [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
-   [**ICatalogCollection**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogcollection)
-   [**ICatalogObject**](/windows/desktop/api/ComAdmin/nn-comadmin-icatalogobject)

Les rubriques suivantes de cette section fournissent une vue d’ensemble de l’automatisation de l’administration à l’aide des objets comadmin :

-   [Vue d’ensemble des objets comadmin](overview-of-the-comadmin-objects.md)
-   [Récupération des regroupements sur le catalogue COM+](retrieving-collections-on-the-com--catalog.md)
-   [Définition des propriétés et enregistrement des modifications dans le catalogue COM+](setting-properties-and-saving-changes-to-the-com--catalog.md)
-   [Gestion des erreurs d’administration COM+](handling-com--administration-errors.md)
-   [Opérations d’administration COM+ dans les transactions](com--administration-operations-within-transactions.md)
-   [Exemple d’introduction utilisant le catalogue d’administration COM+](introductory-example-using-the-com--administration-catalog.md)

 

 



