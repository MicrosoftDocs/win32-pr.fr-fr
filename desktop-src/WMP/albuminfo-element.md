---
title: Élément AlbumInfo
description: l’élément AlbumInfo spécifie l’URL de la page web qui Lecteur Windows Media s’affiche lorsque l’utilisateur choisit d’afficher plus d’informations sur un élément multimédia particulier.
ms.assetid: c872e95a-3723-4ce8-8d61-e2bc9e12c785
keywords:
- élément AlbumInfo Lecteur Windows Media
topic_type:
- apiref
api_name:
- AlbumInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a5f8fab7da8f61ce6ee5451ebcef4dc33517aae2396f0817fac19222713db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055377"
---
# <a name="albuminfo-element"></a>Élément AlbumInfo

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’élément **AlbumInfo** spécifie l’URL de la page web qui Lecteur Windows Media s’affiche lorsque l’utilisateur choisit d’afficher plus d’informations sur un élément multimédia particulier.

``` syntax
<AlbumInfo
   URL = "URL"
/>
      
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)
</dt> <dd>

URL de la page web que Lecteur Windows Media affiche.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | None            |



 

## <a name="remarks"></a>Remarques

quand l’utilisateur clique sur un bouton dans Lecteur Windows Media pour afficher des informations supplémentaires sur un élément multimédia particulier, le lecteur envoie la demande d’URL avec des paramètres attachés à l’aide d’un séparateur de chaîne de requête de point d’interrogation ( ?). Le tableau suivant détaille les paramètres envoyés avec la demande d’URL. D’autres peuvent être présents à des fins de compatibilité héritée.



| Nom         | Valeur                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Album*      | Valeur de l’attribut **WM/AlbumTitle** pour l’élément multimédia.                                                                                                        |
| *Peinture*     | Valeur de l’attribut **WM/AlbumArtist** , s’il en existe un, ou la valeur de l’attribut **Author** pour l’élément multimédia.                                         |
| *GeoId*      | Windows l’ID d’emplacement géographique. L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration. |
| *locale*     | ID de paramètres régionaux Lecteur Windows Media.                                                                                                                                     |
| *Titre*      | Valeur de l’attribut **title** pour l’élément multimédia.                                                                                                                |
| *UFID*       | Valeur de l’attribut **WM/UniqueFileIdentifier** pour l’élément multimédia.                                                                                              |
| *UserLocale* | ID de paramètres régionaux Windows. Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.        |
| *version*    | Lecteur Windows Media numéro de version en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





