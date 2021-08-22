---
title: Message TB_SETWINDOWTHEME (commctrl. h)
description: Définit le style visuel d’un contrôle de barre d’outils.
ms.assetid: 8b05c561-af66-47e7-8ef3-7f9f81da4840
keywords:
- TB_SETWINDOWTHEME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_SETWINDOWTHEME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1f3f4ae5f6e7a3a05670a8ba9bfe533156e1ef3e6043ff2a039744da705da39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119078123"
---
# <a name="tb_setwindowtheme-message"></a>TO \_ SETWINDOWTHEME message

Définit le style visuel d’un contrôle de barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne Unicode qui contient le style visuel de la barre d’outils à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour n’est pas utilisée.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

L’envoi de ce message revient à appeler [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) dans la barre d’outils et son contrôle ToolTip, le cas échéant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





