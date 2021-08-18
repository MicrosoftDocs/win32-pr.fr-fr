---
title: Message WM_RENDERALLFORMATS (winuser. h)
description: Envoyé au propriétaire du presse-papiers avant sa destruction, si le propriétaire du presse-papiers a retardé le rendu d’un ou de plusieurs formats de presse-papiers.
ms.assetid: dff9100f-2dba-467d-be74-a9a9c2b2122b
keywords:
- WM_RENDERALLFORMATS des données de message Exchange
topic_type:
- apiref
api_name:
- WM_RENDERALLFORMATS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77dae9b44cb379ed62c99c601d308fdec500440a9ebad0ffeaffad16ec780dfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636059"
---
# <a name="wm_renderallformats-message"></a>\_Message WM RENDERALLFORMATS

Envoyé au propriétaire du presse-papiers avant sa destruction, si le propriétaire du presse-papiers a retardé le rendu d’un ou de plusieurs formats de presse-papiers. Pour que le contenu du presse-papiers reste disponible pour d’autres applications, le propriétaire du presse-papiers doit restituer les données dans tous les formats qu’il est en charge de générer et placer les données dans le presse-papiers en appelant la fonction [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata) .

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_RENDERALLFORMATS             0x0306
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

Lors de la réponse à un message **WM \_ RENDERALLFORMATS** , l’application doit appeler la fonction [**OpenClipboard**](/windows/win32/api/winuser/nf-winuser-openclipboard) , puis vérifier qu’elle est toujours le propriétaire du presse-papiers en appelant la fonction [**GetClipboardOwner**](/windows/win32/api/winuser/nf-winuser-getclipboardowner) avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata).

L’application doit vérifier qu’elle est toujours le propriétaire du presse-papiers après avoir ouvert le presse-papiers, car après avoir reçu le message **WM \_ RENDERALLFORMATS** , mais avant d’ouvrir le presse-papiers, une autre application a peut-être ouvert et pris possession du presse-papiers, et les données de cette application ne doivent pas être remplacées.

Dans la plupart des cas, l’application ne doit pas appeler la fonction [**EmptyClipboard**](/windows/win32/api/winuser/nf-winuser-emptyclipboard) avant d’appeler [**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata), car cela entraînera l’effacement des formats de presse-papiers que l’application a déjà rendus.

Lorsque l’application est retournée, le système supprime tous les formats non rendus de la liste des formats de presse-papiers disponibles. Pour plus d’informations sur le rendu retardé, consultez [rendu retardé](clipboard-operations.md#delayed-rendering).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EmptyClipboard**](/windows/desktop/api/Winuser/nf-winuser-emptyclipboard)
</dt> <dt>

[**OpenClipboard**](/windows/desktop/api/Winuser/nf-winuser-openclipboard)
</dt> <dt>

[**SetClipboardData**](/windows/win32/api/winuser/nf-winuser-setclipboarddata)
</dt> <dt>

[**\_RENDERFORMAT WM**](wm-renderformat.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

