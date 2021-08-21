---
title: Message EM_GETFILELINECOUNT (CommCtrl. h)
description: Obtient le nombre de lignes dans un contrôle d’édition multiligne, indépendamment de la façon dont les lignes sont affichées à l’écran.
ms.assetid: 9fe63c10-7395-4f98-a672-14960a70d14f
keywords:
- EM_GETFILELINECOUNT les contrôles de Windows de message
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
ms.openlocfilehash: 28539af32212a699e12d2cf1d1787fa2e7aaa224f374eb6a63717279fcad16b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019677"
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

## <a name="remarks"></a>Remarques

Le message **em \_ GETFILELINECOUNT** récupère le nombre total de lignes de texte, indépendamment de la façon dont les lignes sont affichées à l’écran, et pas seulement du nombre de lignes actuellement visibles.

Le retour automatique à la ligne ne change pas le nombre de lignes renvoyées par ce message, car ce message fonctionne indépendamment de la façon dont les lignes sont affichées à l’écran.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, 1809 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                                     |
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

 

 





