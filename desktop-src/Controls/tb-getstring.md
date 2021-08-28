---
title: Message TB_GETSTRING (commctrl. h)
description: Récupère une chaîne à partir du pool de chaînes d’une barre d’outils.
ms.assetid: a5f80c16-bc6d-466d-8ec6-77451432148e
keywords:
- TB_GETSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETSTRING
- TB_GETSTRINGA
- TB_GETSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d25cbf20fd084c2ce60b29d131b7f488ca2b8cee178a2218fcfac191b3c1af33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918480"
---
# <a name="tb_getstring-message"></a>TO \_ GETSTRING (message)

Récupère une chaîne à partir du pool de chaînes d’une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie la longueur de la mémoire tampon *lParam* , en octets. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie l’index de la chaîne.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon utilisée pour retourner la chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la longueur de chaîne en cas de réussite, ou-1 dans le cas contraire.

## <a name="remarks"></a>Remarques

Ce message retourne la chaîne spécifiée à partir du pool de chaînes de la barre d’outils. Elle ne correspond pas nécessairement à la chaîne de texte actuellement affichée par un bouton. Pour récupérer la chaîne de texte actuelle d’un bouton, envoyez la barre d’outils à un message [**\_ GETBUTTONTEXT to**](tb-getbuttontext.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ GETSTRINGW** (Unicode) et **to \_ GETSTRINGA** (ANSI)<br/>                 |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TO \_ ADDSTRING**](tb-addstring.md)
</dt> <dt>

[**TO \_ ADDBUTTONS**](tb-addbuttons.md)
</dt> <dt>

[**TO \_ INSERTBUTTON**](tb-insertbutton.md)
</dt> </dl>

 

