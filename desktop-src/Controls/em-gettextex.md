---
title: Message EM_GETTEXTEX (RichEdit. h)
description: Obtient le texte à partir d’un contrôle RichEdit.
ms.assetid: 46431563-fde1-4407-ab7a-b2248c0e12b8
keywords:
- EM_GETTEXTEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357cfe37d3432b396183b500c945ad89397c0294
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465150"
---
# <a name="em_gettextex-message"></a>\_Message GETTEXTEX em

Obtient le texte à partir d’un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) , qui indique comment traduire le texte avant de le placer dans la mémoire tampon de sortie.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon pour recevoir le texte. La taille de cette mémoire tampon, en octets, est spécifiée par le membre **CB** de la structure [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) . Utilisez le message [**em \_ GETTEXTLENGTHEX**](em-gettextlengthex.md) pour connaître la taille requise pour la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le nombre de **TCHAR** s copié dans la mémoire tampon de sortie, y compris la marque de fin null.

## <a name="remarks"></a>Notes

Si la taille de la mémoire tampon de sortie est inférieure à la taille du texte dans le contrôle, le contrôle d’édition copie le texte à partir de son début et le place dans la mémoire tampon jusqu’à ce que la mémoire tampon soit pleine. Un caractère null de fin sera toujours placé à la fin de la mémoire tampon.

Si du texte ANSI est demandé, **em \_ GETTEXTEX** utilise la fonction [**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) pour convertir les caractères Unicode en ANSI. Elle vous permet de passer d’Unicode à ANSI à l’aide d’une page de codes particulière. La structure [**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex) contient des membres (**lpDefaultChar** et **lpUsedDefChar**) qui sont utilisés dans la traduction Unicode en ANSI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETTEXTEX em**](em-settextex.md)
</dt> <dt>

[**GETTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-gettextex)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
</dt> <dt>

[**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

