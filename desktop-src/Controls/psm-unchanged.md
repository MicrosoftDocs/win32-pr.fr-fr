---
title: Message PSM_UNCHANGED (Prsht. h)
description: Informe une feuille de propriétés que les informations d’une page sont rétablies à l’état enregistré précédemment. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet inchangée.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_UNCHANGED
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d6216f94afd610bb49710a3e84b4c21a673f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200578"
---
# <a name="psm_unchanged-message"></a>Message PSM non \_ modifié

Informe une feuille de propriétés que les informations d’une page sont rétablies à l’état enregistré précédemment. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ inchangée**](/windows/desktop/api/Prsht/nf-prsht-propsheet_unchanged) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers la page qui a rétabli l’état enregistré précédemment.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

La feuille des propriétés désactive le bouton **appliquer** si aucune autre page n’a enregistré des modifications dans la feuille de propriétés.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





