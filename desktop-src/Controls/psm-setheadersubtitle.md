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
ms.openlocfilehash: 2d73376b5ed35f20b43c743b31a4a78d3a4fa809
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117437"
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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Si vous spécifiez la page actuelle, elle est immédiatement repeinte pour afficher le nouveau sous-titre.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Spécifications



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

 

 





