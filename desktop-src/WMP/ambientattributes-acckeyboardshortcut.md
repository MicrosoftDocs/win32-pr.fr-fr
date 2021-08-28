---
title: AmbientAttributes.accKeyboardShortcut
description: L’attribut accKeyboardShortcut spécifie ou récupère une description de raccourci clavier pour tout élément.
ms.assetid: f97cffc9-4e7c-4226-9e02-0ea7f84b7450
keywords:
- AmbientAttributes. accKeyboardShortcut Lecteur Windows Media
topic_type:
- apiref
api_name:
- AmbientAttributes.accKeyboardShortcut
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467304bb9f38ab0683440d2a0ebc5fcc51adb92fbb1d50e8275eb36f256a159
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055208"
---
# <a name="ambientattributesacckeyboardshortcut"></a>AmbientAttributes.accKeyboardShortcut

L’attribut **accKeyboardShortcut** spécifie ou récupère une description de raccourci clavier pour tout élément.

``` syntax
        elementID.accKeyboardShortcut
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture dont la valeur par défaut est «» (chaîne vide). Pour l’élément **Button** , cet attribut a une valeur par défaut « espace ou entrée ». Pour l’élément **Slider** , la valeur par défaut est « flèche droite/haut pour augmenter, flèche gauche/bas pour diminuer ».

## <a name="remarks"></a>Remarques

Cet attribut est utilisé à des fins d’accessibilité. Il permet d’obtenir une description du raccourci clavier pour tout élément à lire à voix haute par un programme de lecture. Cet attribut ne définit pas le raccourci. Le scripteur doit effectuer cette tâche.

Cet attribut s’applique également aux éléments de bouton à l’intérieur du contrôle de groupe de boutons.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs ambiants**](ambient-attributes.md)
</dt> </dl>

 

 





