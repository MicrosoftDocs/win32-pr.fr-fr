---
description: Les tables du groupe tables système suivent les tables et les colonnes de la base de données d’installation.
ms.assetid: d20be8b6-f456-4f90-aa9e-dc122c20d20c
title: Groupe de tables système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c05bfd06bcff049d2aea847a2bb8d0c4c3fc3d1443a615f75912ac7d4f86d73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623918"
---
# <a name="system-tables-group"></a>Groupe de tables système

Les tables du groupe tables système suivent les tables et les colonnes de la base de données d’installation.

-   La [ \_ table tables](-tables-table.md) effectue le suivi de toutes les tables de la base de données. Cela comprend les tables que vous avez créées pour vos propres actions personnalisées. Interrogez cette table pour savoir si une table existe.
-   La [ \_ Table Columns](-columns-table.md) effectue le suivi des colonnes dans la base de données d’installation. Les colonnes temporaires ne sont pas suivies actuellement par cette table. Interrogez cette table pour savoir si une colonne donnée existe.
-   le [ \_ tableau Flux](-streams-table.md) répertorie les flux de données OLE incorporés.
-   Le [ \_ tableau stockages](-storages-table.md) répertorie les stockages de données OLE incorporés.
-   [ \_ Tableau de validation](-validation-table.md). Le \_ tableau de validation effectue le suivi des types et des plages autorisées de chaque colonne de la base de données. Le \_ tableau de validation est utilisé pendant le processus de validation de la base de données pour s’assurer que toutes les colonnes sont comptabilisées et ont les valeurs correctes. Cette table n’est pas fournie avec la base de données du programme d’installation.

 

 



