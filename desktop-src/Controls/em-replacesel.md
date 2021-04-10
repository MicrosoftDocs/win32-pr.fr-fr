---
title: Message EM_REPLACESEL (winuser. h)
description: Remplace le texte sélectionné dans un contrôle d’édition ou un contrôle RichEdit par le texte spécifié.
ms.assetid: 525e6f5a-f52f-4bab-bc76-caa484729897
keywords:
- EM_REPLACESEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_REPLACESEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9745b870a310626a6cbbbddbef118a63c64479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106270"
---
# <a name="em_replacesel-message"></a>\_Message REPLACESEL em

Remplace le texte sélectionné dans un contrôle d’édition ou un contrôle RichEdit par le texte spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si l’opération de remplacement peut être annulée. Si la **valeur est true**, l’opération peut être annulée. Si la **valeur est false** , l’opération ne peut pas être annulée.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le texte de remplacement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Utilisez le message **em \_ REPLACESEL** pour remplacer uniquement une partie du texte dans un contrôle d’édition. Pour remplacer tout le texte, utilisez le message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) .

Si aucune sélection n’est effectuée, le texte de remplacement est inséré au niveau du signe insertion.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

Dans un contrôle Rich Edit, le texte de remplacement prend la mise en forme du caractère au point d’insertion ou, s’il existe une sélection, du premier caractère de la sélection.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

