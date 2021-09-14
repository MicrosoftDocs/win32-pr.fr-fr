---
title: Message CCM_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle.
ms.assetid: 0200fa11-847f-477c-92e0-790b4d1ca0ef
keywords:
- CCM_SETWINDOWTHEME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CCM_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cea8996273a0c9d03123ce58f5fbb0dfb099be94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127007661"
---
# <a name="ccm_setwindowtheme-message"></a>\_Message CCM SETWINDOWTHEME

Définit le style visuel d’un contrôle.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le style visuel de contrôle à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





