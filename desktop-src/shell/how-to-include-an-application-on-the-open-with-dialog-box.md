---
description: Montre comment s’assurer que votre application apparaît dans le menu et la boîte de dialogue Ouvrir avec pour les applications de bureau et qu’elle est disponible en tant qu’application du Windows Store par défaut pour les types de fichiers spécifiés.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Comment inclure une application dans la boîte de dialogue Ouvrir avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864922"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Comment inclure une application dans la boîte de dialogue Ouvrir avec

Montre comment s’assurer que votre application apparaît dans le menu et la boîte de dialogue **Ouvrir avec** pour les applications de bureau et qu’elle est disponible en tant qu’application du Windows Store par défaut pour les types de fichiers spécifiés.

## <a name="instructions"></a>Instructions

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Pour chaque type de fichier, ajoutez votre application à la sous-clé de Registre OpenWithProgIds.

Ajoutez votre ProgID sous la forme d’un nom de valeur, avec le type de valeur REG \_ None ou reg \_ SZ et une chaîne vide comme valeur de données.

Les exemples de registre suivants montrent des entrées qui associent InfoPath et pour Microsoft Visual Studio avec le type de fichier XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Notes

La sous-clé **OpenWithProgids** est préférable à **OpenWithList** pour identifier une application. Pour plus d’informations sur ces sous-clés, consultez [définition des sous-clés facultatives et des attributs d’extension de type de fichier](fa-file-types.md).

**OpenWithList** est destiné uniquement aux applications héritées (il doit s’agir de. exe uniquement) sur les systèmes d’exploitation antérieurs à Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



