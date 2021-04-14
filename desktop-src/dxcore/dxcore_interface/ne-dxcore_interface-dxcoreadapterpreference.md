---
title: DXCoreAdapterPreference
description: Définit des constantes qui spécifient les préférences d’adaptateur DXCore à utiliser comme critères de tri de liste.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: 4301bdc1fe0ece8d9594ec3287e2ea8ddcce8f0a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382384"
---
# <a name="dxcoreadapterpreference-enum"></a>Énumération DXCoreAdapterPreference

## <a name="description"></a>Description

Définit des constantes qui spécifient les préférences d’adaptateur DXCore à utiliser comme critères de tri de liste. Vous pouvez trier une liste d’adaptateurs DXCore en passant un tableau de **DXCoreAdapterPreference** à [IDXCoreAdapterList :: sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md).

## <a name="syntax"></a>Syntaxe

```cpp
enum class DXCoreAdapterPreference : uint32_t
{
  Hardware = 0,
  MinimumPower = 1,
  HighPerformance = 2
};
```

## <a name="enum-fields"></a>Champs d’énumération

### <a name="hardware"></a>Matériel

Spécifie une préférence pour les cartes matérielles (par opposition aux adaptateurs logiciels).

### <a name="minimumpower"></a>MinimumPower

Spécifie une préférence pour le GPU avec une alimentation minimale (comme un processeur graphique intégré ou iGPU).

### <a name="highperformance"></a>HighPerformance

Spécifie une préférence pour le GPU le plus performant, tel qu’un processeur graphique externe (xGPU), s’il est disponible, ou un processeur graphique discret (dGPU) s’il est disponible.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterList :: sort](./nf-dxcore_interface-idxcoreadapterlist-sort.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)