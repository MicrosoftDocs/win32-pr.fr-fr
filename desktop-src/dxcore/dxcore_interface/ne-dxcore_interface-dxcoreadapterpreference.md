---
title: DXCoreAdapterPreference
description: Définit des constantes qui spécifient les préférences d’adaptateur DXCore à utiliser comme critères de tri de liste.
ms.localizationpriority: low
ms.topic: reference
ms.date: 09/03/2019
ms.openlocfilehash: a58f2c948751d5217a89e52bc862057ac6a67c85bdf2fabed96c2b5ad68364cc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117729"
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