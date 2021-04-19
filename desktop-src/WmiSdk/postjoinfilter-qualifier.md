---
description: Vous pouvez filtrer les instances d’une classe de vue de jointure en affectant une requête WQL au qualificateur PostJoinFilter.
ms.assetid: 926a7262-ea6b-4a5a-8aa7-6ec0ae389031
ms.tgt_platform: multiple
title: Qualificateur PostJoinFilter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PostJoinFilter
api_type:
- NA
api_location: ''
ms.openlocfilehash: ac86aeafefc8057a1612c5007e55e7633c655c59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534642"
---
# <a name="postjoinfilter-qualifier"></a>Qualificateur PostJoinFilter

Vous pouvez filtrer les instances d’une classe de vue de jointure en affectant une requête WQL au qualificateur **PostJoinFilter** . La valeur de la requête WQL est appliquée aux instances de la classe de vue de jointure. Vous pouvez utiliser ce qualificateur pour limiter les instances de votre classe d’affichage à celles qui répondent à des conditions spécifiques. La requête WQL suivante filtre les instances d’une classe join appelée en fonction des instances de [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).


```C++
PostJoinFilter("SELECT * FROM JoinDrive" +
    " WHERE FreeSpace > 1000000" +
    " and Description = \"3 1/2 Inch Floppy Drive\"")
```



L’utilisation de ce qualificateur présente plusieurs restrictions :

-   **PostJoinFilter** est disponible uniquement pour les classes de vue de jointure.
-   Le nom de la classe et les noms de propriété spécifiés dans la requête font référence aux propriétés de la classe d’affichage, et non à la classe source.
-   Aucune exclusion de propriétés n’est autorisée ; seules `SELECT *` les requêtes de type sont autorisées.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Qualificateurs spécifiques au fournisseur de vues**](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

