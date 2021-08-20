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
ms.openlocfilehash: e66a0c56ab2f5fc3d5d6a27d996d8b3f3cf7834c61e62113a40af3c42aeb4d59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117932544"
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

 

 





