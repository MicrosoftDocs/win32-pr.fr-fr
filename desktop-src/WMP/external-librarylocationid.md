---
title: External. libraryLocationID
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. libraryLocationID
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- External. libraryLocationID Lecteur Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192388"
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

Cette propriété fonctionne en association avec la propriété [External. libraryLocationType](external-librarylocationtype.md) . Par exemple, supposons que **libraryLocationType** est égal à CPAlbumID et que **libraryLocationID** est égal à 3. cela signifie que la vue actuelle dans Lecteur Windows Media affiche l’album dont l’ID est 3. pour plus d’informations sur la façon dont Lecteur Windows Media caractérise les vues du contenu du magasin en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).

certaines vues de Lecteur Windows Media sont associées à un élément multimédia particulier. Par exemple, si la vue actuelle représente un album individuel, **libraryLocationType** est égal à CPAlbumID et **LIBRARYLOCATIONID** est l’ID de l’album. Les autres vues ne sont pas associées à un élément multimédia particulier. Par exemple, si la vue actuelle représente tous les albums, **libraryLocationType** est égal à AllCPAlbumIDs, mais il n’existe aucune valeur significative pouvant être assignée à **libraryLocationID**. Dans les cas où la propriété **libraryLocationID** n’a aucune valeur significative, elle est égale à la chaîne vide.

## <a name="requirements"></a>Spécifications



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

 

 





