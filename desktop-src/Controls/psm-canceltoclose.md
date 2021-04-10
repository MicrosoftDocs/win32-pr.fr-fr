---
title: Message PSM_CANCELTOCLOSE (Prsht. h)
description: Envoyé par une application lorsqu’elle a effectué des modifications depuis la dernière \_ notification d’application PSN qui ne peut pas être annulée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet CancelToClose.
ms.assetid: 0a4b6176-7ddb-469f-8ebf-a31e533a8690
keywords:
- PSM_CANCELTOCLOSE les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_CANCELTOCLOSE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1377801fddeeb52badee55869ace7e9c2277c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105277"
---
# <a name="psm_canceltoclose-message"></a>\_Message PSM CANCELTOCLOSE

Envoyé par une application lorsqu’elle a effectué des modifications depuis la dernière notification d' [ \_ application PSN](psn-apply.md) qui ne peut pas être annulée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ CancelToClose**](/windows/desktop/api/Prsht/nf-prsht-propsheet_canceltoclose) .

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

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

**PSM \_ CANCELTOCLOSE** désactive le bouton **Annuler** et remplace le texte du bouton **OK** par « fermer ».

La plupart des feuilles de propriétés attendent d’effectuer des modifications irréversibles jusqu’à la réception d’une \_ notification d’application PSN. Toutefois, dans certains cas, une feuille de propriétés peut apporter des modifications irréversibles en dehors de la \_ séquence de réinitialisation PSN Apply/PSN standard \_ . Par exemple, une feuille de propriétés qui contient un bouton **modifier** utilisé pour afficher une boîte de dialogue de sous-boîte de dialogue pour la modification d’une propriété. Quand l’utilisateur clique sur **OK** pour envoyer la modification, la page de la feuille de propriétés comporte plusieurs options.

-   Il peut enregistrer les modifications, mais attendre qu’il reçoive une \_ notification d’application PSN pour les appliquer. Il s’agit de l’approche privilégiée.
-   Il peut appliquer les modifications immédiatement après avoir quitté la boîte de dialogue, mais conserver les paramètres d’origine. Ces paramètres peuvent être utilisés pour restaurer l’état d’origine si une \_ notification de réinitialisation de PSN est reçue.
-   Il peut appliquer les modifications immédiatement et ne pas tenter de restaurer les paramètres d’origine lorsqu’il reçoit une notification de [ \_ réinitialisation PSN](psn-reset.md) . Cette approche n’est pas recommandée, mais elle peut s’avérer nécessaire si les modifications sont trop éloignées pour que les deux autres options soient pratiques.

Pour la troisième option, les applications doivent envoyer un message **\_ CANCELTOCLOSE PSM** à la feuille de propriétés. Elle indique à l’utilisateur que les modifications apportées à la sous-boîte de dialogue ne peuvent pas être inversées en cliquant sur le bouton **Annuler** .

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





