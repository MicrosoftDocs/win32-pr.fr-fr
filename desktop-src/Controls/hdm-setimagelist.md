---
title: Message HDM_SETIMAGELIST (commctrl. h)
description: Affecte une liste d’images à un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ SetImageList ou d’en-tête \_ SetStateImageList.
ms.assetid: 1d7f07fa-f6f4-422a-949c-97d0388343e3
keywords:
- HDM_SETIMAGELIST les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006263"
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

## <a name="return-value"></a>Valeur de retour

Retourne le handle de la liste d’images précédemment associée au contrôle. Retourne la **valeur null** en cas d’échec ou si aucune liste d’images n’a été définie précédemment.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





