---
description: Représente la méthode qui est appelée lorsqu’une action asynchrone se termine.
ms.assetid: B410E7C1-B108-4204-9AD1-663F7E05BBC3
title: Interface AsyncActionCompletedHandler
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncActionCompletedHandler
api_type:
- COM
api_location:
- Windows.Foundation.idl
ms.openlocfilehash: 5d7e091ab250dc8b7475dbf17a1d1502cd1c4aa110106584c8c8b190c927f4aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561174"
---
# <a name="asyncactioncompletedhandler-interface"></a>Interface AsyncActionCompletedHandler

Représente la méthode qui est appelée lorsqu’une action asynchrone se termine.

## <a name="members"></a>Membres

L’interface **AsyncActionCompletedHandler** hérite de [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo). **AsyncActionCompletedHandler** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **AsyncActionCompletedHandler** possède ces méthodes.



| Méthode                                               | Description                                                                                    |
|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**Appeler**](asyncactioncompletedhandler-invoke.md) | Appelle la méthode qui est appelée lorsque l’action asynchrone spécifiée se termine.<br/> |



 

## <a name="remarks"></a>Remarques

Assignez un **AsyncActionCompletedHandler** à un [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) pour recevoir une notification lorsque l’action asynchrone se termine.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                    |
| En-tête<br/>                   | <dl> <dt>Windows. Foundation. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo)
</dt> </dl>

 

