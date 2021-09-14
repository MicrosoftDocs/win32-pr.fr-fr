---
title: Message PSM_GETCURRENTPAGEHWND (Prsht. h)
description: Récupère un handle de la fenêtre de la page active d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet GetCurrentPageHwnd.
ms.assetid: 1f2d0af9-5853-48e7-b827-483be032b6ca
keywords:
- PSM_GETCURRENTPAGEHWND les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_GETCURRENTPAGEHWND
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae9ac89e6bc60317f2caf31ea92754d10983e11a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117526"
---
# <a name="psm_getcurrentpagehwnd-message"></a>\_Message PSM GETCURRENTPAGEHWND

Récupère un handle de la fenêtre de la page active d’une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ GetCurrentPageHwnd**](/windows/desktop/api/Prsht/nf-prsht-propsheet_getcurrentpagehwnd) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne un handle vers la fenêtre de la page de la feuille de propriétés actuelle.

## <a name="remarks"></a>Notes

Utilisez le **message \_ GETCURRENTPAGEHWND PSM** avec les feuilles de propriétés non modales pour déterminer quand détruire la boîte de dialogue. Quand l’utilisateur clique sur le bouton **OK** ou **Annuler** , **PSM \_ GETCURRENTPAGEHWND** retourne la **valeur null** et vous pouvez ensuite utiliser la fonction [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) pour détruire la boîte de dialogue.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta)
</dt> </dl>

 

