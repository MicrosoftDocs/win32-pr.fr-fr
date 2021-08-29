---
description: 'En savoir plus sur : le cast du type de données d’une colonne'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Conversion du type de données d’une colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad09572ca80ed433ebba63e84d4b7ca8bacdb6bd5cae45c356e358cbe978b04c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094930"
---
# <a name="casting-the-data-type-of-a-column"></a>Conversion du type de données d’une colonne

Parfois, il peut être nécessaire de convertir les données de type chaîne extraites de documents en un autre type de données, afin de pouvoir effectuer une comparaison appropriée. Effectuez un cast d’un identificateur ou d’un littéral comme un autre type de données en utilisant la syntaxe suivante :


```
CAST (<identifier> | <literal> AS <datatype>)
```



Par exemple :


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappages de type de données](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



