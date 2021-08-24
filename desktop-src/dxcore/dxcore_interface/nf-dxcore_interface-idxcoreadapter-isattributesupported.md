---
title: IDXCoreAdapter::IsAttributeSupported
description: Détermine si cet objet adaptateur DXCore prend en charge l’attribut d’adaptateur spécifié.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 9dda05ca9dc1d3b7a7a84792c7ac122bb64144d5fdba3ad630be1a3f4d9ddf24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787079"
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

Retourne `true` si cet objet adaptateur dxcore prend en charge l’attribut d’adaptateur spécifié. Sinon, retourne `false`.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)