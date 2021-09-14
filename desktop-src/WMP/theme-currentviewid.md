---
title: THÈME. currentViewID
description: L’attribut currentViewID spécifie ou récupère la vue actuellement affichée.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- thème. currentViewID Lecteur Windows Media
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013196"
---
# <a name="themecurrentviewid"></a>THÈME. currentViewID

L’attribut **currentViewID** spécifie ou récupère la **vue** actuellement affichée.

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture spécifiant l' **ID** de la **vue** actuelle. Il n'a aucune valeur par défaut.

## <a name="remarks"></a>Remarques

La spécification de **currentViewID** ferme automatiquement la **currentView** existante (vers laquelle pointe l’attribut **View** global) et ouvre la **vue** spécifiée.

## <a name="examples"></a>Exemples


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément THEMe**](theme-element.md)
</dt> </dl>

 

 





