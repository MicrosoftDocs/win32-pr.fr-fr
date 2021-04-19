---
description: Les classes suivantes sont déclarées et associées à des identificateurs de classe (CLSID) dans wmcodecdsp. h.
ms.assetid: f82d92dc-fbce-4274-a10f-72fa8dd776cc
title: Identificateurs de classe pour l’analyseur de table des matières (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5108855c687085e77ce36aa14b3424732e25572
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514967"
---
# <a name="class-identifiers-for-table-of-contents-parser"></a>Identificateurs de classe pour l’analyseur de table des matières

Les classes suivantes sont déclarées et associées à des identificateurs de classe (CLSID) dans wmcodecdsp. h.



| Nom de classe       | Nom convivial de l’objet |
|------------------|----------------------|
| CTocEntry        | Entrée de la table des matières            |
| CTocEntryList    | Liste des entrées de la table des matières       |
| CToc             | Table des matières                  |
| CTocCollection   | Collection TOC       |
| CTocParser       | Analyseur de table des matières           |
| CTocGeneratorDmo | Générateur de table des matières        |



 

Le tableau précédent fournit un nom d’objet convivial pour chaque classe. Cette documentation utilise ces noms conviviaux pour faire référence aux instances des classes. Par exemple, la documentation fait référence à une instance de la classe CTocEntry en tant qu’objet d’entrée de table des matières.

Dans le code, vous pouvez utiliser **\_ \_ uuidof** pour faire référence aux CLSID. Par exemple, vous pouvez utiliser le code suivant pour faire référence au CLSID pour CTocGeneratorDmo.


```C++
__uuidof(CTocGeneratorDmo)
```



### <a name="clsid-constants-defined-in-wmcodecdsph"></a>Constantes CLSID définies dans Wmcodecdsp. h

Au lieu d’utiliser **\_ \_ uuidof**, vous pouvez utiliser des constantes pour faire référence aux CLSID. Les constantes suivantes sont définies dans wmcodecdsp. h



| Nom de classe     | CLSID, constante        |
|----------------|-----------------------|
| CTocEntry      | CLSID \_ CTocEntry      |
| CTocEntryList  | CLSID \_ CTocEntryList  |
| CToc           | CLSID \_ CToc           |
| CTocCollection | CLSID \_ CTocCollection |
| CTocParser     | CLSID \_ CTocParser     |



 

### <a name="clsid-constants-defined-in-wmcodecdspuuidlib"></a>Constantes CLSID définies dans Wmcodecdspuuid. lib

La constante CLSID suivante est déclarée, mais pas définie, dans wmcodecdsp. h. Pour l’utiliser dans le code, vous devez effectuer une liaison par rapport à wmcodecdspuuid. lib.



| Nom de classe       | CLSID, constante          |
|------------------|-------------------------|
| CTocGeneratorDmo | CLSID \_ CTocGeneratorDmo |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmvdspa.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets de l’analyseur de table des matières](toc-parser-objects.md)
</dt> </dl>

 

 




