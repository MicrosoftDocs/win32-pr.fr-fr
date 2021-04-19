---
description: 'En savoir plus sur : création de bases de données'
title: Création de bases de données
TOCTitle: Creating Databases
ms:assetid: d221144d-f777-4f8a-80ca-2ebdb77108dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294100(v=EXCHG.10)
ms:contentKeyID: 32765715
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: eac708b64837fc79fa8a5060df7deb93ec552e49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534377"
---
# <a name="creating-databases"></a>Création de bases de données


_**S’applique à :** Windows | Serveur Windows_

## <a name="creating-databases"></a>Création de bases de données

La base de données ESE comprend une ou plusieurs tables qui organisent les données par colonnes et par lignes. La base de données ESE est identifiée par le nom et l’ID de base de données. Une base de données ESE ressemble à un fichier unique pour le système d’exploitation Microsoft Windows. Toutefois, en interne, la base de données est stockée sous la forme d’une collection de pages. Ces pages contiennent des métadonnées qui décrivent les données de la base de données, les données elles-mêmes et un ou plusieurs index qui stockent différentes commandes des données. La base de données peut contenir jusqu’à 2 ^ 31 pages, ou 16 téraoctets de données pour une base de données avec des pages de 8 Ko.

L’application crée une instance du moteur de base de données, puis crée une base de données et l’attache à l’instance. Jusqu’à 6 bases de données peuvent être connectées simultanément à une instance avec [JetCreateDatabase](./jetcreatedatabase-function.md) ou [JetAttachDatabase](./jetattachdatabase-function.md). Une ou plusieurs sessions doivent être démarrées dans la base de données, car toutes les opérations ESE suivantes sont effectuées dans le contexte d’une session. Une session distincte doit être ouverte pour chaque thread à l’aide de ESE.

Cette procédure permet d’initialiser le moteur ESE et de créer une base de données.

### <a name="to-initialize-ese-and-create-a-database"></a>Pour initialiser ESE et créer une base de données

1.  [JetCreateInstance](./jetcreateinstance-function.md): crée une instance du moteur de base de données.
    
    **Windows XP et versions ultérieures :** Cette fonction est disponible dans Windows XP et versions ultérieures. Sur Windows 2000, une seule instance est prise en charge et cette instance est créée implicitement

2.  [JetSetSystemParameter](./jetsetsystemparameter-function.md): les paramètres système qui affectent la disposition physique, tels que les JET_paramLogFilePath et JET_paramSystemPath doivent être définis avant d’initialiser l’instance avec [JetInit](./jetinit-function.md). Les paramètres définis à cette étape sont définis pour toutes les bases de données créées dans l’instance. [JetSetSystemParameter](./jetsetsystemparameter-function.md) est la seule fonction qui peut utiliser l’instance avant qu’elle ne soit initialisée avec [JetInit](./jetinit-function.md).

3.  [JetInit](./jetinit-function.md): Initialise l’instance. L’instance doit être initialisée avec [JetInit](./jetinit-function.md) pour pouvoir être utilisée avec d’autres fonctions.

4.  [JetBeginSession](./jetbeginsession-function.md): crée la session pour toutes les transactions suivantes. Toutes les transactions de base de données ont lieu dans le contexte de la session ([JET_SESID](./jet-sesid.md)).

5.  [JetCreateDatabase](./jetcreatedatabase-function.md): crée la base de données et retourne un descripteur à l’ID de base de données ([JET_DBID](./jet-dbid.md)).
    
    Si la base de données existe déjà, l’étape 5 ci-dessus est remplacée par les deux étapes suivantes :
    
    1.  [JetAttachDatabase](./jetattachdatabase-function.md): attache la base de données par son nom à la session
    
    2.  [JetOpenDatabase](./jetopendatabase-function.md): retourne l’ID de base de données utilisé dans les opérations de base de données suivantes.

Une base de données peut être détachée d’une instance ESE à l’aide de [JetDetachDatabase](./jetdetachdatabase-function.md) et d’une version ultérieure attachée à une autre instance avec [JetAttachDatabase](./jetattachdatabase-function.md). Lorsque la base de données est détachée, elle peut être copiée sous la forme d’un fichier unique à l’aide des utilitaires Windows standard. Toutefois, lorsque la base de données est attachée à une instance ESE, elle ne peut pas être copiée, car ESE ouvre les fichiers de base de données en mode exclusif. En outre, si l’instance se bloque, le fichier de base de données ne peut pas être copié seul parce qu’il a besoin des fichiers journaux des transactions qui lui sont associés pour récupérer à partir de ce blocage.
