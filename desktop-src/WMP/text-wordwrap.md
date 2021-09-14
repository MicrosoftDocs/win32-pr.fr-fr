---
title: TEXT. wordWrap
description: L’attribut wordWrap spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé ou désactivé.
ms.assetid: 3bb127d8-42f1-4167-986a-d41690cb5647
keywords:
- TEXT. wordWrap Lecteur Windows Media
topic_type:
- apiref
api_name:
- TEXT.wordWrap
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2b4d030a7e9efdda1bc7503ae3bf8eb5985401
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127232890"
---
# <a name="textwordwrap"></a>TEXT. wordWrap

L’attribut **wordWrap** spécifie ou récupère une valeur indiquant si le retour automatique à la ligne est activé ou désactivé.

``` syntax
        elementID.wordWrap
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                                                                                       |
|-------|---------------------------------------------------------------------------------------------------|
| true  | Le retour automatique à la ligne est activé.                                                                             |
| false | Par défaut. Le retour automatique à la ligne est désactivé. Si le texte ne tient pas dans le contrôle, le texte est rogné. |



 

## <a name="remarks"></a>Notes

Le contrôle Text ne sépare pas les mots. Si un mot dépasse la largeur du contrôle, le retour automatique à la ligne est utilisé pour déplacer le mot vers la ligne suivante. Si un mot unique est plus long que la largeur du contrôle, ce mot est coupé et occupe une seule ligne.

Si l’attribut **Width** n’est pas spécifié, **wordWrap** est ignorée et le contrôle Text est redimensionné au lieu d’habiller le texte.

Si des sauts de ligne sont souhaités dans des emplacements particuliers, ils doivent être spécifiés explicitement dans la **valeur** à l’aide de « &\# 13 ; » ou « \\ r ». si cette dernière forme est utilisée lors de la spécification directe de la valeur, la chaîne doit être précédée de « JScript : » et la valeur réelle doit être entourée de guillemets simples, comme indiqué ci-dessous. Cela n’est pas nécessaire si la valeur est définie dynamiquement à partir d’un gestionnaire d’événements.

Si **wordWrap** a la valeur true et que l' **info-bulle** n’est pas spécifiée, l’info-bulle affiche le texte complet de l’attribut **value** . Si aucune info-bulle n’est souhaitée, affectez la valeur "" (chaîne vide) à l' **info-bulle** .

## <a name="examples"></a>Exemples


```C++
<THEME>
  <VIEW>
    <TEXT
      width = "50"
      height = "200"
      wordWrap = "true"
      backgroundColor = "blue"
      foregroundColor = "white"
      value = "This is a test.&#13;&#13;It is only a test."
    />
    <TEXT
      width = "50"
      height = "200"
      left = "100"
      wordWrap = "true"
      backgroundColor = "green"
      foregroundColor = "white"
      value = "JScript:'This is a test.\r\rIt is only a test.'"
    />
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**AmbientAttributes. Width**](ambientattributes-width.md)
</dt> <dt>

[**Élément de texte**](text-element.md)
</dt> <dt>

[**TEXT. toolTip**](text-tooltip.md)
</dt> <dt>

[**TEXT. Value**](text-value.md)
</dt> </dl>

 

 





