---
title: Message TB_MAPACCELERATOR (commctrl. h)
description: Détermine l’ID du bouton qui correspond au caractère d’accélérateur spécifié.
ms.assetid: 724b593d-39af-4301-b721-0332844677b1
keywords:
- TB_MAPACCELERATOR les contrôles de message Windows
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
ms.openlocfilehash: 029584d9e1614a3a135da5ebd3f4f446795fd9ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742660"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ MAPACCELERATORW** (Unicode) et **to \_ MAPACCELERATORA** (ANSI)<br/>       |



 

 





