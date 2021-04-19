---
title: Élément Centre d’informations
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément Centre d’informations
ms.assetid: 1a9cc513-5dd1-46d8-9409-16413695b4c8
keywords:
- Élément Centre d’informations lecteur Windows Media
topic_type:
- apiref
api_name:
- InfoCenter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ef62e0f6b41090642400a7f0a8b88af72818da4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530418"
---
# <a name="infocenter-element"></a>Élément Centre d’informations

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **Centre** d’informations spécifie l’URL de la page Web que le lecteur Windows Media affiche dans la fonctionnalité d’affichage du centre d’informations de en **cours de lecture** lorsque le magasin en ligne est actif.

``` syntax
<InfoCenter
    URL = "URL"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="URL__required_"></span><span id="url__required_"></span><span id="URL__REQUIRED_"></span>**URL** (obligatoire)
</dt> <dd>

URL de la page Web affichée par le lecteur Windows Media.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | Aucune            |



 

## <a name="remarks"></a>Notes

L’utilisateur contrôle quand l’affichage du centre d’informations est actif.

Pour récupérer des informations sur l’élément multimédia en cours de lecture, vous devez incorporer une instance du contrôle du lecteur Windows Media dans votre page Web et utiliser le modèle objet du lecteur.

Le tableau suivant détaille les paramètres envoyés avec la demande d’URL. D’autres peuvent être présents à des fins de compatibilité héritée.



| Nom         | Valeur                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | ID d’emplacement géographique Windows. L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration. |
| *locale*     | ID de paramètres régionaux du lecteur Windows Media.                                                                                                                                     |
| *UserLocale* | ID de paramètres régionaux Windows. Les paramètres régionaux sont spécifiés par l’utilisateur dans la zone **standards et formats** des paramètres Options régionales et linguistiques du panneau de configuration.        |
| *version*    | Numéro de version du lecteur Windows Media en utilisant le format suivant : 10.0. x. xxxx ou 11.0. x. xxxx.                                                                         |



 

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

 

 





