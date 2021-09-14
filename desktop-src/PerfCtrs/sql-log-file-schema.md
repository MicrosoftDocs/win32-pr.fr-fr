---
description: les Applications peuvent utiliser PDH pour extraire des compteurs de performances de SQL journaux, ou extraire des compteurs formatés ou bruts directement à partir de la base de données via des requêtes SQL.
ms.assetid: 89515dd9-2d65-4b19-bb7a-ef9e7d146caa
title: SQL Schéma de fichier journal
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 33b988194a8fda4a99f713e0026aeaddb65e9c26
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007165"
---
# <a name="sql-log-file-schema"></a>SQL Schéma de fichier journal

> [!IMPORTANT]
> la prise en charge de PDH pour les bases de données SQL ODBC peut être modifiée ou non disponible à l’avenir.

les Applications peuvent utiliser des api PDH lire et écrire des données de compteur de performance dans les bases de données SQL ODBC compatibles, puis effectuer un traitement supplémentaire via des requêtes SQL. cette section décrit le schéma de SQL utilisé pour stocker les compteurs de performance. Vous pouvez utiliser ces informations pour créer des affichages et des rapports personnalisés. Le schéma se compose des trois tables suivantes :

- [**CounterData**](counterdata.md)
- [**CounterDetails**](counterdetails.md)
- [**DisplayToID**](displaytoid.md)

> [!NOTE]
> la prise en charge de PDH pour les bases de données SQL odbc fonctionne uniquement avec les pilotes de SQL odbc qui prennent en charge les [Extensions de copie en bloc (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).
