---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Définit des constantes contrôlant la transformation appliquée dans les opérateurs DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) et **DML_OPERATOR_SPACE_TO_DEPTH1**.
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417215"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a>Énumération DML_DEPTH_SPACE_ORDER (directml. h)

Définit des constantes contrôlant la transformation appliquée dans les opérateurs DirectML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) et **DML_OPERATOR_SPACE_TO_DEPTH1**. Elles sont utilisées dans les structures [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .

> [!IMPORTANT]
> Cette API est disponible dans le cadre du package redistribuable autonome DirectML (consultez [Microsoft. ai. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1,4 et versions ultérieures. Consultez également [l’historique des versions DirectML](../dml-version-history.md).

## <a name="syntax"></a>Syntaxe
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a>Constantes

| Nom | Description |
| ---- |:---- |
| DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW | Provoque l’interprétation des dizaines d' [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et des [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) avec les dispositions suivantes, où les dimensions entre parenthèses sont aplaties ensemble.<br><br>- **Version de profondeur**: [lot, (BlockHeight, BlockWidth, canaux), hauteur, largeur]<br>- **Version d’espace**: [lot, canaux, (hauteur, BlockHeight), (largeur, BlockWidth)] |
| DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH | Provoque l’interprétation des dizaines d' [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et des [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) avec les dispositions suivantes, où les dimensions entre parenthèses sont aplaties ensemble.<br><br>- **Version de profondeur**: [lot, (canaux, BlockHeight, BlockWidth), hauteur, largeur]<br>- **Version d’espace**: [lot, canaux, (hauteur, BlockHeight), (largeur, BlockWidth)] |

## <a name="remarks"></a>Remarques

Pour obtenir des exemples illustrant l’effet de ces valeurs, consultez la documentation [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) et [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) .

## <a name="requirements"></a>Spécifications
| &nbsp; | &nbsp; |
| ---- |:---- |
| **En-tête** | directml. h |

## <a name="see-also"></a>Voir aussi

* [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a>Disponibilité
Cette énumération a été introduite dans `DML_FEATURE_LEVEL_2_1` .