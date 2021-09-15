---
title: CDN_SELCHANGE le code de notification (COMMDLG. h)
description: Envoyé par une boîte de dialogue Ouvrir ou enregistrer sous de style Explorateur lorsque la sélection change dans la zone de liste qui affiche le contenu du dossier ou du répertoire actuellement ouvert.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- Boîtes de dialogue CDN_SELCHANGE code de notification
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c21aa9dda117c74707b3c890ad96e017b45bcc0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517429"
---
# <a name="cdn_selchange-notification-code"></a>CDN \_ Code de notification SELCHANGE

\[à partir de Windows Vista, les boîtes de dialogue **ouvrir** et **enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Envoyé par une boîte de dialogue **ouvrir** ou **Enregistrer sous** de style Explorateur lorsque la sélection change dans la zone de liste qui affiche le contenu du dossier ou du répertoire actuellement ouvert.

Votre procédure de hook [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) reçoit ce message sous la forme d’un message [**WM \_ Notify**](../controls/wm-notify.md) .


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) . la structure **OFNOTIFY** contient une structure [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) dont le membre de **code** indique le CDN message de notification **\_ SELCHANGE** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée.

## <a name="remarks"></a>Notes

Le système envoie cette notification uniquement si la boîte de dialogue a été créée à l’aide de la valeur **OFN \_ Explorer** .

Pour récupérer le nom du fichier ou du dossier que vous venez de sélectionner, la procédure de hook peut envoyer le message [**CDM \_ GETFILEPATH**](cdm-getfilepath.md) ou [**CDM \_ GETSPEC**](cdm-getspec.md) à la boîte de dialogue.

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

[**\_GETFILEPATH CDM**](cdm-getfilepath.md)
</dt> <dt>

[**\_GETSPEC CDM**](cdm-getspec.md)
</dt> <dt>

[**GetOpenFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[**GetSaveFileName**](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

