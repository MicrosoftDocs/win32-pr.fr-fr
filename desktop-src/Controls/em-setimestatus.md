---
title: Message EM_SETIMESTATUS (winuser. h)
description: Définit les indicateurs d’État qui déterminent le mode d’interaction d’un contrôle d’édition avec l’éditeur de méthode d’entrée (IME).
ms.assetid: 3de2e8b5-bdd8-4b25-9427-38a11b77a17a
keywords:
- EM_SETIMESTATUS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e896c358281b2d4b5012fe13003720e0d008e6a4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006387"
---
# <a name="em_setimestatus-message"></a>\_Message SETIMESTATUS em

Définit les indicateurs d’État qui déterminent le mode d’interaction d’un contrôle d’édition avec l’éditeur de méthode d’entrée (IME).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type d’État à définir. Ce paramètre peut avoir la valeur suivante.



| Valeur                                                                                                                                                                                       | Signification                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Définit le comportement de la chaîne de composition de gestion.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Données spécifiques au type d’État. Si *wParam* est **EMSIS \_ COMPOSITIONSTRING**, ce paramètre peut avoir une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EIMES_GETCOMPSTRATONCE"></span><span id="eimes_getcompstratonce"></span><dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>                         | Si cet indicateur est défini, le contrôle d’édition intercepte le message de composition de l' [**\_ IME \_ WM**](/windows/desktop/Intl/wm-ime-composition) avec *lParam* défini sur GC \_ RESULTSTR et retourne la chaîne de résultat immédiatement. Si cet indicateur n’est pas défini, le contrôle d’édition passe le message de **\_ \_ composition de l’IME WM** à la procédure de fenêtre par défaut et gère la chaîne de résultat à partir du message [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; il s’agit du comportement par défaut du contrôle d’édition.<br/> |
| <span id="EIMES_CANCELCOMPSTRINFOCUS"></span><span id="eimes_cancelcompstrinfocus"></span><dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>             | Si cet indicateur est défini, le contrôle d’édition annule la chaîne de composition lorsqu’il reçoit le message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) . Si cet indicateur n’est pas défini, le contrôle d’édition n’annule pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.<br/>                                                                                                                                                                     |
| <span id="EIMES_COMPLETECOMPSTRKILLFOCUS"></span><span id="eimes_completecompstrkillfocus"></span><dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si cet indicateur est défini, le contrôle d’édition termine la chaîne de composition lors de la réception du message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) . Si cet indicateur n’est pas défini, le contrôle d’édition ne termine pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.<br/>                                                                                                                                                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la valeur précédente du paramètre *lParam* .

## <a name="remarks"></a>Notes

**Modification riche :** Le **message \_ SETIMESTATUS em** n’est pas pris en charge.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETIMESTATUS em**](em-getimestatus.md)
</dt> </dl>

 

