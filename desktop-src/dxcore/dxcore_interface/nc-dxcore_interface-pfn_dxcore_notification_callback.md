---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Fonction de rappel (implémentée par votre application), qui est appelée par un objet DXCore pour les événements de notification.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: f86bef2d2183562b322cdc0b01ffb64d25b23bb64dd8967e09e2dd761f7654b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787099"
---
# <a name="pfn_dxcore_notification_callback-callback"></a>Rappel de PFN_DXCORE_NOTIFICATION_CALLBACK

Fonction de rappel (implémentée par votre application), qui est appelée par un objet DXCore pour les événements de notification.

## <a name="syntax"></a>Syntaxe

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a>Paramètres

### <a name="notificationtype"></a>notificationType

Type : **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Type de notification représentant cet appel. Consultez le tableau dans [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) pour plus d’informations sur les types qui sont valides avec les genres d’objets.

### <a name="object"></a>object

Type : **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

Objet [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) ou [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) déclenchant la notification.

### <a name="context-in"></a>contexte [in]

Type : **void \***

Pointeur, qui peut être `nullptr` , vers un objet contenant des informations de contexte.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)