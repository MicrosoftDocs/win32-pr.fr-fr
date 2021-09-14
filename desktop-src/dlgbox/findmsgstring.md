---
title: Message FINDMSGSTRING (COMMDLG. h)
description: Une boîte de dialogue Rechercher ou remplacer envoie le message FINDMSGSTRING Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton Rechercher suivant, remplacer ou remplacer tout ou ferme la boîte de dialogue.
ms.assetid: ed0b256a-96df-4588-b8f3-f7d1f89ffe74
keywords:
- Boîtes de dialogue de message FINDMSGSTRING
topic_type:
- apiref
api_name:
- FINDMSGSTRING
- FINDMSGSTRINGA
- FINDMSGSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d3a73d8734d79d5ed0862f66bf9ba5c030e46
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127191996"
---
# <a name="findmsgstring-message"></a>Message FINDMSGSTRING

Une boîte de dialogue **Rechercher** ou **remplacer** envoie le message **FINDMSGSTRING** Registered à la procédure de fenêtre de sa fenêtre propriétaire quand l’utilisateur clique sur le bouton **Rechercher suivant**, **remplacer** ou **remplacer tout** ou ferme la boîte de dialogue.


```C++
#define FINDMSGSTRING TEXT("commdlg_FindReplace")
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) . Les membres de cette structure contiennent la dernière entrée utilisateur, y compris la chaîne à rechercher, la chaîne de remplacement (le cas échéant) et les options de recherche et de remplacement.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Vous devez spécifier la constante **FINDMSGSTRING** dans un appel à la fonction [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) pour obtenir l’identificateur du message envoyé par la boîte de dialogue.

Lorsque vous créez la boîte de dialogue, utilisez le membre **hwndOwner** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) pour identifier la fenêtre de réception des messages **FINDMSGSTRING** .

Le membre **Flags** de la structure [**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea) comprend l’un des indicateurs suivants pour indiquer l’événement à l’origine du message.



| Indicateur                            | Signification                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ DIALOGTERM** (0x00000040) | La boîte de dialogue se ferme. Une fois que la fenêtre propriétaire a traité ce message, un descripteur de la boîte de dialogue n’est plus valide.                                                                                    |
| **Fr \_ FINDNEXT** (0x00000008)   | L’utilisateur a cliqué sur le bouton **suivant** de la boîte de dialogue **Rechercher** ou **remplacer** . Le membre **lpstrFindWhat** spécifie la chaîne à rechercher.                                                         |
| **Fr \_ REMPLACER** (0x00000010)    | L’utilisateur a cliqué sur le bouton **remplacer** dans une boîte de dialogue **remplacer** . Le membre **lpstrFindWhat** spécifie la chaîne à remplacer et le membre **lpstrReplaceWith** spécifie la chaîne de remplacement.     |
| **Fr \_ REPLACEALL** (0x00000020) | L’utilisateur a cliqué sur le bouton **remplacer tout** dans une boîte de dialogue **remplacer** . Le membre **lpstrFindWhat** spécifie la chaîne à remplacer et le membre **lpstrReplaceWith** spécifie la chaîne de remplacement. |



 

Pour un message **suivant** ou **remplacer tout** , le membre **indicateurs** peut inclure un ou plusieurs des indicateurs suivants pour indiquer les options de recherche.



| Indicateur                           | Signification                                                                                                                                                                                                                                                                                         |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Fr \_ En baisse** (0x00000001)      | Si cette option est définie, le bouton **bas** des cases d’option de la direction est sélectionné, ce qui indique que l’utilisateur souhaite effectuer une recherche à partir de l’emplacement actuel jusqu’à la fin du document. Si **fr \_** n’est pas défini, le bouton haut est sélectionné afin que l’utilisateur souhaite effectuer **une** recherche jusqu’au début du document.       |
| **Fr \_ MATCHCASE** (0x00000004) | Si cette option est définie, la case à cocher **respecter la casse** est activée, ce qui indique que l’utilisateur veut que la recherche respecte la casse. Si **fr \_ RespecterCasse** n’est pas défini, la case à cocher est désactivée afin que la recherche ne respecte pas la casse.                                                                         |
| **Fr \_ WHOLEWORD** (0x00000002) | Si cette option est définie, la case à cocher **mot entier uniquement** est activée, ce qui indique que l’utilisateur souhaite rechercher uniquement les mots entiers qui correspondent à la chaîne recherchée. Si **fr \_ WHOLEWORD** n’est pas défini, la case à cocher est désactivée. par conséquent, vous devez également rechercher les fragments de mots qui correspondent à la chaîne recherchée. |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Commdlg. h (inclure Windows. h)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **FINDMSGSTRINGW** (Unicode) et **FINDMSGSTRINGA** (ANSI)<br/>                                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**FINDREPLACE**](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
</dt> <dt>

[**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Bibliothèque de boîtes de dialogue communes](common-dialog-box-library.md)
</dt> </dl>

 

