---
title: External. libraryLocationID
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External. libraryLocationID Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525940"
---
# <a name="externallibrarylocationid"></a>External. libraryLocationID

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **libraryLocationID** récupère l’identificateur de l’élément multimédia spécifique qui est actuellement affiché dans la vue du joueur.

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule.

## <a name="remarks"></a>Notes

Cette propriété fonctionne en association avec la propriété [External. libraryLocationType](external-librarylocationtype.md) . Par exemple, supposons que **libraryLocationType** est égal à CPAlbumID et que **libraryLocationID** est égal à 3. Cela signifie que la vue actuelle dans le lecteur Windows Media affiche l’album dont l’ID est 3. Pour plus d’informations sur la façon dont le lecteur Windows Media caractérise les vues du contenu de la boutique en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).

Certains affichages du lecteur Windows Media sont associés à un élément multimédia particulier. Par exemple, si la vue actuelle représente un album individuel, **libraryLocationType** est égal à CPAlbumID et **LIBRARYLOCATIONID** est l’ID de l’album. Les autres vues ne sont pas associées à un élément multimédia particulier. Par exemple, si la vue actuelle représente tous les albums, **libraryLocationType** est égal à AllCPAlbumIDs, mais il n’existe aucune valeur significative pouvant être assignée à **libraryLocationID**. Dans les cas où la propriété **libraryLocationID** n’a aucune valeur significative, elle est égale à la chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. libraryLocationType**](external-librarylocationtype.md)
</dt> <dt>

[**Emplacement et élément sélectionné**](location-and-selected-item.md)
</dt> </dl>

 

 





