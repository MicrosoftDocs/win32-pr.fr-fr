---
title: Message PSM_RECALCPAGESIZES (Prsht. h)
description: Recalcule la taille de page d’une feuille de propriétés standard ou d’Assistant après l’ajout ou la suppression de pages. Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro PropSheet RecalcPageSizes.
ms.assetid: 42257ea3-0471-4c67-adcd-01cd2669a51e
keywords:
- PSM_RECALCPAGESIZES les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_RECALCPAGESIZES
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ae2030f432e8c52ed6208be34d429b4579edb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117473"
---
# <a name="psm_recalcpagesizes-message"></a>\_Message PSM RECALCPAGESIZES

Recalcule la taille de page d’une feuille de propriétés standard ou d’Assistant après l’ajout ou la suppression de pages. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**PropSheet \_ RecalcPageSizes**](/windows/desktop/api/Prsht/nf-prsht-propsheet_recalcpagesizes) .

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

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Lorsqu’une feuille de propriétés est créée, elle est dimensionnée pour correspondre à sa collection initiale de pages. Pour assurer la compatibilité avec les versions précédentes des contrôles communs, les feuilles de propriétés et les assistants ne se redimensionnent pas automatiquement quand les pages sont ajoutées ou supprimées par la suite. Avec les contrôles communs [version 5,80](common-control-versions.md), les applications doivent envoyer un message **PSM \_ RECALCPAGESIZES** après l’ajout ou la suppression de pages avec [**PSM \_ ADDPAGE**](psm-addpage.md), [**PSM \_ INSERTPAGE**](psm-insertpage.md), [**PSM \_ REMOVEPAGE**](psm-removepage.md)ou leurs macros équivalentes. Elle garantit que la feuille de propriétés est correctement dimensionnée pour sa collection de pages actuelle. Si ce message n’est pas envoyé, certaines pages de la feuille de propriétés peuvent être tronquées ou trop volumineuses.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





