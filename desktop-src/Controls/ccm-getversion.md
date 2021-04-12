---
title: Message CCM_GETVERSION (commctrl. h)
description: Obtient le numéro de version d’un contrôle défini par le message CCM SETVERSION le plus récent \_ .
ms.assetid: c4b401d7-bba0-430c-b368-c363d49b3411
keywords:
- CCM_GETVERSION les contrôles de message Windows
topic_type:
- apiref
api_name:
- CCM_GETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd302774f8821b51a4abaf72bccc403e7302e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104512"
---
# <a name="ccm_getversion-message"></a>Message de l’outil CCM. \_

Obtient le numéro de version d’un contrôle défini par le message [**CCM \_ SETVERSION**](ccm-setversion.md) le plus récent.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le numéro de version défini par le dernier message [**CCM \_ SETVERSION**](ccm-setversion.md) . Si aucun message de ce type n’a été envoyé, elle retourne la valeur zéro.

## <a name="remarks"></a>Notes

Ce message ne retourne pas la version de la DLL. Pour plus d’informations sur l’utilisation de [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) pour récupérer la version actuelle de la dll, consultez [versions de Shell](common-control-versions.md) .

> [!Note]  
> Le numéro de version est défini sur un contrôle en fonction du contrôle et peut ne pas être le même pour tous les contrôles.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

