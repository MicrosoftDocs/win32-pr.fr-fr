---
title: Image, élément (kit de développement logiciel (SDK) WMP)
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Image, élément (kit de développement logiciel (SDK) WMP)
ms.assetid: 06804c26-e847-43a7-bb75-60da600c7d4f
keywords:
- Élément image lecteur Windows Media
topic_type:
- apiref
api_name:
- Image Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c10b62365453f395c1aaf373e355c21260900f8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540594"
---
# <a name="image-element-wmp-sdk"></a>Image, élément (kit de développement logiciel (SDK) WMP)

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **image** spécifie les images que le lecteur Windows Media affiche à l’utilisateur pour représenter le magasin en ligne.

``` syntax
<Image
    EulaURL = "URL"
    MenuURL = "URL"
    ServiceLargeURL = "URL"
    ServiceSmallURL = "URL"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="EulaURL__required_for_type_1_stores__ignored_for_type_2_"></span><span id="eulaurl__required_for_type_1_stores__ignored_for_type_2_"></span><span id="EULAURL__REQUIRED_FOR_TYPE_1_STORES__IGNORED_FOR_TYPE_2_"></span>**EulaURL** (requis pour les magasins de type 1, ignoré pour le type 2)
</dt> <dd>

URL du logo affiché par le lecteur Windows Media dans la boîte de dialogue contrat de licence utilisateur final (CLUF). Il doit s’agir d’une image PNG de 80 x 80 pixels.

</dd> <dt>

<span id="MenuURL__optional_"></span><span id="menuurl__optional_"></span><span id="MENUURL__OPTIONAL_"></span>**MenuURL** (facultatif)
</dt> <dd>

URL de l’image affichée par le lecteur Windows Media dans le menu Services. Cette image doit être de 15 x 15 pixels.

</dd> <dt>

<span id="ServiceLargeURL__optional_"></span><span id="servicelargeurl__optional_"></span><span id="SERVICELARGEURL__OPTIONAL_"></span>**ServiceLargeURL** (facultatif)
</dt> <dd>

Pour une boutique en ligne de type 1, il s’agit de l’URL de l’image affichée par le lecteur Windows Media sur l’onglet **magasins en ligne** . Pour le lecteur Windows Media 11, cette image doit être de 45 pixels de large sur 13 pixels de haut. Pour le lecteur Windows Media 12, cette image doit être de 45 pixels de large sur 30 pixels de haut. Pour prendre en charge les versions 11 et 12 du lecteur Windows Media, vous devez fournir deux documents ServiceInfo.xml distincts, chacun pointant vers l’image de taille appropriée pour ServiceLargeURL.

Pour un magasin de type 2 en ligne, il s’agit de l’URL de l’image que le lecteur Windows Media affiche en regard de l’onglet **magasins en ligne** ou à côté des boutons du volet de tâches. Cette image doit être de 30 x 30 pixels.

</dd> <dt>

<span id="ServiceSmallURL__optional_"></span><span id="servicesmallurl__optional_"></span><span id="SERVICESMALLURL__OPTIONAL_"></span>**ServiceSmallURL** (facultatif)
</dt> <dd>

URL du logo qui s’affiche avec la description marketing spécifiée dans l’élément **Description** . S’il n’est pas fourni, il est vide. (Tous les types, facultatifs) Il doit s’agir d’une image PNG de 45 pixels de large et de 13 pixels de haut.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | Aucune            |



 

## <a name="remarks"></a>Notes

Les formats d’image pris en charge sont. gif,. jpg,. bmp et. png (format recommandé). L’utilisation de la transparence Web est prise en charge et recommandée. Les fichiers GIF animés ne sont pas pris en charge.

Si vous ne fournissez pas de valeur pour **MenuURL**, le lecteur Windows Media n’affiche aucun graphique dans le menu de votre magasin en ligne.

Vous pouvez fournir une image animée pour ServiceLargeURL. Dans le lecteur Windows Media 10 ou 11, l’image est animée. Dans le lecteur Windows Media 12, seule la première image de l’image est affichée. Pour fournir une image animée, créez un fichier image unique qui contient des frames successifs de votre animation. Par exemple, pour une image d’une largeur de 30 pixels et de 30 pixels de haut, vous pouvez fournir 20 images successives côte à côte dans une image de 600 pixels de large et de 30 pixels de haut. Le lecteur Windows Media animera automatiquement une image de ce type en présentant les 20 images individuelles l’une après l’autre. Cette animation se produit une seule fois lors de l’ouverture du magasin en ligne. elle ne se répète pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





