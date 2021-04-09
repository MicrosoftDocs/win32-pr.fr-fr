---
title: Code de notification EN_SAVECLIPBOARD (RichEdit. h)
description: Avertit la fenêtre parente du contrôle RichEdit que le contrôle est en fermeture et que le presse-papiers contient des informations. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: e8b95e80-6494-4153-8e78-ede9ed17c66f
keywords:
- Contrôles Windows de code de notification EN_SAVECLIPBOARD
topic_type:
- apiref
api_name:
- EN_SAVECLIPBOARD
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1fd7c6e11ed82a7f77483c692dd68f860395c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843437"
---
# <a name="en_saveclipboard-notification-code"></a>\_Code de notification en SAVECLIPBOARD

Avertit la fenêtre parente du contrôle RichEdit que le contrôle est en fermeture et que le presse-papiers contient des informations. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_SAVECLIPBOARD

    penSaveClipboard = (ENSAVECLIPBOARD *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard) qui contient des informations sur les informations du presse-papiers.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro si le presse-papiers doit être mis à la disposition d’autres applications.

Retourne une valeur différente de zéro si le presse-papiers ne doit pas être enregistré.

## <a name="remarks"></a>Notes

La fenêtre parente reçoit toujours un [**message \_ de notification WM**](wm-notify.md) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**ENSAVECLIPBOARD**](/windows/desktop/api/Richedit/ns-richedit-ensaveclipboard)
</dt> </dl>

 

 





