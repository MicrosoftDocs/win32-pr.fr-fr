---
title: Message PSM_UNCHANGED (Prsht. h)
description: Informe une feuille de propriétés que les informations d’une page sont rétablies à l’état enregistré précédemment. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet inchangée.
ms.assetid: 61c15dec-40d0-4720-a117-4eed765c8819
keywords:
- PSM_UNCHANGED les contrôles de Windows de message
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
ms.openlocfilehash: 83fc0097896af0ad18ff89895eb8c5debc36e196e1687fc9706c655b4ec95d48
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088459"
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

## <a name="remarks"></a>Remarques

La feuille des propriétés désactive le bouton **appliquer** si aucune autre page n’a enregistré des modifications dans la feuille de propriétés.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





