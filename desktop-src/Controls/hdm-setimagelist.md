---
title: Message HDM_SETIMAGELIST (commctrl. h)
description: Affecte une liste d’images à un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetImageList ou d’en-tête \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17fe21d64b141cf27d32e00fac0ce78228421518
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942069"
---
# <a name="hdm_setimagelist-message"></a>\_Message HDM SETIMAGELIST

Affecte une liste d’images à un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en [**-tête \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setimagelist) ou d' [**en-tête \_ SetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_setstateimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>*wParam*</dt> <dd>Une des valeurs suivantes :

| Value                                                                                                                                                      | Signification                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normal**</dt> </dl> | Indique qu’il s’agit d’une liste d’images normale.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**État de HDSIL \_**</dt> </dl>    | Indique qu’il s’agit d’une liste d’images d’État.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle d’une liste d’images.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le handle de la liste d’images précédemment associée au contrôle. Retourne la **valeur null** en cas d’échec ou si aucune liste d’images n’a été définie précédemment.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





