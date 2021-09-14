---
title: Message FILEOKSTRING (COMMDLG. h)
description: Une boîte de dialogue Ouvrir ou enregistrer sous envoie le message FILEOKSTRING Registered à votre procédure de Hook, OFNHookProc, lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton OK.
ms.assetid: 32bf3cc7-76a2-4b78-81d7-682b088c4e14
keywords:
- Boîtes de dialogue de message FILEOKSTRING
topic_type:
- apiref
api_name:
- FILEOKSTRING
- FILEOKSTRINGA
- FILEOKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24dd07faecc66bc50c408eab36bcbd8c93c460ef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192000"
---
# <a name="fileokstring-message"></a>Message FILEOKSTRING

\[à partir de Windows Vista, les boîtes de dialogue **ouvrir** et **enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie le message **FILEOKSTRING** Registered à votre procédure de Hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), lorsque l’utilisateur spécifie un nom de fichier et clique sur le bouton **OK** . La procédure de raccordement peut accepter le nom de fichier et autoriser la fermeture de la boîte de dialogue, ou refuser le nom de fichier et forcer la boîte de dialogue à rester ouverte.


```C++
#define FILEOKSTRING TEXT("commdlg_FileNameOK")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Le membre **lpstrFile** de cette structure contient le lecteur, le chemin d’accès et le nom de fichier spécifiés par l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la procédure de raccordement retourne la valeur zéro, la boîte de dialogue **ouvrir** ou **Enregistrer sous** accepte le nom de fichier spécifié et se ferme.

Si la procédure de raccordement retourne une valeur différente de zéro, la boîte de dialogue **ouvrir** ou **Enregistrer sous** rejette le nom de fichier spécifié et reste ouverte.

## <a name="remarks"></a>Notes

La procédure de hook doit spécifier la constante **FILEOKSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **FILEOKSTRINGW** (Unicode) et **FILEOKSTRINGA** (ANSI)<br/>                                      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CDN \_ FILEOK**](cdn-fileok.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

