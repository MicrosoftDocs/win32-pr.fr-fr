---
title: IDXCoreAdapter::IsPropertySupported
description: Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge la propriété de l’adaptateur spécifiée.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106538598"
---
# <a name="idxcoreadapterispropertysupported-method"></a>IDXCoreAdapter :: IsPropertySupported, méthode

Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge la propriété de l’adaptateur spécifiée.

## <a name="syntax"></a>Syntaxe

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="property"></a>propriété

Type : **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**

Type de propriété pour lequel vous effectuez une requête sur la prise en charge de. Consultez le tableau dans [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) pour plus d’informations sur chaque propriété de l’adaptateur.

## <a name="returns"></a>Retours

Type : **bool**

Retourne  `true`   si cet objet adaptateur dxcore et le système d’exploitation actuel prennent en charge la propriété de l’adaptateur spécifiée. Sinon, retourne  `false` .

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)