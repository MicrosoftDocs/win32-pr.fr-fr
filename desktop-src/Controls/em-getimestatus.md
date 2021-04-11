---
title: Message EM_GETIMESTATUS (winuser. h)
description: Obtient un jeu d’indicateurs d’État qui indiquent comment le contrôle d’édition interagit avec l’éditeur de méthode d’entrée (IME).
ms.assetid: 56705aed-afab-4f4d-9e0b-dc533b516a15
keywords:
- EM_GETIMESTATUS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETIMESTATUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a9b449053972db8101db7f5c01d1a03611cae67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105121"
---
# <a name="em_getimestatus-message"></a>\_Message GETIMESTATUS em

Obtient un jeu d’indicateurs d’État qui indiquent comment le contrôle d’édition interagit avec l’éditeur de méthode d’entrée (IME).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type d’État à récupérer. Ce paramètre peut avoir la valeur suivante.



| Valeur                                                                                                                                                                                       | Signification                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EMSIS_COMPOSITIONSTRING"></span><span id="emsis_compositionstring"></span><dl> <dt>**EMSIS \_ COMPOSITIONSTRING**</dt> </dl> | Définit le comportement de gestion de la chaîne de composition.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Données spécifiques au type d’État à récupérer. Avec la valeur de **\_ COMPOSITIONSTRING EMSIS** pour l' *État*, cette valeur de retour est une ou plusieurs des valeurs suivantes.



| Code de retour                                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**EIMES \_ GETCOMPSTRATONCE**</dt> </dl>         | Si cet indicateur est défini, le contrôle d’édition intercepte le message de composition de l' [**\_ \_ IME WM**](/windows/desktop/Intl/wm-ime-composition) avec *fFlags* défini sur GC \_ RESULTSTR et retourne la chaîne de résultat immédiatement. Si cet indicateur n’est pas défini, le contrôle d’édition passe le message de **\_ \_ composition de l’IME WM** à la procédure de fenêtre par défaut et traite la chaîne de résultat à partir du message [**WM \_ char**](/windows/desktop/inputdev/wm-char) ; il s’agit du comportement par défaut du contrôle d’édition.<br/> |
| <dl> <dt>**EIMES \_ CANCELCOMPSTRINFOCUS**</dt> </dl>     | Si cet indicateur est défini, le contrôle d’édition annule la chaîne de composition lorsqu’il reçoit le message [**WM \_ SetFocus**](/windows/desktop/inputdev/wm-setfocus) . Si cet indicateur n’est pas défini, le contrôle d’édition n’annule pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.<br/>                                                                                                                                                                       |
| <dl> <dt>**EIMES \_ COMPLETECOMPSTRKILLFOCUS**</dt> </dl> | Si cet indicateur est défini, le contrôle d’édition termine la chaîne de composition lors de la réception du message [**WM \_ KILLFOCUS**](/windows/desktop/inputdev/wm-killfocus) . Si cet indicateur n’est pas défini, le contrôle d’édition ne termine pas la chaîne de composition ; Il s’agit du comportement par défaut du contrôle d’édition.<br/>                                                                                                                                                                   |



 

## <a name="remarks"></a>Notes

**Modification riche :** Le **message \_ GETIMESTATUS em** n’est pas pris en charge.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETIMESTATUS em**](em-setimestatus.md)
</dt> </dl>

 

