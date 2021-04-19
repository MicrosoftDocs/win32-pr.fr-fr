---
title: Color, élément
description: Remarque Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Color, élément
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Élément de couleur lecteur Windows Media
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530347"
---
# <a name="color-element"></a>Color, élément

> [!Note]  
> Cette section décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’élément Color spécifie la couleur d’arrière-plan des boutons de navigation de la boutique en ligne, du texte du bouton et de la barre des tâches fonctionnalités.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (obligatoire)
</dt> <dd>

Valeur de couleur RVB hexadécimale. Spécifie la couleur d’arrière-plan des boutons et de la barre des tâches.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (obligatoire)
</dt> <dd>

Valeur de couleur RVB hexadécimale. Spécifie la couleur du texte du bouton.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Élément         |
|-----------------|-----------------|
| Éléments parents | **ServiceInfo** |
| Éléments enfants  | Aucune            |



 

## <a name="remarks"></a>Notes

La valeur par défaut de **MediaPlayer** est \# 7C9AD6. La valeur par défaut pour **MediaPlayerText** est \# FFFFFF.

Veillez à utiliser des couleurs qui permettent à l’utilisateur de lire facilement le texte du bouton. Par exemple, vous devez éviter d’utiliser du texte de bouton blanc sur les boutons de couleur claire.

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

 

 





