---
title: Message PSM_RESTARTWINDOWS (Prsht. h)
description: Indique que Windows doit être redémarré pour que les modifications prennent effet.
ms.assetid: 5bf634ee-7408-45df-adb6-c5b947f6c47b
keywords:
- PSM_RESTARTWINDOWS les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_RESTARTWINDOWS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb12126ae0a2b9187a941ccc1aff53186a0cda7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843425"
---
# <a name="psm_restartwindows-message"></a>\_Message PSM RESTARTWINDOWS

Indique que Windows doit être redémarré pour que les modifications prennent effet.

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

Une application doit envoyer ce message uniquement en réponse au code de notification [PSN \_ apply](psn-apply.md) ou [PSN \_ KILLACTIVE](psn-killactive.md) . Vous pouvez envoyer le **message \_ RESTARTWINDOWS PSM** de manière explicite ou à l’aide de la macro [**PropSheet \_ RESTARTWINDOWS**](/windows/desktop/api/Prsht/nf-prsht-propsheet_restartwindows) .

Ce message force la fonction [**feuille**](/windows/desktop/api/Prsht/nf-prsht-propertysheeta) à retourner la \_ valeur ID PSRESTARTWINDOWS, mais uniquement si l’utilisateur clique sur le bouton **OK** pour fermer la feuille de propriétés. L’application est responsable du redémarrage de Windows, ce qui peut être effectué à l’aide de la fonction [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) .

> [!Note]  
> Ce message n’est pas pris en charge lors de l’utilisation du style de l’Assistant Aero ([**PSH \_ AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

