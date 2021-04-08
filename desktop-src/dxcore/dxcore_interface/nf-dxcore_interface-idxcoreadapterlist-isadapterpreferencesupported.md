---
title: IDXCoreAdapterList::IsAdapterPreferenceSupported
description: Détermine si une valeur [DXCoreAdapterPreference](./ne-dxcore_interface-dxcoreadapterpreference.md) spécifiée est comprise par le système d’exploitation.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 1678568eb17c0dd833c130e6184931c8896261e9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728037"
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