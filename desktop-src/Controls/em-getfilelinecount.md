---
title: Message EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtient le nombre de lignes dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETFILELINECOUNT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: bf48b3abeb10b98bf0c22a7dd2ef93c73a2a59c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104833"
---
# <a name="em_getfilelinecount-message-commctrlh"></a>Message EM_GETFILELINECOUNT (CommCtrl. h)

Obtient le nombre de lignes dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un entier spécifiant le nombre total de lignes de texte dans le contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran. Si le contrôle n’a pas de texte, la valeur de retour est 1. La valeur de retour ne sera jamais inférieure à 1.

## <a name="remarks"></a>Notes

Le message **em \_ GETFILELINECOUNT** récupère le nombre total de lignes de texte, indépendamment de la façon dont les lignes sont affichées à l’écran, et pas seulement du nombre de lignes actuellement visibles.

Le retour automatique à la ligne ne change pas le nombre de lignes renvoyées par ce message, car ce message fonctionne indépendamment de la façon dont les lignes sont affichées à l’écran.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, 1809 \[ uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>CommCtrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETFILELINE em**](em-getfileline.md)
</dt> <dt>

[**\_FILELINELENGTH em**](em-filelinelength.md)
</dt> <dt>

[**Modifier \_ GetFileLineCount**](/windows/win32/api/commctrl/nf-commctrl-edit_getfilelinecount)
</dt> </dl>

 

 





