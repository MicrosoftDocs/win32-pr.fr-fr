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
ms.openlocfilehash: 445ea8626d7ecc6c1c72cd13eebfc9811ae229b772787eae2625224d830bc25e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721077"
---
# <a name="cdn_includeitem-notification-code"></a>CDN \_ Code de notification INCLUDEITEM

\[à partir de Windows Vista, les boîtes de dialogue **ouvrir** et **enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** pour déterminer si la boîte de dialogue doit afficher un élément dans la liste d’éléments d’un dossier de l’interpréteur de commandes. lorsque l’utilisateur ouvre un dossier, la boîte de dialogue envoie une notification **CDN \_ INCLUDEITEM** pour chaque élément du dossier. La boîte de dialogue envoie cette notification uniquement si l’indicateur **OFN \_ ENABLEINCLUDENOTIFY** a été défini lors de la création de la boîte de dialogue.

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

la structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) contient une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le CDN message de notification **\_ INCLUDEITEM** .

Le membre des **fibres** discontinues de la structure [**OFNOTIFYEX**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifyexa) est un pointeur vers une interface pour le dossier dont les éléments sont énumérés. Le membre **PIDL** est un pointeur vers une liste d’identificateurs d’éléments qui identifie l’élément par rapport au dossier.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) retourne la valeur zéro, la boîte de dialogue exclut l’élément de la liste d’éléments.

Pour inclure l’élément, retournez une valeur différente de zéro à partir de la procédure de raccordement.

## <a name="remarks"></a>Remarques

la boîte de dialogue comprend toujours les éléments qui ont à la fois les attributs **SFGAO \_ FILESYSTEM** et **SFGAO \_ FILESYSANCESTOR** , quelle que soit la valeur retournée par **CDN \_ INCLUDEITEM**.

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

