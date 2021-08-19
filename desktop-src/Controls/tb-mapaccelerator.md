---
title: Message TB_MAPACCELERATOR (commctrl. h)
description: Détermine l’ID du bouton qui correspond au caractère d’accélérateur spécifié.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_MAPACCELERATOR
- TB_MAPACCELERATORA
- TB_MAPACCELERATORW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f905ccf5ea01e3c06cb87a160a44598c2c4a7790c972f4ee83b245e3ed5c0111
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168083"
---
# <a name="tb_mapaccelerator-message"></a>TO \_ MAPACCELERATOR message

Détermine l’ID du bouton qui correspond au caractère d’accélérateur spécifié.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Caractère d’accélérateur.

</dd> <dt>

*lParam* \[ à\]
</dt> <dd>

Pointeur vers un **uint**. En cas de retour, en cas de réussite, ce paramètre contiendra l’ID du bouton avec *wParam* comme caractère d’accélérateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro si l’un des boutons a *wParam* comme caractère d’accélérateur, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ MAPACCELERATORW** (Unicode) et **to \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





