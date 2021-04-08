---
title: Code de notification EN_OBJECTPOSITIONS (RichEdit. h)
description: Avertit une fenêtre parente d’un contrôle RichEdit quand le contrôle lit des objets. Un contrôle RichEdit envoie ce code de notification sous la forme d’un \_ message WM Notify.
ms.assetid: 1965185f-8a13-4989-8574-af8b9b30f6b0
keywords:
- Contrôles Windows de code de notification EN_OBJECTPOSITIONS
topic_type:
- apiref
api_name:
- EN_OBJECTPOSITIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35681f6734457eb6b6ebcac1bcb67227cbd3b9e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843678"
---
# <a name="en_objectpositions-notification-code"></a>\_Code de notification en OBJECTPOSITIONS

Avertit une fenêtre parente d’un contrôle RichEdit quand le contrôle lit des objets. Un contrôle RichEdit envoie ce code de notification sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
EN_OBJECTPOSITIONS

    pOjectPositions = (OBJECTPOSITIONS *) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Structure [**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez zéro pour poursuivre l’opération de **lecture** .

Retourne une valeur différente de zéro pour arrêter l’opération de **lecture** .

## <a name="remarks"></a>Notes

Pour recevoir un \_ Code de notification en OBJECTPOSITIONS, spécifiez l’indicateur [**ENM \_ OBJECTPOSITIONS**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) .

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

[**EM \_ SETEVENTMASK**](em-seteventmask.md)
</dt> <dt>

[**OBJECTPOSITIONS**](/windows/desktop/api/Richedit/ns-richedit-objectpositions)
</dt> <dt>

[**\_notification WM**](wm-notify.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

