---
title: TBN_GETOBJECT le code de notification (commctrl. h)
description: Envoyé par un contrôle ToolBar qui utilise le \_ style TBSTYLE REGISTERDROP pour demander un objet cible de déplacement lorsque le pointeur passe sur l’un de ses boutons. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 9fd8516d-fe2e-4f84-9035-e2246aba369a
keywords:
- Contrôles Windows de code de notification TBN_GETOBJECT
topic_type:
- apiref
api_name:
- TBN_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ed144245e351ca4e872128e68fe658bde7c0066
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102860"
---
# <a name="tbn_getobject-notification-code"></a>\_Code de notification TBN GETOBJECT

Envoyé par un contrôle ToolBar qui utilise le style [**TBSTYLE \_ REGISTERDROP**](toolbar-control-and-button-styles.md) pour demander un objet cible de déplacement lorsque le pointeur passe sur l’un de ses boutons. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui contient des informations sur le bouton sur lequel le pointeur a passé et reçoit les données fournies par l’application en réponse à ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application traitant ce code de notification doit retourner zéro.

## <a name="remarks"></a>Notes

Pour fournir un objet, une application doit définir des valeurs dans certains membres de la structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) au niveau de *lParam*. Le membre **pObject** doit être défini sur un pointeur d’objet valide et le membre **HRESULT** doit être défini sur un indicateur de réussite. Pour se conformer aux normes COM (Component Object Model), incrémentez toujours le nombre de références de l’objet lors de la fourniture d’un pointeur d’objet.

Si une application ne fournit pas d’objet, elle doit affecter la valeur **null** à **pObject** et **HRESULT** à un indicateur d’échec.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





