---
title: Message EM_SETFONTSIZE (RichEdit. h)
description: Définit la taille de police du texte sélectionné dans un contrôle RichEdit.
ms.assetid: 18d91370-12c0-4e5f-a0e9-ffde02abc966
keywords:
- EM_SETFONTSIZE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETFONTSIZE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e646d58626a034f4764d6b9636e5b4b3eedba5befd7986eade9979c1f4a4fd5a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048459"
---
# <a name="em_setfontsize-message"></a>\_Message SETFONTSIZE em

Définit la taille de police du texte sélectionné dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Modification de la taille en points du texte sélectionné. Le résultat sera arrondi en fonction des valeurs indiquées dans le tableau suivant. Ce paramètre doit être compris entre-1637 et 1638. La taille de police obtenue sera comprise dans la plage comprise entre 1 et 1638.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si aucune erreur ne s’est produite, la valeur de retour est **true**.

Si une erreur s’est produite, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

Vous pouvez facilement récupérer la taille de police en envoyant le message [**em \_ GETCHARFORMAT**](em-getcharformat.md) .

Rich Edit ajoute d’abord *wParam* à la taille de police actuelle, puis utilise la taille obtenue et le tableau suivant pour déterminer la valeur d’arrondi.



| Élastique    | Valeur d’arrondi |
|---------|----------------|
| <= 12 | 1              |
| 28      | 2              |
| 36      | 0              |
| 48      | 0              |
| 72      | 0              |
| 80      | 0              |
| > 80 | 10             |



 

Si la taille de police obtenue n’est pas divisible par la valeur d’arrondi, la taille de police est ensuite arrondie à un nombre uniformément divisible par la valeur d’arrondi. Par conséquent, si la taille de police est inférieure ou égale à 12, la valeur d’arrondi sera 1. De même, si la taille de police est inférieure ou égale à 28, la valeur d’arrondi est 2. Pour les valeurs supérieures à 28, les tailles de police sont arrondies à la bande suivante. Par conséquent, la taille de police passe à 36, 48, 72, 80. Après 80, tous les arrondis sont effectués par incréments de dix points.

La taille de police est arrondie vers le haut ou vers le haut selon le signe de *wParam*. Si *wParam* est positif, l’arrondi est toujours en haut. Dans le cas contraire, l’arrondi est toujours inactif. Ainsi, si la taille de police actuelle est 10 et que *wParam* est 3, la taille de police obtenue est 14 (10 + 3 = 13, qui n’est pas divisible par 2, donc la taille est arrondie à 14). À l’inverse, si la taille de police actuelle est 14 et que *wParam* est-3, la taille de police obtenue est 10 (14-3 = 11, qui n’est pas divisible par 2, donc la taille est arrondie à 10).

La modification est appliquée à chaque partie de la sélection. Ainsi, si une partie du texte est 10 PT et d’autres 20 points, une fois qu’un appel avec *wParam* a la valeur 1, les tailles de police deviennent 11pt et 22pt, respectivement.

Des exemples supplémentaires sont présentés dans le tableau suivant.



| Taille de la police d’origine | *wParam* | Taille de police obtenue |
|--------------------|----------|---------------------|
| 7                  | 1        | 8                   |
| 7                  | 3        | 10                  |
| 10                 | 3        | 14                  |
| 14                 | -3       | 10                  |
| 28                 | 1        | 36                  |
| 28                 | 3        | 36                  |
| 80                 | 1        | 90                  |
| 80                 | -1       | 72                  |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETCHARFORMAT em**](em-getcharformat.md)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[À propos des contrôles RichEdit](about-rich-edit-controls.md)
</dt> </dl>

 

 





