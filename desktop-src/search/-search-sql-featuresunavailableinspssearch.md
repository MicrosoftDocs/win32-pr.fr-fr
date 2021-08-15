---
description: le langage de requête de recherche Microsoft Windows est basé sur langage SQL (SQL); Toutefois, il n’effectue pas de recherches dans une base de données relationnelle avec des tables ou des index définis par l’utilisateur.
ms.assetid: e81c436e-3a33-4b00-9860-9a54bc0eebbf
title: SQL fonctionnalités non disponibles dans Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66adb175aa7fae799e0ad9b69916415f12c94ee984d276b5a2238ebb19ec2f06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119716119"
---
# <a name="sql-features-unavailable-in-microsoft-windows-search"></a>SQL fonctionnalités non disponibles dans Microsoft Windows Search

le langage de requête de recherche Microsoft Windows est basé sur langage SQL (SQL); Toutefois, il n’effectue pas de recherches dans une base de données relationnelle avec des tables ou des index définis par l’utilisateur. pour cette raison, de nombreuses instructions de SQL standard et fonctionnalités de syntaxe ne s’appliquent pas. la liste suivante répertorie les fonctionnalités de SQL les plus significatives qui ne sont pas prises en charge dans la recherche Windows.


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
-   SQL-expressions régulières standard (utilisez contains ou LIKE à la place)
-   paramètres pour SQL des requêtes
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

Windows La recherche ne prend pas en charge le dictionnaire des synonymes et les mots parasites.

 

 



