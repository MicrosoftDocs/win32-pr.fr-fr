---
title: VUE. returnToMediaCenter
description: la méthode returnToMediaCenter retourne l’utilisateur au mode complet de Lecteur Windows Media.
ms.assetid: eebf0679-5704-498c-8eb3-f7710e0cb1fe
keywords:
- affichage. returnToMediaCenter Lecteur Windows Media
topic_type:
- apiref
api_name:
- VIEW.returnToMediaCenter
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9c5f0c86bdd15140ba92261d1f5e8c510d77afc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010767"
---
# <a name="viewreturntomediacenter"></a>VUE. returnToMediaCenter

la méthode **returnToMediaCenter** retourne l’utilisateur au mode complet de Lecteur Windows Media.

``` syntax
        elementID.returnToMediaCenter()
```

## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="examples"></a>Exemples


```JScript
<THEME>
  <VIEW id="View1" backgroundImage="greenstone.bmp">
    <BUTTON id="Open" image="Open.png" 
        onclick="jscript:View1.returnToMediaCenter()">
    </BUTTON>
  </VIEW>
</THEME>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément VIEW**](view-element.md)
</dt> </dl>

 

 





