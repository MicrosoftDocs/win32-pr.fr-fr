---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Définit des constantes qui spécifient la direction d’une opération le long de l’axe donné pour l’opérateur (par exemple, la somme, en sélectionnant les éléments les plus hauts, en sélectionnant l’élément minimum).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_AXIS_DIRECTION
ms.openlocfilehash: 18cd2189f88378245be0824e0a68e5f618008bc7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106539783"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a>Énumération DML_AXIS_DIRECTION (directml. h)

Définit des constantes qui spécifient la direction d’une opération le long de l’axe donné pour l’opérateur (par exemple, la somme, en sélectionnant les éléments les plus hauts, en sélectionnant l’élément minimum).

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (voir [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a>Constantes

| Nom | Description |
| ---- |:---- |
| DML_AXIS_DIRECTION_INCREASING | Spécifie l’ordre d’incrémentation (à partir de l’index de poids faible vers l’index supérieur). |
| DML_AXIS_DIRECTION_DECREASING | Spécifie l’ordre décroissant (de l’index le plus élevé vers l’index faible). |


## <a name="requirements"></a>Configuration requise
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |