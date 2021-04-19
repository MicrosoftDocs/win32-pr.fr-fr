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
# <a name="sql-log-file-schema"></a><span data-ttu-id="9e06b-103">Schéma du fichier journal SQL</span><span class="sxs-lookup"><span data-stu-id="9e06b-103">SQL Log File Schema</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9e06b-104">La prise en charge de PDH pour les bases de données SQL ODBC peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="9e06b-104">PDH support for ODBC SQL databases may be altered or unavailable in the future.</span></span>

<span data-ttu-id="9e06b-105">Les applications peuvent utiliser des API PDH lire et écrire des données de compteur de performance dans les bases de données SQL ODBC compatibles, puis effectuer un traitement supplémentaire par le biais de requêtes SQL.</span><span class="sxs-lookup"><span data-stu-id="9e06b-105">Applications can use PDH APIs read and write performance counter data in compatible ODBC SQL databases and then perform further processing through SQL queries.</span></span> <span data-ttu-id="9e06b-106">Cette section décrit le schéma SQL utilisé pour stocker les compteurs de performance.</span><span class="sxs-lookup"><span data-stu-id="9e06b-106">This section describes the SQL schema used to store performance counters.</span></span> <span data-ttu-id="9e06b-107">Vous pouvez utiliser ces informations pour créer des affichages et des rapports personnalisés.</span><span class="sxs-lookup"><span data-stu-id="9e06b-107">You can use this information to create custom views and reports.</span></span> <span data-ttu-id="9e06b-108">Le schéma se compose des trois tables suivantes :</span><span class="sxs-lookup"><span data-stu-id="9e06b-108">The schema consists of the following three tables:</span></span>

- [<span data-ttu-id="9e06b-109">**CounterData**</span><span class="sxs-lookup"><span data-stu-id="9e06b-109">**CounterData**</span></span>](counterdata.md)
- [<span data-ttu-id="9e06b-110">**CounterDetails**</span><span class="sxs-lookup"><span data-stu-id="9e06b-110">**CounterDetails**</span></span>](counterdetails.md)
- [<span data-ttu-id="9e06b-111">**DisplayToID**</span><span class="sxs-lookup"><span data-stu-id="9e06b-111">**DisplayToID**</span></span>](displaytoid.md)

> [!NOTE]
> <span data-ttu-id="9e06b-112">La prise en charge de PDH pour les bases de données SQL ODBC fonctionne uniquement avec les pilotes SQL ODBC qui prennent en charge les [extensions de copie en bloc (BCP)](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span><span class="sxs-lookup"><span data-stu-id="9e06b-112">PDH support for ODBC SQL databases only works with ODBC SQL drivers that support [Bulk Copy (BCP) Extensions](/sql/relational-databases/native-client-odbc-extensions-bulk-copy-functions/sql-server-driver-extensions-bulk-copy-functions).</span></span>
