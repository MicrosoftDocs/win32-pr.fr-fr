---
title: Élément de COPYRIGHT (msfeeds. h)
description: L’élément COPYRIGHT définit une chaîne de texte spécifiant les informations de copyright pour un élément ASX ou ENTRy.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Élément de COPYRIGHT lecteur Windows Media
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543240"
---
# <a name="copyright-element"></a>Élément de COPYRIGHT

L’élément **Copyright** définit une chaîne de texte spécifiant les informations de copyright pour un élément **ASX** ou **entry** .

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments           |
|-----------------|--------------------|
| Éléments parents | **ASX**, **entrée** |
| Éléments enfants  | Aucune               |



 

## <a name="remarks"></a>Notes

Cet élément définit une chaîne de texte qui spécifie les informations de copyright pour un élément **ASX** ou d' **entrée** .

Lorsque cet élément apparaît dans un élément **ASX** , la chaîne de Copyright s’affiche uniquement comme **Afficher** les informations. Lorsque cet élément apparaît dans un élément **entry** , le texte est affiché sous forme d’informations de clips. Chaque **ASX** parent et élément d' **entrée** doit contenir au plus un élément de **Copyright** enfant. Plusieurs éléments de **Copyright** après le premier seront ignorés et ne seront pas affichés.

Les caractères des symboles de copyright et de marque déposée (ou) peuvent ne pas s’afficher correctement si le métafichier n’est pas encodé à l’aide du schéma d’encodage UTF-8. Dans ce cas, pour afficher correctement l’un de ces symboles pour tous les utilisateurs, vous pouvez utiliser les équivalents ASCII (c) et (R) à la place.

Si le métafichier est encodé à l’aide de UTF-8, les symboles de copyright et de marque s’affichent correctement.

## <a name="examples"></a>Exemples


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/>                                 |
| En-tête<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Ajout de caractères de copyright aux sous-fichiers**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





