---
description: à partir de Windows XP, le panneau de configuration prend en charge la catégorisation des éléments du panneau de configuration. Les éléments sont inscrits pour apparaître dans une ou plusieurs catégories. Impossible de créer des catégories.
title: Affectation des catégories du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.assetid: e189b57d-c066-4f28-b1d5-3e05d6c6eeb2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b6785a786bfe80f5a5b13bc5e9dfbe39507a2c9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478485"
---
# <a name="assigning-control-panel-categories"></a>Affectation des catégories du panneau de configuration

à partir de Windows XP, le panneau de configuration prend en charge la catégorisation des éléments du panneau de configuration. Les éléments sont inscrits pour apparaître dans une ou plusieurs catégories. Impossible de créer des catégories.

Pour inscrire un élément du panneau de configuration dans une ou plusieurs catégories, ajoutez des valeurs comme expliqué dans la section inscription de l’élément du panneau de configuration de l' [exécutable](registering-control-panel-items.md) ou [inscription](registering-control-panel-items.md) de l’élément du panneau de configuration de l’enregistrement des éléments du panneau de [configuration, le](registering-control-panel-items.md)cas échéant.




| ID de la catégorie | nom de la catégorie (Windows 7) | nom de la catégorie (Windows Vista) | nom de la catégorie (Windows XP) | 
|-------------|---------------------------|-------------------------------|----------------------------|
| 0 | « Tous les éléments du panneau de configuration » | « Options supplémentaires »<blockquote>[!Note]<br />Tout élément du panneau de configuration qui ne spécifie pas d’ID de catégorie apparaît dans cette catégorie.</blockquote><br /> | « Autres options du panneau de configuration »<blockquote>[!Note]<br />Tout élément du panneau de configuration qui ne spécifie pas d’ID de catégorie apparaît dans cette catégorie.</blockquote><br /> | 
| 1 | « Apparence et personnalisation » | « Apparence et personnalisation » | « Apparence et thèmes » | 
| 2 | « Matériel et son » | « Matériel et son » | « Imprimantes et autres matériels » | 
| 3 | « Réseau et Internet » | « Réseau et Internet » | « Connexions réseau et Internet » | 
| 4 | N'est plus utilisé. Tout élément qui s’ajoute uniquement à la catégorie 4 apparaît dans la catégorie 2 (matériel et audio). | N'est plus utilisé. Tout élément qui s’ajoute uniquement à la catégorie 4 apparaît dans la catégorie 2 (matériel et audio). | « Sons, voix et périphériques audio » | 
| 5 | « Système et sécurité » | « Système et maintenance » | « Performances et maintenance » | 
| 6 | « Horloge, langue et région » | « Horloge, langue et région » | « Date, heure, langue et options régionales » | 
| 7 | « Facilité d’accès » | « Facilité d’accès » | « Options d’accessibilité » | 
| 8 | Installés | Installés | « Ajout/suppression de programmes » | 
| 9 | « Comptes d’utilisateur »<blockquote>[!Note]<br />Lorsque vous n’êtes pas connecté à un domaine, on parle de « comptes d’utilisateur et de sécurité des familles ».</blockquote><br /> | « Comptes d’utilisateur »<blockquote>[!Note]<br />Lorsque vous n’êtes pas connecté à un domaine, on parle de « comptes d’utilisateur et de sécurité des familles ».</blockquote><br /> | « Comptes d’utilisateur » | 
| 10 | N'est plus utilisé. Les éléments inscrits dans cette catégorie s’affichent dans la catégorie 5 (système et sécurité). | « Security » | « Security Center »<blockquote>[!Note]<br />disponible uniquement dans Windows XP Service Pack 2 (SP2) ou version ultérieure.</blockquote><br /> | 
| 11 | N'est plus utilisé. Les éléments inscrits dans cette catégorie s’affichent dans la catégorie 0 (tous les éléments du panneau de configuration). | « ORDINATEUR portable »<blockquote>[!Note]<br />Cette catégorie est visible uniquement sur les ordinateurs portables.</blockquote><br /> | Non utilisé. | 




 

dans Windows XP, les catégories **ajout/suppression de programmes** et **comptes d’utilisateur** fonctionnent différemment des autres catégories dans le panneau de configuration. Lorsqu’un ou plusieurs éléments sont ajoutés à l’une de ces deux catégories, le lien associé dans le panneau de configuration ouvre une page de catégorie. Les éléments inscrits s’affichent dans la partie inférieure de la page sous le titre « ou sélectionnent une icône du panneau de configuration ». quand aucun élément n’est inscrit pour l’une de ces catégories, le lien associé dans le panneau de configuration appelle directement l’élément de Windows standard pour cette catégorie. dans Windows Vista et versions ultérieures, la catégorie **programmes** et la catégorie **comptes d’utilisateurs** ne disposent pas de cette propriété.

la catégorie **Security Center** , disponible uniquement dans Windows XP SP2, est également un peu non standard. Cliquez sur cette catégorie pour ouvrir la page **Security Center** dans une nouvelle fenêtre. Les éléments inscrits pour **Security Center** s’affichent dans la partie inférieure de cette page sous le titre **gérer les paramètres de sécurité pour :**. Cliquer sur une icône ouvre l’élément du panneau de configuration.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Éléments du panneau de configuration](control-panel-applications.md)
</dt> <dt>

[Conseils sur l’expérience utilisateur](user-experience-guidelines.md)
</dt> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Utilisation de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Traitement des messages du panneau de configuration](message-processing.md)
</dt> <dt>

[Exécution des éléments du panneau de configuration](executing-control-panel-items.md)
</dt> <dt>

[Extension des éléments du panneau de configuration système](extending-system-control-panel-items.md)
</dt> <dt>

[Création de liens de tâches pouvant faire l’objet d’une recherche pour un élément du panneau de configuration](creating-searchable-task-links.md)
</dt> <dt>

[accès au panneau de configuration en Mode Coffre sous Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 




