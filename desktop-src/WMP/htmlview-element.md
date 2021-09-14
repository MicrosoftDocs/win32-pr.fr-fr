---
title: Élément HTMLView
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément HTMLView spécifie l’URL de base d’une page Web HTMLView.
ms.assetid: 741db1ed-9452-4cae-9185-15668abe06b3
keywords:
- élément HTMLView Lecteur Windows Media
topic_type:
- apiref
api_name:
- HTMLView Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f11a60e41b7f78be3440e16a7d2b3934f75e8ee3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416228"
---
# <a name="htmlview-element"></a>Élément HTMLView

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **HTMLView** spécifie l’URL de base d’une page Web HTMLView.

``` syntax
<HTMLView
    BaseURL = "URL"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="BaseURL__required_"></span><span id="baseurl__required_"></span><span id="BASEURL__REQUIRED_"></span>**BaseURL** (obligatoire)
</dt> <dd>

URL de Base de la page web HTMLView que Lecteur Windows Media affiche.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | None            |



 

## <a name="remarks"></a>Notes

Vous pouvez utiliser cet élément pour intégrer la fonctionnalité HTMLView à votre magasin en ligne. Si le domaine de l’URL spécifiée par le magasin en ligne actuel correspond à celui de la page Web HTMLView, le commutateur à **présent** se produit sans intervention de l’utilisateur et le contenu de HTMLView est affiché. dans le cas contraire, Lecteur Windows Media demande à l’utilisateur l’autorisation d’afficher le contenu HTMLView.

Par exemple, si l’URL de la page Web HTMLView est https://www.proseware.com/html/HTMLView.htm et que l’URL de l’attribut **BaseURL** est spécifiée en tant que https://www.proseware.com , la page Web HTMLView s’affiche sans demander confirmation à l’utilisateur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**affichage des Pages Web dans les Lecteur Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Élément PARAM**](param-element.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





