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
# <a name="creating-and-executing-a-view"></a><span data-ttu-id="28f68-105">Création et exécution d’une vue</span><span class="sxs-lookup"><span data-stu-id="28f68-105">Creating and Executing a View</span></span>

<span data-ttu-id="28f68-106">Vous pouvez créer une vue pour les données obtenues à partir de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="28f68-106">You can create a view for data obtained from Active Directory.</span></span> <span data-ttu-id="28f68-107">N’oubliez pas que seule la définition de la vue est stockée dans SQL Server, et non dans le jeu de résultats réel.</span><span class="sxs-lookup"><span data-stu-id="28f68-107">Be aware that only the view definition is stored in SQL Server, and not the actual result set.</span></span> <span data-ttu-id="28f68-108">Par conséquent, vous pouvez obtenir un résultat différent lorsque vous appelez la vue ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="28f68-108">Therefore, you may get a different result when you invoke the view at a later time.</span></span>

<span data-ttu-id="28f68-109">L’exemple de code suivant montre comment créer une vue.</span><span class="sxs-lookup"><span data-stu-id="28f68-109">The following code sample shows how to create a view.</span></span>


```sql
CREATE VIEW viewADUsers 
AS
SELECT * FROM OpenQuery( ADSI,
    '<LDAP://DC=Fabrikam,DC=com>;(&(objectCategory=Person)(objectClass=user));name, adspath, title;subtree')
```



<span data-ttu-id="28f68-110">Utilisez le code suivant pour appeler une vue.</span><span class="sxs-lookup"><span data-stu-id="28f68-110">Use the following code to invoke a view.</span></span>


```sql
SELECT * from viewADUsers
```



## <a name="related-topics"></a><span data-ttu-id="28f68-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="28f68-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28f68-112">Création d’une jointure hétérogène entre SQL Server et Active Directory</span><span class="sxs-lookup"><span data-stu-id="28f68-112">Creating a Heterogeneous Join between SQL Server and Active Directory</span></span>](creating-a-heterogeneous-join-between-sql-server-and-active-directory.md)
</dt> </dl>

 

 




