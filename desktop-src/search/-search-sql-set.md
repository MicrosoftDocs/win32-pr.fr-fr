---
description: L’instruction SET spécifie les options PROPERTYNAME et RANKMETHOD pour la requête.
ms.assetid: 14b833a5-5e6a-4f1a-b15e-3b32d7e0df37
title: Instruction SET
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55124f75c1462dbd377ff0de02a55596fbd3ab71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112414"
---
# <a name="set-statement"></a>Instruction SET

L’instruction SET spécifie les options PROPERTYNAME et RANKMETHOD pour la requête.

## <a name="propertyname"></a>PROPERTYNAME

Vous pouvez associer une propriété à un alias convivial pour la requête à l’aide de la syntaxe suivante :


```
SET PROPERTYNAME <guid_format> 
PROPID <property_id> | <property_name> 
AS <column_alias> [<type_clause>] 
```



## <a name="rankmethod"></a>RANKMETHOD

Vous pouvez spécifier la méthode rank pour les requêtes avec le terme ISABOUT à l’aide de la syntaxe suivante :


```
SET RANKMETHOD <rankmethod>      
```



Les méthodes RANKMETHOD qui peuvent être spécifiées à l’aide de l’instruction SET sont le coefficient JACCARD, le coefficient des dés et le produit interne.

 

 



