---
title: IDXCoreAdapter::IsAttributeSupported
description: Détermine si cet objet adaptateur DXCore prend en charge l’attribut d’adaptateur spécifié.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9824595326f9e81bfa21ab198a3f5b2e6eae74bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382100"
---
# <a name="idxcoreadapterisattributesupported-method"></a>IDXCoreAdapter :: IsAttributeSupported, méthode

Détermine si cet objet adaptateur DXCore prend en charge l’attribut d’adaptateur spécifié.

## <a name="syntax"></a>Syntaxe

```cpp
virtual bool STDMETHODCALLTYPE IsAttributeSupported( 
  REFGUID attributeGUID) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="attributeguid"></a>attributeGUID

Type : **REFGUID**

Référence à un GUID d’attribut d’adaptateur. Pour obtenir la liste des GUID d’attribut, consultez [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md).

## <a name="returns"></a>Retours

Type : **bool**

Retourne  `true`   si cet objet adaptateur dxcore prend en charge l’attribut d’adaptateur spécifié. Sinon, retourne  `false` .

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)