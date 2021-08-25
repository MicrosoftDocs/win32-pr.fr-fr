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
ms.openlocfilehash: 7be1d21b5153d480e409c6e9e7f4204746b5509b058bc292509e24ad9e03b538
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877019"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

La fenêtre qui perd l’activation reçoit le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) , et la fenêtre qui obtient l’activation reçoit le code de [notification \_ PSN](psn-setactive.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





