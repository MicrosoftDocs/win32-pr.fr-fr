---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Détermine si une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) spécifiée est comprise par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: f8a42040ecd6c5667a3d33fb506fd97cfdfe53e8950c2e42b6068bbed6c19467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118502580"
---
# <a name="idxcoreadapterlistisadapterpreferencesupported-method"></a>IDXCoreAdapterList :: IsAdapterPreferenceSupported, méthode

## <a name="description"></a>Description

Détermine si une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) spécifiée est comprise par le système d’exploitation actuel. Vous pouvez appeler **IsAdapterPreferenceSupported** avant d’appeler [IDXCoreAdapterList :: sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Syntaxe

```cpp
bool IsAdapterPreferenceSupported(
  DXCoreAdapterPreference preference
);
```

## <a name="parameters"></a>Paramètres

### <a name="preference"></a>preference

Type : **[DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md)**

Valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) qui sera vérifiée pour déterminer si elle est prise en charge par le système d’exploitation.

## <a name="returns"></a>Retours

Type : **bool**

Retourne `true` si le type de tri est interprété par le système d’exploitation actuel. Sinon, retourne `false`.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)