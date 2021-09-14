---
title: Message PSM_APPLY (Prsht. h)
description: Simule la sélection du bouton appliquer, indiquant qu’une ou plusieurs pages ont été modifiées et que les modifications doivent être validées et enregistrées.
ms.assetid: 2948fb66-ad77-4552-88b6-455418515e4c
keywords:
- PSM_APPLY les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_APPLY
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67d798d4a9a2f780ac81cc84c90a57d0efd4e299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117546"
---
# <a name="psm_apply-message"></a>\_Message d’application PSM

Simule la sélection du bouton **appliquer** , indiquant qu’une ou plusieurs pages ont été modifiées et que les modifications doivent être validées et enregistrées.

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

Retourne la **valeur true** si toutes les pages ont correctement appliqué les modifications, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La feuille de propriétés envoie le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) à la page actuelle. Si la page active retourne la **valeur false**, la feuille de propriétés envoie le code de notification d' [ \_ application PSN](psn-apply.md) à toutes les pages actives. Vous pouvez envoyer le \_ message d’application PSM de manière explicite ou à l’aide de la macro [**PropSheet \_ apply**](/windows/desktop/api/Prsht/nf-prsht-propsheet_apply) .

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





