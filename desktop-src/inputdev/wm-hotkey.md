---
title: Message WM_HOTKEY (winuser. h)
description: Publié lorsque l’utilisateur appuie sur une touche d’accès rapide enregistrée par la fonction RegisterHotKey. Le message est placé en haut de la file d’attente de messages associée au thread qui a enregistré la touche d’accès rapide.
ms.assetid: 28d87c2f-b2bb-4176-910b-0addea6beb93
keywords:
- WM_HOTKEY l’entrée du clavier et de la souris du message
topic_type:
- apiref
api_name:
- WM_HOTKEY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f09e81a964542a6a8166ae54a0df4d7127466c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413114"
---
# <a name="wm_hotkey-message"></a>\_Message de raccourci WM

Publié lorsque l’utilisateur appuie sur une touche d’accès rapide enregistrée par la fonction [**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey) . Le message est placé en haut de la file d’attente de messages associée au thread qui a enregistré la touche d’accès rapide.


```C++
#define WM_HOTKEY                       0x0312
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de la touche d’accès rapide qui a généré le message. Si le message a été généré par une touche d’accès rapide définie par le système, ce paramètre aura l’une des valeurs suivantes.



| Valeur                                                                                                                                                                                                                             | Signification                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="IDHOT_SNAPDESKTOP"></span><span id="idhot_snapdesktop"></span><dl> <dt>**IDHOT \_ SNAPDESKTOP**</dt> <dt>-2</dt> </dl> | La touche d’accès rapide « Snap Desktop » a été enfoncée.<br/> |
| <span id="IDHOT_SNAPWINDOW"></span><span id="idhot_snapwindow"></span><dl> <dt>**IDHOT \_ SNAPWINDOW**</dt> <dt>-1</dt> </dl>    | La touche d’accès rapide « fenêtre d’alignement » a été enfoncée.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie les clés qui doivent être enfoncées en association avec la clé spécifiée par le mot de poids fort pour générer le message de **\_ raccourci WM** . Ce mot peut être une ou plusieurs des valeurs suivantes. Le mot de poids fort spécifie le code de touche virtuelle de la touche d’accès rapide.



| Valeur                                                                                                                                                                                                               | Signification                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MOD_ALT"></span><span id="mod_alt"></span><dl> <dt>**Mod \_ ALT**</dt> <dt>0x0001</dt> </dl>             | La touche ALT était maintenue enfoncée.<br/>                                                                                                                                      |
| <span id="MOD_CONTROL"></span><span id="mod_control"></span><dl> <dt>**Mod \_**</dt> <dt>0X0002</dt> de contrôle </dl> | La touche CTRL était maintenue enfoncée.<br/>                                                                                                                                     |
| <span id="MOD_SHIFT"></span><span id="mod_shift"></span><dl> <dt>**Mod \_ SHIFT**</dt> <dt>0x0004</dt> </dl>       | La touche Maj était maintenue enfoncée.<br/>                                                                                                                                    |
| <span id="MOD_WIN"></span><span id="mod_win"></span><dl> <dt>**Mod \_ WIN**</dt> <dt>0x0008</dt> </dl>             | La touche WINDOWS était maintenue enfoncée. ces clés sont étiquetées avec le logo Windows. les raccourcis clavier qui impliquent la clé de Windows sont réservés à une utilisation par le système d’exploitation.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

**WM \_ La touche** d’accès rapide n’est pas liée aux touches d’accès rapide [**WM \_ GETHOTKEY**](wm-gethotkey.md) et [**WM \_ SETHOTKEY**](wm-sethotkey.md) . Le message de **\_ raccourci WM** est envoyé pour les touches d’accès rapide génériques, tandis que les messages **WM \_ SETHOTKEY** et **WM \_ GETHOTKEY** sont liés aux touches d’activation de fenêtre.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**RegisterHotKey**](/windows/win32/api/winuser/nf-winuser-registerhotkey)
</dt> <dt>

[**\_GETHOTKEY WM**](wm-gethotkey.md)
</dt> <dt>

[**\_SETHOTKEY WM**](wm-sethotkey.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Entrée au clavier](keyboard-input.md)
</dt> </dl>

 

