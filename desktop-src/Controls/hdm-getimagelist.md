---
title: Message HDM_GETIMAGELIST (commctrl. h)
description: Obtient le handle vers la liste d’images qui a été définie pour un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en-tête \_ GetImageList ou d’en-tête \_ GetStateImageList.
ms.assetid: 3e1a979c-60c5-4538-bd4d-16238829062e
keywords:
- HDM_GETIMAGELIST les contrôles de message Windows
topic_type:
- apiref
api_name:
- HDM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e199d603af873f1957d33855ccf5c59a90a4002
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742277"
---
# <a name="hdm_getimagelist-message"></a>\_Message HDM GETIMAGELIST

Obtient le handle vers la liste d’images qui a été définie pour un contrôle d’en-tête existant. Vous pouvez envoyer ce message explicitement ou utiliser la macro d’en [**-tête \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getimagelist) ou d' [**en-tête \_ GetStateImageList**](/windows/desktop/api/Commctrl/nf-commctrl-header_getstateimagelist) .

## <a name="parameters"></a>Paramètres

<dl> <dt>*wParam*</dt> <dd>Une des valeurs suivantes :

| Value                                                                                                                                                      | Signification                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="HDSIL_NORMAL"></span><span id="hdsil_normal"></span><dl> <dt>**HDSIL \_ normal**</dt> </dl> | Indique qu’il s’agit d’une liste d’images normale.<br/> |
| <span id="HDSIL_STATE"></span><span id="hdsil_state"></span><dl> <dt>**État de HDSIL \_**</dt> </dl>    | Indique qu’il s’agit d’une liste d’images d’État.<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne un handle vers le jeu de listes d’images pour le contrôle d’en-tête.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





