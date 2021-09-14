---
title: Message SHAREVISTRING (COMMDLG. h)
description: Une boîte de dialogue Ouvrir ou enregistrer sous envoie le message SHAREVISTRING Registered à votre procédure de Hook, OFNHookProc, si une violation de partage se produit pour le fichier sélectionné quand l’utilisateur clique sur le bouton OK.
ms.assetid: 53884497-4872-4aa8-b56e-2bb98df58fed
keywords:
- Boîtes de dialogue de message SHAREVISTRING
topic_type:
- apiref
api_name:
- SHAREVISTRING
- SHAREVISTRINGA
- SHAREVISTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 043bed9edd08269e4e030482cbd44debea3a3695
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918055"
---
# <a name="sharevistring-message"></a>Message SHAREVISTRING

\[à partir de Windows Vista, les boîtes de dialogue **ouvrir** et **enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie le message **SHAREVISTRING** Registered à votre procédure de Hook, [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc), si une violation de partage se produit pour le fichier sélectionné quand l’utilisateur clique sur le bouton **OK** .


```C++
#define SHAREVISTRING TEXT("commdlg_ShareViolation")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) . Le membre **lpstrFile** de cette structure contient le nom de fichier qui a provoqué la violation de partage.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La procédure de raccordement doit retourner l’une des valeurs suivantes pour indiquer comment la boîte de dialogue doit gérer la violation de partage.



| Code/valeur de retour                                                                                                                                           | Description                                                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**OFN \_ SHAREFALLTHROUGH**</dt> <dt>2</dt> </dl> | Accepter le nom de fichier<br/>                                                                                            |
| <dl> <dt>**OFN \_ SHARENOWARN**</dt> <dt>1</dt> </dl>      | Refuser le nom de fichier, mais ne pas avertir l’utilisateur. L’application est responsable de l’affichage d’un message d’avertissement.<br/> |
| <dl> <dt>**OFN \_ SHAREWARN**</dt> <dt>0</dt> </dl>        | Rejetez le nom de fichier et affichez un message d’avertissement (le même résultat qu’en l’absence de procédure de raccordement).<br/>       |



 

## <a name="remarks"></a>Notes

La procédure de hook doit spécifier la constante **SHAREVISTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.

La boîte de dialogue envoie le message **SHAREVISTRING** Registered uniquement si vous n’avez pas spécifié l’indicateur **OFN \_ SHAREAWARE** dans le membre **Flags** de la structure [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) quand vous avez créé la boîte de dialogue.

Si la procédure de raccordement retourne une valeur non définie, la boîte de dialogue répond comme si **OFN \_ SHAREWARN** était retourné.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SHAREVISTRINGW** (Unicode) et **SHAREVISTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CDN \_ SHAREVIOLATION**](cdn-shareviolation.md)
</dt> <dt>

[**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

