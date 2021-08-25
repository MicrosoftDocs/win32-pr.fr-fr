---
title: IDXCoreAdapter::IsValid
description: Détermine si cet objet adaptateur DXCore est toujours valide.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6b8a0ccadb46f20db9c5f2a23ac8709b391254ee453f05424dadee309f33fc40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842539"
---
# <a name="idxcoreadapterisvalid-method"></a>IDXCoreAdapter :: IsValid, méthode

Détermine si cet objet adaptateur DXCore est toujours valide. Pour obtenir des conseils de programmation et des exemples de code, consultez [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md).

## <a name="syntax"></a>Syntaxe

```cpp
virtual bool STDMETHODCALLTYPE IsValid() = 0;
```

## <a name="returns"></a>Retours

Type : **bool**

Retourne `true` si cet objet adaptateur dxcore est toujours valide. Sinon, retourne `false`.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer les adaptateurs](../dxcore-enum-adapters.md)