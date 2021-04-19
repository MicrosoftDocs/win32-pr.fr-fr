---
title: Élément Description
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Description, élément
ms.assetid: 4d9ff447-e5a4-46b1-b599-87202077abfb
keywords:
- Élément de description du lecteur Windows Media
topic_type:
- apiref
api_name:
- Description Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4318a7936f4713d3ff89a2fa73731eea0cdd97db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523934"
---
# <a name="description-element"></a>Élément Description

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **Description** spécifie une description marketing de la boutique en ligne qui s’affiche pendant la première expérience de l’utilisateur avec une installation du lecteur Windows Media.

``` syntax
<Description>
    text string
</Description>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | Aucune            |



 

## <a name="remarks"></a>Notes

La longueur de la description doit être inférieure ou égale à 255 caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple de document ServiceInfo pour une boutique en ligne de type 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Document ServiceInfo**](serviceinfo-document.md)
</dt> </dl>

 

 





