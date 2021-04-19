---
title: Cdrom. EJECT, méthode
description: La méthode EJECT éjecte le CD ou DVD du lecteur. | Cdrom. EJECT, méthode
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- méthode EJECT lecteur Windows Media
- EJECT, méthode lecteur Windows Media, classe cdrom
- Classe cdrom lecteur Windows Media, méthode EJECT
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106531491"
---
# <a name="cdromeject-method"></a>Cdrom. EJECT, méthode

La méthode **EJECT** éjecte le CD ou DVD du lecteur.

## <a name="syntax"></a>Syntaxe


```JScript
Cdrom.eject()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si le loquet du lecteur est ouvert, cette méthode ferme la porte.

Pour utiliser cette méthode, l’accès en lecture à la bibliothèque est requis. Pour plus d’informations, consultez [accès à la bibliothèque](library-access.md).

**Lecteur Windows Media 10 Mobile :** Cette méthode n’est pas prise en charge.

## <a name="examples"></a>Exemples

L’exemple suivant crée un élément Button HTML qui utilise *cdrom*. **éjectez** pour ouvrir la porte du lecteur qui a l’index de spécificateur de lecteur zéro. L’objet **Player** a été créé avec ID = "Player".


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| Version<br/>                  | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>                      | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet cdrom**](cdrom-object.md)
</dt> <dt>

[**Player. lecture**](player-playstate.md)
</dt> <dt>

[**Paramètres. mediaAccessRights**](settings-mediaaccessrights.md)
</dt> <dt>

[**Paramètres. requestMediaAccessRights**](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





