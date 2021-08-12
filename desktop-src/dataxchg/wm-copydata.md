---
title: Message WM_COPYDATA (winuser. h)
description: Une application envoie le \_ message WM COPYDATA pour passer des données à une autre application.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA des données de message Exchange
topic_type:
- apiref
api_name:
- WM_COPYDATA
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eb91b2544bf0ebf0e8767a611b422de9aaaf1d73161e47c7bf27768f4acecb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304484"
---
# <a name="wm_copydata-message"></a>\_Message WM COPYDATA

Une application envoie le message **WM \_ COPYDATA** pour passer des données à une autre application.


```C++
#define WM_COPYDATA                     0x004A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre qui passe les données.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct) qui contient les données à passer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si l’application réceptrice traite ce message, elle doit retourner la **valeur true**; Sinon, elle doit retourner **false**.

## <a name="remarks"></a>Notes

Les données transmises ne doivent pas contenir de pointeurs ou d’autres références à des objets qui ne sont pas accessibles à l’application recevant les données.

Pendant l’envoi de ce message, les données référencées ne doivent pas être modifiées par un autre thread du processus d’envoi.

L’application réceptrice doit tenir compte des données en lecture seule. Le paramètre *lParam* n’est valide que pendant le traitement du message. L’application réceptrice ne doit pas libérer la mémoire référencée par *lParam*. Si l’application réceptrice doit accéder aux données après que [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) a été retourné, elle doit copier les données dans une mémoire tampon locale.

## <a name="examples"></a>Exemples

Pour obtenir un exemple, consultez Utilisation de la [copie de données](using-data-copy.md).

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**COPYDATASTRUCT**](/windows/win32/api/winuser/ns-winuser-copydatastruct)
</dt> </dl>

 

