---
description: Le langage de requête de recherche Microsoft Windows est basé sur langage SQL (SQL); Toutefois, il n’effectue pas de recherches dans une base de données relationnelle avec des tables ou des index définis par l’utilisateur.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: Fonctionnalités SQL non disponibles dans Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cf0e082a10a7775ca2d880be6153b7d99b6bc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514587"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>Fonctionnalités SQL non disponibles dans Microsoft Windows Search

Le langage de requête de recherche Microsoft Windows est basé sur langage SQL (SQL); Toutefois, il n’effectue pas de recherches dans une base de données relationnelle avec des tables ou des index définis par l’utilisateur. Pour cette raison, de nombreuses instructions SQL standard et fonctionnalités de syntaxe ne s’appliquent pas. La liste suivante répertorie les fonctionnalités SQL les plus significatives qui ne sont pas prises en charge dans Windows Search.


-   Instructions BATCH
-   \_Fonction de table COALESCE
-   CONVERT, fonction (utilisez à la place les fonctions CAST)
-   CREATE VIEW (instruction)
-   Langage de définition de données
-   DATASOURCE (instruction)
-   Formats de date et d’heure autres que l’horodatage ISO
-   Instruction DELETE
-   GRANT, instruction
-   Schéma d’informations
-   Instruction INSERT
-   Types de données OLE DB
-   Expressions régulières standard SQL (utilisez CONTAINs ou LIKE à la place)
-   Paramètres pour les requêtes SQL
-   Comparaison des colonnes relationnelles
-   En-tête ID de révision
-   REVOKE, instruction
-   Alias d’étendue ou numéros de révision
-   Sélectionner tout (supprime automatiquement les doublons)
-   Procédures stockées
-   Développement de documents structurés
-   UNION ALL
-   Mot clé Unknown
-   Instruction UPDATE

Windows Search ne prend pas en charge les dictionnaires des synonymes et les mots parasites.

 

 



