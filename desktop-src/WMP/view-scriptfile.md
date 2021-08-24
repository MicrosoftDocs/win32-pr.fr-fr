---
title: VUE. scriptFile
description: l’attribut scriptFile spécifie les noms de fichiers des fichiers JScript associés.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- affichage. scriptFile Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f22b0fb5f0815c8977a363c033d26c0d68f725e0cdcd546bc2f2c1a7b723c64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119615329"
---
# <a name="viewscriptfile"></a>VUE. scriptFile

l’attribut **scriptFile** spécifie les noms de fichiers des fichiers JScript associés.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en écriture seule sans valeur par défaut. les noms de fichiers de plusieurs fichiers de JScript sont délimités par des points-virgules. Les espaces et les points-virgules de début et suivants ne doivent pas être présents.

## <a name="remarks"></a>Remarques

Le code dans les fichiers spécifiés peut être utilisé par n’importe quel gestionnaire d’événements dans la vue. Le code utilisé par les gestionnaires d’événements dans plusieurs vues peut être placé dans un fichier portant le même nom que le fichier de définition d’apparence, mais avec une extension de .js au lieu d’une extension. WMS. Ce fichier est chargé automatiquement et n’a pas besoin d’être spécifié dans le fichier de définition d’apparence.

## <a name="examples"></a>Exemples


```C++
<VIEW id="theView" scriptFile="theScript.js">
</VIEW>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> </dl>

 

 





