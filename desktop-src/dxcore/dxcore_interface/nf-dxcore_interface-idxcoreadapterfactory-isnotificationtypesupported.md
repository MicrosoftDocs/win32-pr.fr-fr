---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Détermine si un type de notification spécifié est pris en charge par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126917992"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a>IDXCoreAdapterFactory :: IsNotificationTypeSupported, méthode

Détermine si un type de notification spécifié est pris en charge par le système d’exploitation. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="notificationtype"></a>notificationType

Type : **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**

Le type de notification que vous interrogez sur la prise en charge de. Pour plus d’informations sur les types de notification, consultez le tableau dans [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) .

## <a name="returns"></a>Retours

Type : **bool**

Retourne `true` si le type de notification est pris en charge par le système. Sinon, retourne `false`.

## <a name="remarks"></a>Notes

Vous pouvez appeler **IsNotificationTypeSupported** pour déterminer si un type de notification donné est connu pour cette version du système d’exploitation. par exemple, un type de notification introduit dans une version particulière de Windows est inconnu des versions précédentes de Windows.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)