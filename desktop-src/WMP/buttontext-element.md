---
title: Élément ButtonText
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Élément ButtonText
ms.assetid: 1afe1626-769a-40c8-883a-968ebd995a93
keywords:
- Élément ButtonText Windows Media Player
topic_type:
- apiref
api_name:
- ButtonText Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c94577ad772a5c6fa198bd43f2475d53821da72c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540715"
---
# <a name="buttontext-element"></a>Élément ButtonText

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément **ButtonText** spécifie la chaîne de texte que le lecteur Windows Media affiche pour un bouton du volet des tâches.

``` syntax
<ButtonText>
   text string
</ButtonText>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément                                              |
|-----------------|------------------------------------------------------|
| Éléments parents | **ServiceTask1**, **ServiceTask2**, **ServiceTask3** |
| Éléments enfants  | Aucune                                                 |



 

## <a name="remarks"></a>Notes

Cet élément est requis pour chaque instance de **ServiceTask1**, **ServiceTask2** ou **ServiceTask3**.

> [!Note]  
> Le lecteur Windows Media 10 comporte trois volets de tâches où un magasin en ligne peut afficher ses pages Web. Le magasin en ligne peut choisir d’utiliser un, deux ou les trois volets de tâches. Le lecteur Windows Media 11 n’a qu’un seul volet de tâches, que l’utilisateur peut afficher en cliquant sur l’onglet **magasins en ligne** . le lecteur Windows Media 11 ignore les éléments **ServiceTask2** et **ServiceTask3** .

 

Le lecteur Windows Media peut rogner le texte du bouton pour l’ajuster à l’espace disponible. Le joueur utilise toujours la police Tahoma gras à 8 points pour ce texte. Il y a deux lignes disponibles pour afficher le texte du bouton, mais le lecteur ne renvoie pas automatiquement le texte de la première ligne à la seconde. Pour spécifier un saut de ligne dans le texte du bouton, insérez la nouvelle séquence d’échappement « \\ n » dans votre chaîne de texte.

La chaîne de texte s’affiche également dans le menu **atteindre** de l’interface utilisateur du lecteur Windows Media.

Vous devez tester votre magasin en ligne à l’aide de divers paramètres d’affichage pour vous assurer que le texte s’affiche comme prévu.

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

 

 





