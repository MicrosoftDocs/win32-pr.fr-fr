---
title: Message PSM_SETFINISHTEXT (Prsht. h)
description: Définit le texte du bouton Terminer dans un Assistant, affiche et active le bouton et masque les boutons suivant et précédent. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetFinishText.
ms.assetid: fa89c6d7-9ab7-4e7c-ba08-d665420492a3
keywords:
- PSM_SETFINISHTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_SETFINISHTEXT
- PSM_SETFINISHTEXTA
- PSM_SETFINISHTEXTW
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08195cddc96c8b92f403be6940f31099e21151f1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117446"
---
# <a name="psm_setfinishtext-message"></a>\_Message PSM SETFINISHTEXT

Définit le texte du bouton **Terminer** dans un Assistant, affiche et active le bouton et masque les boutons **suivant** et **précédent** . Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetFinishText**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setfinishtext) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers le nouveau texte pour le bouton **Terminer** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Par défaut, le bouton **Terminer** n’a pas d’accélérateur clavier. Vous pouvez créer une touche d’accès rapide avec ce message en incluant une esperluette (&) dans la chaîne de texte que vous attribuez à *lParam*. Par exemple, « &Finish » définit F comme touche accélérateur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **PSM \_ SETFINISHTEXTW** (Unicode) et **PSM \_ SETFINISHTEXTA** (ANSI)<br/>    |



 

 





