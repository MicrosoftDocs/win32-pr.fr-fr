---
title: Élément ServiceInfo
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. L’élément ServiceInfo est l’élément principal du document ServiceInfo.xml.
ms.assetid: d2f9e642-143e-405d-8588-c78e4355b9b9
keywords:
- élément ServiceInfo Lecteur Windows Media
topic_type:
- apiref
api_name:
- ServiceInfo Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b3be774d019555daa75b78edf6a7ed76351e7523712313365dd6c80bfee7cd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763639"
---
# <a name="serviceinfo-element"></a>Élément ServiceInfo

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **serviceInfo** est l’élément principal du document ServiceInfo.xml.

``` syntax
<ServiceInfo
    Version = 1.00
    Key = "service key"
    ContentPartner = "true|false"
/>
```

## <a name="attributes"></a>Attributs



| Terme                                                                                                                                             | Description                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Version__optional_"></span><span id="version__optional_"></span><span id="VERSION__OPTIONAL_"></span>**Version** (facultatif)<br/> | Version du fichier ServiceInfo.xml. la Version 1,00 est prise en charge pour Lecteur Windows Media.<br/>                                                                                                                                                            |
| <span id="Key__required_"></span><span id="key__required_"></span><span id="KEY__REQUIRED_"></span>**Clé** (obligatoire)<br/>                 | Chaîne de clé de service qui identifie de façon unique le magasin en ligne.<br/>                                                                                                                                                                                   |
| <span id="ContentPartner"></span><span id="contentpartner"></span><span id="CONTENTPARTNER"></span>**ContentPartner**<br/>                 | Indique si le magasin en ligne est un magasin de type 1. La valeur « true » indique que le magasin est un magasin de type 1. La valeur « false » indique que le magasin n’est pas un magasin de type 1 ; autrement dit, il s’agit d’un magasin de type 2. La valeur par défaut est « false ».<br/> |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément                                                                                                                                                                            |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Éléments parents | Aucun                                                                                                                                                                               |
| Éléments enfants  | **AlbumInfo**, **BuyCD**, **Color**, **Description**, **FriendlyName**, **HTMLView**, **image**, **Centre** d’informations, **installer**, **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |



 

## <a name="remarks"></a>Remarques

Le tableau suivant détaille les paramètres envoyés avec la demande d’URL. D’autres peuvent être présents à des fins de compatibilité héritée. la requête inclut également tous les paramètres que vous avez spécifiés à l’aide du paramètre de ligne de commande ServiceExtra de Lecteur Windows Media configuration.



| Name         | Valeur                                                                                                                                                               |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *GeoId*      | Windows l’ID d’emplacement géographique. L’ID d’emplacement est spécifié par l’utilisateur dans la zone **emplacement** des paramètres Options régionales et linguistiques du panneau de configuration. |
| *locale*     | ID de paramètres régionaux Lecteur Windows Media.                                                                                                                                     |
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

 

 





