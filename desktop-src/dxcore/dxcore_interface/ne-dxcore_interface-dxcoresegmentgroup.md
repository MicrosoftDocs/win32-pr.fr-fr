---
title: DXCoreSegmentGroup
description: Définit des constantes qui spécifient le regroupement des segments de mémoire d’un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: ce94d5f806879ea84f64c88d3a62b074a5c5415b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106536278"
---
# <a name="dxcoresegmentgroup-enum"></a>Énumération DXCoreSegmentGroup

Définit des constantes qui spécifient le regroupement des segments de mémoire d’un adaptateur.

## <a name="syntax"></a>Syntaxe

```cpp
enum class DXCoreSegmentGroup : uint32_t
{
  Local = 0,
  NonLocal = 1
};
```

## <a name="constants"></a>Constantes

### <a name="local"></a>Local

Spécifie un regroupement de segments considérés comme locaux sur l’adaptateur et représente la mémoire la plus rapide disponible pour le GPU. Votre application doit cibler le groupe de segments local en tant que taille cible de sa plage de travail.

### <a name="nonlocal"></a>Non locale

Spécifie un regroupement de segments considérés comme non locaux par l’adaptateur et peut avoir des performances plus lentes que le groupe de segments local.

## <a name="see-also"></a>Voir aussi

[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)