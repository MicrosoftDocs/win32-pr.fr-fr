---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher une entrée de Registre et créer une propriété contenant la valeur du Registre.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862038"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a>Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre

**Pour rechercher une entrée de Registre et créer une propriété contenant la valeur de ce fichier**

1.  N’ajoutez pas la signature à la table de [signature](signature-table.md) ou à la [table CompLocator](complocator-table.md). Si une signature de fichier figure dans la [table AppSearch](appsearch-table.md) et qu’elle n’est pas listée dans les tables signature ou CompLocator, le programme d’installation recherche dans la [table RegLocator](reglocator-table.md).

2.  Spécifiez l’entrée de Registre à rechercher dans la [table RegLocator](reglocator-table.md). Si la signature est absente de la [table de signature](signature-table.md) et que la valeur de la colonne de type est **msidbLocatorTypeRawValue**, la recherche est supposée être pour le nom de clé de Registre spécifique vers lequel pointe la table RegLocator.

    [Table RegLocator](reglocator-table.md) (partielle)

    

    | Signature\_         | Root         | Clé                                                           | Nom                  | Type                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | AppValue<br/> | 2<br/> | **Logiciel** \\ **Microsoft** \\ **MyApp**<br/> <br/> | **SOCIETE**<br/> | **msidbLocatorTypeRawValue**<br/> |

    

     

3.  Enfin, remplissez la [table AppSearch](appsearch-table.md) afin que l' [action AppSearch](appsearch-action.md) retourne la valeur de AppValue. Une fois que le programme d’installation a exécuté l’action AppSearch, la valeur de MYREGVAL est la valeur de AppValue.

    [Table AppSearch](appsearch-table.md) (partielle)

    

    | Propriété            | Signature           |
    |---------------------|---------------------|
    | MYREGVAL<br/> | AppValue<br/> |

    

     

 

 




