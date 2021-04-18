---
title: THEMe. openView
description: La méthode openView ouvre une vue dans une nouvelle fenêtre.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- THEMe. openView lecteur Windows Media
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540290"
---
# <a name="themeopenview"></a>THEMe. openView

La méthode **openView** ouvre une **vue** dans une nouvelle fenêtre.

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="view"></span><span id="VIEW"></span>*affichage*
</dt> <dd>

**Chaîne** spécifiant l' **ID** de la **vue** à ouvrir.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples


```JScript
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

[**THÈME. évènement CloseView**](theme-closeview.md)
</dt> <dt>

[**THÈME. openViewRelative**](theme-openviewrelative.md)
</dt> </dl>

 

 





