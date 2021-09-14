---
title: Message LBSELCHSTRING (COMMDLG. h)
description: Une boîte de dialogue Ouvrir ou enregistrer sous envoie le message LBSELCHSTRING Registered à votre procédure de hook lorsque la sélection change dans l’une des zones de liste ou des zones de liste modifiable de la boîte de dialogue.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Boîtes de dialogue de message LBSELCHSTRING
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62d61f88bd7cb6a84a94a3d8a246e6045f88a305
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918056"
---
# <a name="lbselchstring-message"></a>Message LBSELCHSTRING

\[à partir de Windows Vista, les boîtes de dialogue **ouvrir** et **enregistrer comme** courantes ont été remplacées par la [boîte de dialogue élément commun](../shell/common-file-dialog.md). Nous vous recommandons d’utiliser l’API de la boîte de dialogue élément commun au lieu de ces boîtes de dialogue à partir de la bibliothèque de boîtes de dialogue communes.\]

Une boîte de dialogue **ouvrir** ou **Enregistrer sous** envoie le message **LBSELCHSTRING** Registered à votre procédure de hook lorsque la sélection change dans l’une des zones de liste ou des zones de liste modifiable de la boîte de dialogue.


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de la zone de liste ou zone de liste déroulante dans laquelle la sélection a été modifiée.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie le numéro d’élément de la chaîne sélectionnée dans la zone de liste ou la zone de liste déroulante. Le mot de poids fort spécifie le type de modification de la sélection. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                       | Signification                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <dt>**CD-ROM \_ LBSELCHANGE**</dt> <dt>0</dt> </dl>     | L’élément est le seul élément sélectionné dans une zone de liste à sélection unique.<br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <dt>**CD-ROM \_ LBSELADD**</dt> <dt>2</dt> </dl>              | L’élément est l’un des éléments sélectionnés dans une zone de liste à sélection multiple.<br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <dt>**CD-ROM \_ LBSELSUB**</dt> <dt>1</dt> </dl>              | L’élément n’est plus sélectionné dans une zone de liste à sélection multiple.<br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <dt>**CD-ROM \_ LBSELNOITEMS**</dt> <dt>-1</dt> </dl> | Il n’existe aucun élément dans une zone de liste à sélection multiple.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

La procédure de hook doit spécifier la constante **LBSELCHSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LBSELCHSTRINGW** (Unicode) et **LBSELCHSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**CDN \_ SELCHANGE**](cdn-selchange.md)
</dt> <dt>

[**CDN \_ TYPECHANGE**](cdn-typechange.md)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

