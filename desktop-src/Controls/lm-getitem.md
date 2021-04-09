---
title: Message LM_GETITEM (commctrl. h)
description: Récupère les États et les attributs d’un élément.
ms.assetid: 75381f28-04d7-4a5c-bc0e-4cc74a06553f
keywords:
- LM_GETITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- LM_GETITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbb0e05f896df00f3762c53e6f5f62119cb3645f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102920"
---
# <a name="lm_getitem-message"></a>\_Message LM GETITEM

Récupère les États et les attributs d’un élément.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit avoir la **valeur null**. </dd> <dt>

*lParam* 
</dt> <dd>Pointeur vers une structure <a href="/windows/win32/api/commctrl/ns-commctrl-litem">litem</a> à remplir avec des informations sur l’élément. </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si le message parvient à obtenir les valeurs et les attributs spécifiés.

## <a name="remarks"></a>Notes

Avec le message **LM \_ GETITEM** , les liens sont accessibles uniquement par le biais de l’index numérique renvoyé dans le membre **iLink** de [**litem**](/windows/win32/api/commctrl/ns-commctrl-litem). L’accès au lien via le nom d’ID renvoyé dans **szID** n’est pas pris en charge.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





