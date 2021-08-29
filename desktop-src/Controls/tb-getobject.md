---
title: Message TB_GETOBJECT (commctrl. h)
description: Récupère le IDropTarget pour un contrôle ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETOBJECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4671c3b6998c170f6ef59e8a0019b58a166728d1c560eac8420dbaf40c4dcb0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061339"
---
# <a name="tb_getobject-message"></a>TO \_ GETOBJECT message

Récupère le [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) pour un contrôle ToolBar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de l’interface demandée. Cette valeur doit pointer sur l' **IID \_ IDropTarget**.

</dd> <dt>

*lParam* 
</dt> <dd>

Adresse qui reçoit le pointeur d’interface. Si une erreur se produit, un pointeur **null** est placé dans cette adresse.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** indiquant la réussite ou l’échec de l’opération.

## <a name="remarks"></a>Remarques

Le [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de la barre d’outils est utilisé par la barre d’outils lorsque les objets sont glissés ou déplacés dessus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

