---
title: VUE. scriptFile
description: L’attribut scriptFile spécifie les noms de fichiers des fichiers JScript associés.
ms.assetid: c285c467-5ba7-4f46-b316-977e833c3cdd
keywords:
- AFFICHER. scriptFile lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.scriptFile
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac7f447f1934c2589b7ae52b3a24e2dcb2b1ef7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541421"
---
# <a name="viewscriptfile"></a>VUE. scriptFile

L’attribut **scriptFile** spécifie les noms de fichiers des fichiers JScript associés.

``` syntax
        elementID.scriptFile
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en écriture seule sans valeur par défaut. Les noms de fichiers de plusieurs fichiers JScript sont délimités par des points-virgules. Les espaces et les points-virgules de début et suivants ne doivent pas être présents.

## <a name="remarks"></a>Notes

Le code dans les fichiers spécifiés peut être utilisé par n’importe quel gestionnaire d’événements dans la vue. Le code utilisé par les gestionnaires d’événements dans plusieurs vues peut être placé dans un fichier portant le même nom que le fichier de définition d’apparence, mais avec une extension. js au lieu d’une extension. WMS. Ce fichier est chargé automatiquement et n’a pas besoin d’être spécifié dans le fichier de définition d’apparence.

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

 

 





