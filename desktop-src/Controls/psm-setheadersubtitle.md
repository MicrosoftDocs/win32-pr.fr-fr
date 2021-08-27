---
title: Message PSM_SETHEADERSUBTITLE (Prsht. h)
description: Définit le texte du sous-titre de l’en-tête de la page intérieure d’un Assistant. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet SetHeaderSubTitle.
ms.assetid: 6ef3017b-8a20-4d62-a604-135410d8bdf7
keywords:
- PSM_SETHEADERSUBTITLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_SETHEADERSUBTITLE
- PSM_SETHEADERSUBTITLEA
- PSM_SETHEADERSUBTITLEW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20e030b75a933ba7f647f8b3dffa5e45637999d45f3299f8280fd1db3afb9857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088499"
---
# <a name="psm_setheadersubtitle-message"></a>\_Message PSM SETHEADERSUBTITLE

Définit le texte du sous-titre de l’en-tête de la page intérieure d’un Assistant. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ SetHeaderSubTitle**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setheadersubtitle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la page de l’Assistant.

</dd> <dt>

*lParam* 
</dt> <dd>

Nouveau sous-titre d’en-tête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Remarques

Si vous spécifiez la page actuelle, elle est immédiatement repeinte pour afficher le nouveau sous-titre.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl>      |
| Noms Unicode et ANSI<br/>   | **PSM \_ SETHEADERSUBTITLEW** (Unicode) et **PSM \_ SETHEADERSUBTITLEA** (ANSI)<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_HWNDTOINDEX PSM**](psm-hwndtoindex.md)
</dt> <dt>

[**\_IDTOINDEX PSM**](psm-idtoindex.md)
</dt> <dt>

[**\_PAGETOINDEX PSM**](psm-pagetoindex.md)
</dt> </dl>

 

 





