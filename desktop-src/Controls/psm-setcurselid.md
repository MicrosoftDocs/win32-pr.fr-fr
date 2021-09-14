---
title: Message PSM_SETCURSELID (Prsht. h)
description: Active la page donnée dans une feuille de propriétés en fonction de l’identificateur de ressource de la page. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetCurSelByID.
ms.assetid: 6db5f6ab-77ce-4a80-a84d-cb66eb1cdeaa
keywords:
- PSM_SETCURSELID les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PSM_SETCURSELID
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da6ec827bbf3b9bade0af649f124d25c420d299
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117450"
---
# <a name="psm_setcurselid-message"></a>\_Message PSM SETCURSELID

Active la page donnée dans une feuille de propriétés en fonction de l’identificateur de ressource de la page. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetCurSelByID**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcurselbyid) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificateur de ressource de la page à activer.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La fenêtre qui perd l’activation reçoit le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) , et la fenêtre qui obtient l’activation reçoit le code de [notification \_ PSN](psn-setactive.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





