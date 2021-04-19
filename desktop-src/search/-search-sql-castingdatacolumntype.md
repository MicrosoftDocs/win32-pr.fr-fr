---
description: 'En savoir plus sur : le cast du type de données d’une colonne'
ms.assetid: 78a137a9-ef69-4ce3-8a96-73e722951300
title: Conversion du type de données d’une colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71a72a84c915d066d4b088719808687a965d86b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515823"
---
# <a name="casting-the-data-type-of-a-column"></a><span data-ttu-id="942f6-103">Conversion du type de données d’une colonne</span><span class="sxs-lookup"><span data-stu-id="942f6-103">Casting the Data Type of a Column</span></span>

<span data-ttu-id="942f6-104">Parfois, il peut être nécessaire de convertir les données de type chaîne extraites de documents en un autre type de données, afin de pouvoir effectuer une comparaison appropriée.</span><span class="sxs-lookup"><span data-stu-id="942f6-104">At times you may need to cast string data extracted from documents as another data type, so that an appropriate comparison can be made.</span></span> <span data-ttu-id="942f6-105">Effectuez un cast d’un identificateur ou d’un littéral comme un autre type de données en utilisant la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="942f6-105">Cast an identifier or literal as another data type using the following syntax:</span></span>


```
CAST (<identifier> | <literal> AS <datatype>)
```



<span data-ttu-id="942f6-106">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="942f6-106">For example:</span></span>


```
CAST ('10000' AS DBTYPE_I4)
            
CAST (System.DateCreated AS DBTYPE_WSTR)
```



## <a name="related-topics"></a><span data-ttu-id="942f6-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="942f6-107">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="942f6-108">Mappages de type de données</span><span class="sxs-lookup"><span data-stu-id="942f6-108">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
</dt> </dl>

 

 



