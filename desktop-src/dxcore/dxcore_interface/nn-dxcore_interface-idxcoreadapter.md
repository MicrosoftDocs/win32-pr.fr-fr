---
title: IDXCoreAdapter
description: L’interface **IDXCoreAdapter** implémente des méthodes pour récupérer des détails sur un élément de l’adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 18cdd8082701ea4f1a8b5a3cfa047decd0f77df81b17eebe49bf5a8a887663fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118278786"
---
# <a name="idxcoreadapter-interface"></a>Interface IDXCoreAdapter

L’interface **IDXCoreAdapter** implémente des méthodes pour récupérer des détails sur un élément de l’adaptateur. **IDXCoreAdapter** hérite de l’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="remarks"></a>Notes

Les propriétés d’un adaptateur sont établies au moment du démarrage de l’adaptateur et sont immuables pendant toute la durée de vie de l’adaptateur. Cela diffère de l’état d’une carte, qui peut être interrogé ou défini, et dont les valeurs peuvent changer au fil du temps.

## <a name="see-also"></a>Voir aussi

[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)