---
title: Message WM_COPYDATA (winuser. h)
description: Une application envoie le \_ message WM COPYDATA pour passer des données à une autre application.
ms.assetid: d937a260-9fd2-4450-a762-20120f589ab1
keywords:
- WM_COPYDATA l’échange de données de message
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
ms.openlocfilehash: 8160c88b11fa109e8bbfaa06f0f6c45c9b7daed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465615"
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

## <a name="return-value"></a>Valeur retournée

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

 

