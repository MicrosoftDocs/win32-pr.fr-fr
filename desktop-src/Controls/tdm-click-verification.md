---
title: Message TDM_CLICK_VERIFICATION (commctrl. h)
description: Simule un clic de la case à cocher vérification d’une boîte de dialogue de tâche, si elle existe.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_CLICK_VERIFICATION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3cda5e85b138225d69e159792cbe641122e91bf9602b3e0f5edafa419edc3c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876089"
---
# <a name="tdm_click_verification-message"></a>Message de vérification de \_ clic TDM \_

Simule un clic de la case à cocher vérification d’une boîte de dialogue de tâche, si elle existe.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

**True** pour définir l’état de la case à cocher à vérifier ; **False** pour la désactiver.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

**True** pour définir le focus clavier sur la case à cocher ; **False** dans le cas contraire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





