---
description: montre comment s’assurer que votre application s’affiche dans la boîte de dialogue ouvrir avec dans le menu et la boîte de dialogue pour les applications de bureau et qu’elle est disponible par défaut pour l’application Windows Store pour les types de fichiers spécifiés.
ms.assetid: DFCC07A6-BED5-41A8-86DC-130082AE665A
title: Comment inclure une application dans la boîte de dialogue Ouvrir avec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218dcbfe6dc34770208c017f0e13cfda7686430c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231234"
---
# <a name="how-to-include-an-application-in-the-open-with-dialog-box"></a>Comment inclure une application dans la boîte de dialogue Ouvrir avec

montre comment s’assurer que votre application s’affiche dans la boîte de dialogue **ouvrir avec** dans le menu et la boîte de dialogue pour les applications de bureau et qu’elle est disponible par défaut pour l’application Windows Store pour les types de fichiers spécifiés.

## <a name="instructions"></a>Instructions

### <a name="for-each-file-type-add-your-application-to-the-openwithprogids-registry-subkey"></a>Pour chaque type de fichier, ajoutez votre application à la sous-clé de Registre OpenWithProgIds.

Ajoutez votre ProgID sous la forme d’un nom de valeur, avec le type de valeur REG \_ None ou reg \_ SZ et une chaîne vide comme valeur de données.

les exemples de registre suivants montrent des entrées qui associent InfoPath et pour Microsoft Visual Studio avec le type de fichier XML.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithProgids
         InfoPath.Document.3 REG_SZ
         VisualStudio.xml.10.0 REG_SZ
```

## <a name="remarks"></a>Notes

La sous-clé **OpenWithProgids** est préférable à **OpenWithList** pour identifier une application. Pour plus d’informations sur ces sous-clés, consultez [définition des sous-clés facultatives et des attributs d’extension de type de fichier](fa-file-types.md).

**OpenWithList** est destiné uniquement aux applications héritées (il doit être .exe uniquement) sur les systèmes d’exploitation antérieurs à Windows XP.

```
HKEY_CLASSES_ROOT
   .xml
      OpenWithList
         AlternateProgram1.exe
         AlternateProgram2.exe
```

 

 



