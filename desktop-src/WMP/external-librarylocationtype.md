---
title: External. libraryLocationType
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. libraryLocationType
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- External. libraryLocationType Lecteur Windows Media
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
ms.openlocfilehash: 54e254ce6258cf667884e2815508b413ed1455b1b6924bfebb4edc900da048c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119736199"
---
# <a name="externallibrarylocationtype"></a>External. libraryLocationType

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

la propriété **libraryLocationType** récupère une [constante d’emplacement de bibliothèque](library-location-constants.md) qui indique le type de la vue actuelle dans Lecteur Windows Media.

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture seule qui contient l’une des constantes d’emplacement de la bibliothèque.

## <a name="remarks"></a>Remarques

Cette propriété fonctionne en association avec la propriété [External. libraryLocationID](external-librarylocationid.md) . Par exemple, supposons que **libraryLocationType** est égal à CPAlbumID et que **libraryLocationID** est égal à 3. cela signifie que la vue actuelle dans Lecteur Windows Media affiche l’album dont l’ID est 3. pour plus d’informations sur la façon dont Lecteur Windows Media caractérise les vues du contenu du magasin en ligne, consultez [emplacement et élément sélectionné](location-and-selected-item.md).

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

 

 





