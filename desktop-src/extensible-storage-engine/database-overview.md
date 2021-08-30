---
description: 'En savoir plus sur : vue d’ensemble de la base de données'
title: Présentation de la base de données
TOCTitle: Database Overview
ms:assetid: 6e4ebfab-8bd2-4fcf-9d91-2148a693596c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269290(v=EXCHG.10)
ms:contentKeyID: 32765582
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: c0b90e1faec861c995c5f9f789af9b4dda68cfb68c704c6ace6d3b367a2e209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119976353"
---
# <a name="database-overview"></a>Présentation de la base de données


_**S’applique à :** Windows | Windows Serveurs_

## <a name="database-overview"></a>Présentation de la base de données

La base de données ESE est une méthode d’accès séquentiel indexé (ISAM) pour le stockage et la récupération des données. Une base de données ESE est stockée dans un fichier unique et se compose d’une ou plusieurs tables définies par l’utilisateur. Les données sont organisées dans des enregistrements de la table avec une ou plusieurs colonnes définies par l’utilisateur. Les index créés fournissent une organisation différente pour l’ensemble de l’ensemble ou un sous-ensemble d’enregistrements dans la table. À l’aide de l’API ESE, les applications peuvent créer des curseurs qui parcourent les enregistrements de la base de données dans différents ordres séquentiels. Les éléments de la table sont définis ci-dessous :

  - **Colonne**: la colonne est un champ de la table qui stocke un type spécifique d’informations. Les colonnes peuvent être fixes ou de longueur variable, en fonction du type de données qui y est stocké. Certaines colonnes, telles que les colonnes avec balises, ne prennent pas d’espace quand **null** ou sont définies sur la valeur par défaut et peuvent contenir plusieurs valeurs.

  - **Enregistrements**: un enregistrement est une collection de valeurs de colonnes qui ont une identité unique comme défini par la clé primaire.

  - **Index**: l’index est une collection de colonnes clés qui définissent un classement stocké des enregistrements dans la table. L’index cluster, ou principal, définit l’ordre dans lequel les enregistrements sont stockés dans la table. Vous pouvez définir plusieurs index afin de spécifier des ordres différents de traversée dans les enregistrements de la table. Un index peut également limiter l’ensemble des enregistrements visibles en fonction de critères simples tels que la présence ou l’absence d’une valeur de colonne clé particulière dans l’enregistrement.

  - **Curseur**: le curseur indique l’enregistrement en cours dans la table et navigue vers les enregistrements de la table à l’aide de l’index actuel. Le curseur contient également des informations sur l’état de la mise à jour actuellement préparée.

Les colonnes et les index peuvent être ajoutés ou supprimés de la table à tout moment. Bien qu’il soit possible de définir plusieurs index, les données de la table sont physiquement stockées et ordonnées de manière logique en fonction de la définition d’index primaire dans une arborescence B +. Chaque index secondaire est stocké dans une arborescence B + distincte qui contient uniquement des pointeurs logiques vers les données réelles stockées dans la table primaire. Si aucun index n’est défini, les enregistrements de la table sont stockés dans une arborescence B + dans l’ordre d’insertion et sont désignés par le terme « index séquentiel ».

Le diagramme ci-dessous montre comment les données de la table sont stockées dans une arborescence B + en fonction de l’index primaire. L’index primaire est pour le nom et l’ID, et un index secondaire est créé pour le numéro de bureau de l’employé. Les entrées de l’index secondaire sont stockées dans une arborescence B + distincte qui contient uniquement des pointeurs vers les enregistrements stockés dans la table primaire. Par exemple, le numéro de bureau 12348 dans la table secondaire est lié à l’enregistrement 3 dans la table primaire. Enregistrement 3 contient les valeurs de colonne pour l’employé dans Office 12348. Pour plus d’informations, consultez la rubrique [indexation dans le tableau](./indexing-in-the-table.md) .

![ESE_Documentation_tableandrow2](images/Gg269290.ESE_Documentation_tableandrow2(EXCHG.10).gif "ESE_Documentation_tableandrow2")
