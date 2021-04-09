---
title: Message TB_GETITEMDROPDOWNRECT (commctrl. h)
description: Obtient le rectangle englobant de la fenêtre déroulante pour un élément de barre d’outils avec une \_ liste déroulante BTNS style.
ms.assetid: 4b59c96b-8d75-44c1-b771-c1d62502a2c2
keywords:
- TB_GETITEMDROPDOWNRECT les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_GETITEMDROPDOWNRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbcbcef725b0ade0bfc776200fa5b191618d2ccb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032483"
---
# <a name="tb_getitemdropdownrect-message"></a>TO \_ GETITEMDROPDOWNRECT message

Obtient le rectangle englobant de la fenêtre déroulante pour un élément de barre d’outils avec une [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md)style.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Index de base zéro de l’élément de contrôle de barre d’outils pour lequel récupérer le rectangle englobant.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>Pointeur vers une structure <a href="/previous-versions//dd162897(v=vs.85)">**Rect**</a> pour recevoir les informations de rectangle englobant. L’expéditeur du message est chargé d’allouer cette structure. Les coordonnées retournées dans la structure **Rect** sont exprimées en tant que coordonnées clientes.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne toujours une valeur différente de zéro.

## <a name="remarks"></a>Notes

L’élément doit avoir le style de [**\_ liste déroulante BTNS**](toolbar-control-and-button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

