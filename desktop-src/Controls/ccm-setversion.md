---
title: Message CCM_SETVERSION (commctrl. h)
description: Ce message est utilisé pour informer le contrôle que vous attendez un comportement associé à une version particulière.
ms.assetid: f87b20bc-0139-4d0a-b38c-32c75743d6f6
keywords:
- CCM_SETVERSION les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CCM_SETVERSION
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9453b99ff9cd23675b3b5d79593071e4ebb3fbb65d06a78d0fe8094154b2486
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119320099"
---
# <a name="ccm_setversion-message"></a>\_Message CCM SETVERSION

Ce message est utilisé pour informer le contrôle que vous attendez un comportement associé à une version particulière.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Numéro de version.

</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la version spécifiée dans le message **\_ SETVERSION CCM** précédent. Si *wParam* est défini sur une valeur supérieure à la version actuelle de la dll, la valeur-1 est retournée.

## <a name="remarks"></a>Remarques

Dans certains cas, un contrôle peut se comporter différemment, selon la version. Cela s’applique principalement aux bogues qui ont été résolus dans les versions ultérieures. Le message **CCM \_ SETVERSION** vous permet d’informer le contrôle du comportement attendu. Vous pouvez déterminer la version que vous avez spécifiée en envoyant un message [**CCM \_ GETVERSION**](ccm-getversion.md) . Pour obtenir un exemple d’utilisation de ce message, consultez [dessin personnalisé avec les contrôles List-View et Tree-View](custom-draw.md).

Si vous avez ComCtl32.dll version 6 installée, quelle que soit la valeur que vous avez définie dans *wParam*, le message **CCM \_ SETVERSION** retourne la version 6.

> [!Note]  
> Ce message définit uniquement le numéro de version du contrôle auquel il est envoyé.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





