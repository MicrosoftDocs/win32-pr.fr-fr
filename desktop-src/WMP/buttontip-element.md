---
title: Élément ButtonTip
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément ButtonTip
ms.assetid: 93e5d0c8-8d2d-45c1-9d47-bbd0b6eb8b88
keywords:
- élément ButtonTip Lecteur Windows Media
topic_type:
- apiref
api_name:
- ButtonTip Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb7fb4a162a8e77fea7548265825af6c6cbda75dbafadf05fe32cb664c4d563f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764299"
---
# <a name="buttontip-element"></a>Élément ButtonTip

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **ButtonTip** spécifie la chaîne de texte qui s’affiche lorsque l’utilisateur pointe sur un bouton du volet des tâches.

``` syntax
<ButtonTip>
   text string
</ButtonTip>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément                                              |
|-----------------|------------------------------------------------------|
| Éléments parents | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Éléments enfants  | None                                                 |



 

## <a name="remarks"></a>Remarques

Cet élément est facultatif pour chaque instance de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**. si cet élément n’est pas fourni, Lecteur Windows Media utilise le texte du bouton comme valeur par défaut.

> [!Note]  
> Lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages web. Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches. Lecteur Windows Media 11 n’a qu’un seul volet de tâches, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** . Lecteur Windows Media 11 ignore les éléments **ServiceTask2** et **ServiceTask3** .

 

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

 

 





