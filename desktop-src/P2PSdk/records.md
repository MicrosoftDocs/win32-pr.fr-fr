---
description: Les enregistrements sont un moyen de communiquer entre les nœuds d’un graphique ou les membres d’un groupe.
ms.assetid: f4c0869f-f147-4c2b-9418-3b407e22cb16
title: Enregistrements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3066bb6d309ce70a790947f002e1a74eb329c862ffcb0ef2c1766ca315323f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674999"
---
# <a name="records"></a>Enregistrements

Les enregistrements sont un moyen de communiquer entre les nœuds d’un graphique ou les membres d’un groupe. Un enregistrement se compose des deux parties suivantes :

-   En-tête d’enregistrement
-   Contenu de données opaque spécifique

L’en-tête contient des informations sur l’enregistrement, notamment la version, le créateur et le type de données publiées. L’en-tête contient également un champ d’attributs XML qui permet aux applications d’ajouter des attributs nom-valeur qui décrivent les données, et de rechercher efficacement dans la base de données d’enregistrement des enregistrements spécifiques qui ont été publiés précédemment. Le contenu est les données définies par l’application et est opaque pour l’infrastructure de l’homologue.

Lorsqu’un enregistrement est publié, il (en-tête et données) est inondé dans le graphique ou le groupe. Les homologues synchronisés reçoivent ces données et les stockent dans une base de données locale. Les homologues non synchronisés et hors connexion reçoivent les données la prochaine fois qu’ils se connectent et se synchronisent avec le graphique ou le groupe d’homologues.

Pour plus d’informations sur l’utilisation des enregistrements, consultez les rubriques suivantes :

-   [Dépendances d’enregistrement](record-dependencies.md)
-   [Gestion des enregistrements](record-management.md)
-   [Schéma d’attribut d’enregistrement](record-attribute-schema.md)
-   [Format de requête de recherche d’enregistrements](record-search-query-format.md)

 

 



