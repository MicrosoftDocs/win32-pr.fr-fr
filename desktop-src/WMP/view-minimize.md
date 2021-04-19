---
title: AFFICHER. réduire
description: La méthode Minimize réduit la vue.
ms.assetid: 97c257fa-aa4f-4e6f-bc49-fa54db63b59b
keywords:
- AFFICHER. réduire le lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.minimize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e01c35ad5a77c5a78a705d0188f771e0466a761
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542685"
---
# <a name="viewminimize"></a>AFFICHER. réduire

La méthode **Minimize** réduit la **vue**.

``` syntax
        elementID.minimize()
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples


```JScript
<THEME>
  <VIEW id="View1">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.minimize()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> <dt>

[**AFFICHER. agrandir**](view-maximize.md)
</dt> </dl>

 

 





