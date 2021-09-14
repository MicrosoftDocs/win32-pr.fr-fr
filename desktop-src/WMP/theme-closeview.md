---
title: THÈME. évènement CloseView
description: La méthode évènement CloseView ferme une vue ouverte.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- thème. évènement closeview Lecteur Windows Media
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013198"
---
# <a name="themecloseview"></a>THÈME. évènement CloseView

La méthode **évènement CloseView** ferme une **vue** ouverte.

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*
</dt> <dd>

**Chaîne** spécifiant l' **ID** de la **vue** à fermer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> <dt>

[**THEMe. openView**](theme-openview.md)
</dt> </dl>

 

 





