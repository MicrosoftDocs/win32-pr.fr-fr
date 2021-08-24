---
title: PSN_GETOBJECT le code de notification (Prsht. h)
description: Envoyé par une feuille de propriétés pour demander un objet cible de dépôt lorsque le curseur passe sur l’un des boutons du contrôle onglet. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 179ac47c-9b32-4682-866d-1a1fad85080c
keywords:
- PSN_GETOBJECT les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- PSN_GETOBJECT
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e81803a950c7b8eb9a41d31178c8f57d7e4199f802538616d4ced20c5a5cb4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119798629"
---
# <a name="psn_getobject-notification-code"></a>\_Code de notification PSN GETOBJECT

Envoyé par une feuille de propriétés pour demander un objet cible de dépôt lorsque le curseur passe sur l’un des boutons du contrôle onglet. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PSN_GETOBJECT

    lpnmon = (LPNMOBJECTNOTIFY) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) qui, à l’entrée, contient des informations sur le code de notification. Si ce code de notification est traité, vous devez insérer les informations relatives à l’objet dans cette structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application traitant ce code de notification doit retourner zéro.

## <a name="remarks"></a>Remarques

Pour fournir un objet, une application doit définir des valeurs dans certains membres de la structure [**NMOBJECTNOTIFY**](/windows/win32/api/commctrl/ns-commctrl-nmobjectnotify) au niveau de *lParam*. Le membre **pObject** doit être défini sur un pointeur d’objet valide et le membre **HRESULT** doit être défini sur un indicateur de réussite. Pour se conformer aux normes COM (Component Object Model), incrémentez toujours le nombre de références de l’objet lors de la fourniture d’un pointeur d’objet.

Si une application ne fournit pas d’objet, elle doit affecter la valeur **null** à **pObject** et **HRESULT** à un indicateur d’échec.

> [!Note]  
> Ce code de notification n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





