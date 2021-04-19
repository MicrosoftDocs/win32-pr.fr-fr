---
title: Settings. muet
description: La propriété muet spécifie et récupère une valeur indiquant si l’audio est muet.
ms.assetid: d6d4b46d-5631-4af7-bd99-21674f067121
keywords:
- Settings. muet Windows Media Player
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
ms.openlocfilehash: 7061439e9e091b2ad1cf6be49873d7e3895132b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538102"
---
# <a name="settingsmute"></a>Settings. muet

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

[**Settings (objet)**](settings-object.md)
</dt> </dl>

 

 





