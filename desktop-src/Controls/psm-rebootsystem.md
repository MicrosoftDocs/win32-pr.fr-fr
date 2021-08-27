---
title: Message PSM_REBOOTSYSTEM (Prsht. h)
description: Indique que le système doit être redémarré pour que les modifications prennent effet. Vous pouvez envoyer le \_ message REBOOTSYSTEM PSM de manière explicite ou à l’aide de la \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_REBOOTSYSTEM
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfcfebc931d1dbf01ab053fa2723bdcf361c4be5ef1443b9131115e2300770cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088629"
---
# <a name="psm_rebootsystem-message"></a>\_Message PSM REBOOTSYSTEM

Indique que le système doit être redémarré pour que les modifications prennent effet. Vous pouvez envoyer le **message \_ REBOOTSYSTEM PSM** de manière explicite ou à l’aide de la macro [**PropSheet \_ REBOOTSYSTEM**](/windows/desktop/api/Prsht/nf-prsht-propsheet_rebootsystem) .

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

## <a name="remarks"></a>Remarques

Une application doit envoyer ce message uniquement en réponse au message de notification [PSN \_ apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .

Ce message force la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) à retourner la \_ valeur ID PSREBOOTSYSTEM, mais uniquement si l’utilisateur clique sur le bouton **OK** pour fermer la feuille de propriétés. Il incombe à l’application de redémarrer le système, ce qui peut être fait à l’aide de la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

Ce message remplace tous les [**messages \_ RESTARTWINDOWS PSM**](psm-restartwindows.md) qui le précèdent ou le suivent.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

