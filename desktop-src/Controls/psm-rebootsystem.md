---
title: Message PSM_REBOOTSYSTEM (Prsht. h)
description: Indique que le système doit être redémarré pour que les modifications prennent effet. Vous pouvez envoyer le \_ message REBOOTSYSTEM PSM de manière explicite ou à l’aide de la \_ macro PropSheet REBOOTSYSTEM.
ms.assetid: 461fce3c-183a-4b9b-8eab-ed2838d9f866
keywords:
- PSM_REBOOTSYSTEM les contrôles de message Windows
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
ms.openlocfilehash: 14f5018dc3845d699561740ccd9cbb0a9c793f15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464870"
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

## <a name="remarks"></a>Notes

Une application doit envoyer ce message uniquement en réponse au message de notification [PSN \_ apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) .

Ce message force la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) à retourner la \_ valeur ID PSREBOOTSYSTEM, mais uniquement si l’utilisateur clique sur le bouton **OK** pour fermer la feuille de propriétés. Il incombe à l’application de redémarrer le système, ce qui peut être fait à l’aide de la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

Ce message remplace tous les [**messages \_ RESTARTWINDOWS PSM**](psm-restartwindows.md) qui le précèdent ou le suivent.

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

