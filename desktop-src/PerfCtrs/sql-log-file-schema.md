---
description: Les applications peuvent utiliser PDH pour extraire des compteurs de performances des journaux SQL, ou extraire des compteurs formatés ou bruts directement à partir de la base de données par le biais de requêtes SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: Schéma du fichier journal SQL
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534514"
---
# <a name="sql-log-file-schema"></a>Schéma du fichier journal SQL

> [!IMPORTANT]
> La prise en charge de PDH pour les bases de données SQL ODBC peut être modifiée ou non disponible à l’avenir.

Les applications peuvent utiliser des API PDH lire et écrire des données de compteur de performance dans les bases de données SQL ODBC compatibles, puis effectuer un traitement supplémentaire par le biais de requêtes SQL. Cette section décrit le schéma SQL utilisé pour stocker les compteurs de performance. Vous pouvez utiliser ces informations pour créer des affichages et des rapports personnalisés. Le schéma se compose des trois tables suivantes :

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> La prise en charge de PDH pour les bases de données SQL ODBC fonctionne uniquement avec les pilotes SQL ODBC qui prennent en charge les [extensions de copie en bloc (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).
