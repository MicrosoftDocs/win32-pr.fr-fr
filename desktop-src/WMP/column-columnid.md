---
title: COLUMN. columnID
description: L’attribut columnID spécifie ou récupère un ID de colonne dans le contrôle PLAYLIST.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUMN. columnID Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535002"
---
# <a name="columncolumnid"></a>COLUMN. columnID

L’attribut **ColumnID** spécifie ou récupère un ID de colonne dans le contrôle **playlist** .

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Notes

Les valeurs **ColumnID** sont identiques à celles utilisées avec la méthode **getItemInfo** sur un objet **Media** . Une liste peut être obtenue à l’aide du *média*. propriété **attributeCount** pour déterminer le nombre d’attributs disponibles pour un objet **multimédia** donné. Les numéros d’index peuvent ensuite être utilisés avec le *média*. méthode **getAttributeName** pour déterminer les noms des attributs, qui peuvent à leur tour être passés au *média*. **getItemInfo**. La propriété **ColumnID** ne peut être définie que sur ces valeurs, à l’exception de certaines valeurs qui ne peuvent pas être retournées par le *support*. **getAttributeName**. Ces valeurs sont répertoriées ci-dessous.



| Valeur     | Description                                                                        |
|-----------|------------------------------------------------------------------------------------|
| name      | Affiche le nom de l’objet **multimédia** .                                         |
| duration  | Affiche la durée de l’objet **multimédia** .                                     |
| sourceURL | Affiche l’URL de l’objet **multimédia** .                                          |
| status    | Affiche l’état de la copie des fichiers.                                              |
| est      | Affiche la taille du fichier représenté par l’objet **multimédia** .                |
| extension | Affiche l’extension de nom de fichier du fichier que l’objet **multimédia** représente. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément COLUMN**](column-element.md)
</dt> <dt>

[**Objet Media**](media-object.md)
</dt> <dt>

[**Media. attributeCount**](media-attributecount.md)
</dt> <dt>

[**Media. getAttributeName**](media-getattributename.md)
</dt> <dt>

[**Media. getItemInfo**](media-getiteminfo.md)
</dt> </dl>

 

 





