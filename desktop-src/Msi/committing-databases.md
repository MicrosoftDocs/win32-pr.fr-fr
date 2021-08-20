---
description: Les modifications apportées à la base de données d’installation ne sont pas écrites dans la base de données tant que vous n’avez pas appelé MsiDatabaseCommit.
ms.assetid: 65271631-457c-4d3e-9384-126d2c9d63d7
title: Validation des bases de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1ab5f4da5b82fb3b6b2ac7d2371bd8046ab87a23d2ef43b6473f7e36a4771a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145348"
---
# <a name="committing-databases"></a>Validation des bases de données

Les modifications apportées à la base de données d’installation ne sont pas écrites dans la base de données tant que vous n’avez pas appelé [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit).

**Pour garantir la finalisation des modifications apportées à une base de données**

1.  Vérifiez si une table est écrite quand vous appelez [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) en appelant [**MsiDatabaseIsTablePersistent**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseistablepersistenta).
2.  Appelez la fonction [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit) pour finaliser les modifications apportées à la base de données.

Les modifications apportées dans une base de données sont accumulées et ne sont pas reflétées dans la base de données réelle tant que vous n’avez pas appelé [**MsiDatabaseCommit**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasecommit). Les colonnes ou les lignes temporaires ne sont pas validées dans la base de données. Quand une base de données est fermée, toutes les modifications apportées depuis le dernier **MsiDatabaseCommit** sont automatiquement annulées.

 

 



