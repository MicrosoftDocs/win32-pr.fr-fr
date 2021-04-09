---
title: Message TDM_CLICK_VERIFICATION (commctrl. h)
description: Simule un clic de la case à cocher vérification d’une boîte de dialogue de tâche, si elle existe.
ms.assetid: 1c6c135e-4e39-4f1a-88f4-5e9f7181a2dd
keywords:
- TDM_CLICK_VERIFICATION les contrôles de message Windows
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
ms.openlocfilehash: df61676104169e3084e7cde09439c218f2237e60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102852"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





