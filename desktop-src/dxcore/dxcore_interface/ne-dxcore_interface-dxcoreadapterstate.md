---
title: DXCoreAdapterState
description: Définit des constantes qui spécifient les genres d’États de l’adaptateur DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: e588b75360c141b52989aa14e88c886092af2647
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315558"
---
# <a name="dxcoreadapterstate-enum"></a>Énumération DXCoreAdapterState

Définit des constantes qui spécifient les genres d’États de l’adaptateur DXCore. Transmettez l’une de ces constantes à la méthode [IDXCoreAdapter :: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) pour récupérer l’élément d’état de l’adaptateur pour un genre d’État ; transmettez une constante à la méthode [IDXCoreAdapter :: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) pour définir les informations d’un adaptateur pour un élément d’État.

## <a name="syntax"></a>Syntaxe

```cpp
enum class DXCoreAdapterState : uint32_t
{
  IsDriverUpdateInProgress = 0,
  AdapterMemoryBudget = 1
};
```

## <a name="constants"></a>Constantes

### <a name="isdriverupdateinprogress"></a>IsDriverUpdateInProgress

Spécifie l’état de l’adaptateur <em>IsDriverUpdateInProgress</em> , qui `true` indique qu’une mise à jour du pilote a été lancée sur l’adaptateur, mais qu’elle n’est pas encore terminée. Si la mise à jour du pilote est déjà terminée, cela signifie que l’adaptateur a été invalidé et que votre appel [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md) retourne un <b>HRESULT</b> de <b>DXGI_ERROR_DEVICE_REMOVED</b>.

Lors de l’appel de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l’élément d’état <em>IsDriverUpdateInProgress</em> a le type <b>Uint8_t</b>, représentant une valeur booléenne.

<b>Important</b>. Cet élément d’État n’est pas pris en charge pour [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md).

### <a name="adaptermemorybudget"></a>AdapterMemoryBudget

Spécifie l’état de l’adaptateur <em>AdapterMemoryBudget</em> , qui récupère ou demande le budget de mémoire de l’adaptateur sur l’adaptateur.

Lors de l’appel de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l’état de l’adaptateur <em>AdapterMemoryBudget</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> pour *inputStateDetails* et le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudget">DXCoreAdapterMemoryBudget</a> pour *OUTPUTBUFFER*.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter :: QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), [IDXCoreAdapter :: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)