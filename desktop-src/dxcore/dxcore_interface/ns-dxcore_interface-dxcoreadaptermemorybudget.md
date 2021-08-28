---
title: DXCoreAdapterMemoryBudget
description: Décrit le budget de mémoire pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 2cbe109d4c7f6c03389ec9e51c9468c601730890220fde2dea72aed476093f47
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118683"
---
# <a name="dxcoreadaptermemorybudget-structure"></a>DXCoreAdapterMemoryBudget, structure

Spécifie l’état de l’adaptateur <em>AdapterMemoryBudget</em> , qui récupère ou demande le budget de mémoire de l’adaptateur sur l’adaptateur. Le paramètre (demande) d’un budget représente la mémoire physique minimale requise à réserver, en octets, sur l’adaptateur. Nous vous recommandons de définir une réservation d’adaptateur pour indiquer la quantité de mémoire physique que votre application ne peut pas déconnecter sans. Cette valeur permet au système d’exploitation de réduire rapidement l’impact des situations de sollicitation importante de la mémoire.

Lors de l’appel de [QueryState](./nf-dxcore_interface-idxcoreadapter-querystate.md), l’état de l’adaptateur <em>AdapterMemoryBudget</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> pour *inputStateDetails* et le type **DXCoreAdapterMemoryBudget** pour *OUTPUTBUFFER*.

Lors de l’appel de [SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md), l’état de l’adaptateur <em>AdapterMemoryBudget</em> a le type <a href="/windows/win32/dxcore/dxcore_interface/ns-dxcore_interface-dxcoreadaptermemorybudgetnodesegmentgroup">DXCoreAdapterMemoryBudgetNodeSegmentGroup</a> pour *inputStateDetails* et le type **uint64_t** pour *inputData*.

## <a name="syntax"></a>Syntaxe

```cpp
struct DXCoreAdapterMemoryBudget
{
  uint64_t budget;
  uint64_t currentUsage;
  uint64_t availableForReservation;
  uint64_t currentReservation;
};
```

## <a name="members"></a>Membres

### <a name="budget"></a>budget

Type : **uint64_t**

Spécifie le budget de mémoire de l’adaptateur fourni par le système d’exploitation, en octets, que votre application doit cibler. Si la valeur de *currentUsage* est supérieure à celle du *budget*, votre application risque de subir des interruptions ou des altérations de performances dues à l’activité en arrière-plan par le système d’exploitation, qui est destinée à fournir à d’autres applications une utilisation équitable de la mémoire de l’adaptateur.

### <a name="currentusage"></a>currentUsage

Type : **uint64_t**

Spécifie l’utilisation actuelle de la mémoire de l’adaptateur application, en octets.

### <a name="availableforreservation"></a>availableForReservation

Type : **uint64_t**

Spécifie la quantité de mémoire de l’adaptateur, en octets, que votre application peut réserver. Pour réserver cette mémoire d’adaptateur, votre application doit appeler [IDXCoreAdapter :: SetState](./nf-dxcore_interface-idxcoreadapter-setstate.md) avec l' *État* défini sur [DXCoreAdapterState :: AdapterMemoryBudget](./ne-dxcore_interface-dxcoreadapterstate.md).

### <a name="currentreservation"></a>currentReservation

Type : **uint64_t**

Spécifie la quantité de mémoire de l’adaptateur, en octets, qui est réservée par votre application. Le système d’exploitation utilise la réservation comme indicateur pour déterminer la plage de travail minimale de votre application. Votre application doit tenter de s’assurer que l’utilisation de la mémoire de l’adaptateur peut être réduite pour répondre à cette exigence.

## <a name="see-also"></a>Voir aussi

[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)