---
description: Avant d’utiliser une base de données, vous devez d’abord obtenir un descripteur.
ms.assetid: 53cf73bc-4d52-471c-8384-46d106a36e38
title: Obtention d’un descripteur de base de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a325c7c69bed4141de8f553a344b20b5f3c61bfe28a1594105c0a853b7075744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145562"
---
# <a name="obtaining-a-database-handle"></a>Obtention d’un descripteur de base de données

Avant d’utiliser une base de données, vous devez d’abord obtenir un descripteur.

**Pour accéder aux informations relatives à une base de données de programme d’installation**

1.  Obtenez un descripteur de la base de données de deux façons :
    -   Si une installation est en cours, récupérez un descripteur de la base de données active en appelant la fonction [**MsiGetActiveDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msigetactivedatabase) .
    -   Si une installation n’est pas en cours, ouvrez une base de données spécifiée en appelant la fonction [**MsiOpenDatabase**](/windows/desktop/api/Msiquery/nf-msiquery-msiopendatabasea) .
2.  Une fois la base de données ouverte, vous pouvez appeler des fonctions pour obtenir des informations sur la base de données ou pour manipuler la base de données.
    -   créez un objet de **vue** et spécifiez une SQL requête de la base de données ouverte en appelant la fonction [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .
    -   Obtenez un enregistrement qui contient toutes les clés primaires d’une table spécifiée dans la base de données ouverte en appelant la fonction [**MsiDatabaseGetPrimaryKeys**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegetprimarykeysa) .
    -   Vérifiez l’état actuel d’une base de données ouverte en appelant la fonction [**MsiGetDatabaseState**](/windows/desktop/api/Msiquery/nf-msiquery-msigetdatabasestate) . Avec la fonction **MsiGetDatabaseState** , vous pouvez déterminer l’état de lecture/écriture d’une base de données ou si le descripteur est valide.

 

 



