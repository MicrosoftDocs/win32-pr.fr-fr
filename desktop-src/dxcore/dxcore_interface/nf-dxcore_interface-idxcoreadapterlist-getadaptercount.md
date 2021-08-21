---
title: IDXCoreAdapterList::GetAdapterCount
description: Récupère le nombre de cartes dans un objet de liste d’adaptateurs DXCore.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 952120a039e4060a45f5e6e1de607fd68b50fcd7d7cd88ce5a98474f8f2dcfdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118985119"
---
# <a name="idxcoreadapterlistgetadaptercount-method"></a>IDXCoreAdapterList :: GetAdapterCount, méthode

Récupère le nombre de cartes dans un objet de liste d’adaptateurs DXCore. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual uint32_t STDMETHODCALLTYPE GetAdapterCount() = 0;
```

## <a name="returns"></a>Retours

Type : **uint32_t**

Retourne le nombre d’éléments de l’adaptateur dans la liste.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)