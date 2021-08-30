---
title: Paramètres. muet
description: La propriété muet spécifie et récupère une valeur indiquant si l’audio est muet.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Paramètres. muet Lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.mute
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c3a6d510f2b5906ea604a783f59b6246ac8b302a2a77d8941237361ee888eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002389"
---
# <a name="settingsmute"></a>Paramètres. muet

La propriété **muet** spécifie et récupère une valeur indiquant si l’audio est muet.

## <a name="syntax"></a>Syntaxe

Player. Settings. muet

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **valeur booléenne** en lecture/écriture.



| Valeur | Description                  |
|-------|------------------------------|
| true  | L’audio est muet.              |
| false | Par défaut. L’audio n’est pas muet. |



 

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément de case à cocher HTML qui permet à l’utilisateur d’activer ou de désactiver le son. L’objet **Player** a été créé avec ID = "Player".


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX"  ID = MUTE  
             onClick = "
                        /* Use the CHECKBOX state to set 
                           the mute property. */
                        Player.settings.mute = MUTE.checked;
">
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





