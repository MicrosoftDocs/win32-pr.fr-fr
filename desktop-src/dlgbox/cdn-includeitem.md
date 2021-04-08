---
title: CDN_INCLUDEITEM le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous pour déterminer si la boîte de dialogue doit afficher un élément dans la liste d’éléments d’un dossier de l’interpréteur de commandes.
ms.assetid: 0972a78d-e058-4bac-85bd-fbd4c3885552
keywords:
- Boîtes de dialogue CDN_INCLUDEITEM code de notification
topic_type:
- apiref
api_name:
- CDN_INCLUDEITEM
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67cbe830c644657425eb087dd64884da17a9a0c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742845"
---
# <a name="cdn_includeitem-notification-code"></a>\_Code de notification CDN INCLUDEITEM

\[À compter de Windows Vista, les boîtes de dialogue **ouvrir** et **Enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** pour déterminer si la boîte de dialogue doit afficher un élément dans la liste d’éléments d’un dossier de l’interpréteur de commandes. Lorsque l’utilisateur ouvre un dossier, la boîte de dialogue envoie une notification **\_ INCLUDEITEM CDN** pour chaque élément du dossier. La boîte de dialogue envoie cette notification uniquement si l’indicateur **OFN \_ ENABLEINCLUDENOTIFY** a été défini lors de la création de la boîte de dialogue.

Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INCLUDEITEM         (CDN_FIRST - 0x0007)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) .

La structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le message de notification **CDN \_ INCLUDEITEM** .

Le membre des **fibres** discontinues de la structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) est un pointeur vers une interface pour le dossier dont les éléments sont énumérés. Le membre **PIDL** est un pointeur vers une liste d’identificateurs d’éléments qui identifie l’élément par rapport au dossier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) retourne la valeur zéro, la boîte de dialogue exclut l’élément de la liste d’éléments.

Pour inclure l’élément, retournez une valeur différente de zéro à partir de la procédure de raccordement.

## <a name="remarks"></a>Notes

La boîte de dialogue comprend toujours les éléments qui ont à la fois les attributs **SFGAO \_ FileSystem** et **SFGAO \_ FILESYSANCESTOR** , quelle que soit la valeur retournée par **CDN \_ INCLUDEITEM**.

## <a name="requirements"></a>Configuration requise



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

[**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

