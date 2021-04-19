---
title: CDN_SHAREVIOLATION le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous d’un navigateur quand l’utilisateur clique sur le bouton OK et qu’une violation de partage réseau se produit pour le fichier sélectionné.
ms.assetid: a62ca550-0997-4379-aaaf-a5bc9414bd69
keywords:
- Boîtes de dialogue CDN_SHAREVIOLATION code de notification
topic_type:
- apiref
api_name:
- CDN_SHAREVIOLATION
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e79d9c48d3e80d14d83de07c03f7db119ea8e78
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590696"
---
# <a name="cdn_shareviolation-notification-code"></a>\_Code de notification CDN SHAREVIOLATION

\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/windows/win32/shell/common-file-dialog). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** d’un navigateur quand l’utilisateur clique sur le bouton **OK** et qu’une violation de partage réseau se produit pour le fichier sélectionné.

Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_SHAREVIOLATION      (CDN_FIRST - 0x0003)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) . Le membre **pszFile** de cette structure est un pointeur vers le nom du fichier qui avait la violation de partage. La structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ SHAREVIOLATION** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

La valeur de retour indique comment la boîte de dialogue doit gérer la violation de partage.

Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue affiche le message d’avertissement standard pour une violation de partage.

Pour empêcher l’affichage du message d’avertissement standard, retournez une valeur différente de zéro à partir de la procédure de raccordement et appelez la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) pour définir l’une des valeurs de **\_ MSGRESULT DWL** suivantes.



| Code/valeur de retour                                                                                                                                           | Description                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Fait en sorte que la boîte de dialogue retourne le nom du fichier sans avertir l’utilisateur de la violation de partage.<br/>  |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Fait en sorte que la boîte de dialogue rejette le nom de fichier sans avertir l’utilisateur de la violation de partage. <br/> |



 

## <a name="remarks"></a>Remarques

Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .

Le système envoie cette notification uniquement si la valeur **OFN \_ SHAREAWARE** n’a pas été spécifiée lors de la création de la boîte de dialogue.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

