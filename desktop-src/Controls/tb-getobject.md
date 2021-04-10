---
title: Message TB_GETOBJECT (commctrl. h)
description: Récupère le IDropTarget pour un contrôle ToolBar.
ms.assetid: b26394ea-6f0f-4084-956d-f9166cc54b76
keywords:
- TB_GETOBJECT les contrôles de message Windows
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
ms.openlocfilehash: ce923feaec893e6f4304eb0b993de33dc1fe2a97
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105055"
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

## <a name="remarks"></a>Notes

Le [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) de la barre d’outils est utilisé par la barre d’outils lorsque les objets sont glissés ou déplacés dessus.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

