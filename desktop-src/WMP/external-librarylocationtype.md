---
title: External. libraryLocationType
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External. libraryLocationType Windows Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539514"
---
# <a name="externallibrarylocationtype"></a>External. libraryLocationType

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **libraryLocationType** récupère une [constante d’emplacement de bibliothèque](library-location-constants.md) qui indique le type de la vue actuelle dans le lecteur Windows Media.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule qui contient l’une des constantes d’emplacement de la bibliothèque.

## <a name="remarks"></a>Notes

Cette propriété fonctionne en association avec la propriété [External. libraryLocationID](external-librarylocationid.md) . Par exemple, supposons que **libraryLocationType** est égal à CPAlbumID et que **libraryLocationID** est égal à 3. Cela signifie que la vue actuelle dans le lecteur Windows Media affiche l’album dont l’ID est 3. Pour plus d’informations sur la façon dont le lecteur Windows Media caractérise les vues du contenu de la boutique en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. libraryLocationID**](external-librarylocationid.md)
</dt> <dt>

[**Emplacement et élément sélectionné**](location-and-selected-item.md)
</dt> </dl>

 

 





