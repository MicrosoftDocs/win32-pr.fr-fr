---
title: IDXCoreAdapter::IsSetStateSupported
description: Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge la définition de la valeur de l’état de l’adaptateur spécifié.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 284e38a622c882fce04278d9134908f55c9a25cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918016"
---
# <a name="idxcoreadapterissetstatesupported-method"></a>IDXCoreAdapter :: IsSetStateSupported, méthode

Détermine si cet objet adaptateur DXCore et le système d’exploitation actuel prennent en charge la définition de la valeur de l’état de l’adaptateur spécifié.

## <a name="syntax"></a>Syntaxe

```cpp
virtual bool STDMETHODCALLTYPE IsSetStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a>Paramètres

### <a name="state"></a>state

Type : **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**

Type d’élément d’État sur lequel vous effectuez une requête sur la prise en charge de. Consultez le tableau dans [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) pour plus d’informations sur chaque type d’état de l’adaptateur.

## <a name="returns"></a>Retours

Type : **bool**

Retourne `true` si cet objet adaptateur dxcore et le système d’exploitation actuel prennent en charge la définition de l’état de l’adaptateur spécifié. Sinon, retourne `false`.

## <a name="see-also"></a>Voir aussi

[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [référence dxcore](../dxcore-reference.md), [GUID d’attribut d’adaptateur dxcore](../dxcore-adapter-attribute-guids.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)