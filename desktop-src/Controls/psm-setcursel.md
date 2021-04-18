---
title: Message PSM_SETCURSEL (Prsht. h)
description: Active la page spécifiée dans une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro PropSheet SetCurSel.
ms.assetid: 800aadde-cabc-424e-8e63-60fc7ce952d7
keywords:
- PSM_SETCURSEL les contrôles de message Windows
topic_type:
- apiref
api_name:
- PSM_SETCURSEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12f41f0ba2ec8d13a7bfc932b553b355399f76b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103469"
---
# <a name="psm_setcursel-message"></a>\_Message PSM SETCURSEL

Active la page spécifiée dans une feuille de propriétés. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**PropSheet \_ SetCurSel**](/windows/desktop/api/Prsht/nf-prsht-propsheet_setcursel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la page. Une application peut spécifier l’index ou le descripteur, ou les deux. Si les deux sont spécifiés, *lParam* est prioritaire.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la page à activer. Une application peut spécifier l’index ou le descripteur, ou les deux. Si les deux sont spécifiés, *lParam* est prioritaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

La fenêtre qui perd l’activation reçoit le code de notification [PSN \_ KILLACTIVE](psn-killactive.md) , et la fenêtre qui obtient l’activation reçoit le code de [notification \_ PSN](psn-setactive.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Prsht. h</dt> </dl> |



 

 





