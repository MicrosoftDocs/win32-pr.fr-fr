---
title: Création et exécution d’une vue
description: Vous pouvez créer une vue pour les données obtenues à partir de Active Directory. N’oubliez pas que seule la définition de la vue est stockée dans SQL Server, et non dans le jeu de résultats réel. Par conséquent, vous pouvez obtenir un résultat différent lorsque vous appelez la vue ultérieurement.
ms.assetid: c2892517-11e1-489f-a2f2-5118bccd605b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a47a0956acb8f9d0268240e677f62a2e395b4fed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379597"
---
# <a name="creating-and-executing-a-view"></a>Création et exécution d’une vue

Vous pouvez créer une vue pour les données obtenues à partir de Active Directory. N’oubliez pas que seule la définition de la vue est stockée dans SQL Server, et non dans le jeu de résultats réel. Par conséquent, vous pouvez obtenir un résultat différent lorsque vous appelez la vue ultérieurement.

L’exemple de code suivant montre comment créer une vue.


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



Utilisez le code suivant pour appeler une vue.


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une jointure hétérogène entre SQL Server et Active Directory](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




