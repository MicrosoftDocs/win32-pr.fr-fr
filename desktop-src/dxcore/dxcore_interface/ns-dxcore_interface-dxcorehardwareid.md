---
title: DXCoreHardwareID
description: Représente les éléments d’ID de matériel PnP pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126916251"
---
# <a name="dxcorehardwareid-structure"></a>DXCoreHardwareID, structure

Représente les éléments d’ID de matériel PnP pour un adaptateur.

## <a name="syntax"></a>Syntaxe

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a>Membres

### <a name="vendorid"></a>vendorId

Type : **uint32_t \***

ID PCI du fournisseur de matériel de l’adaptateur.

### <a name="deviceid"></a>deviceId

Type : **uint32_t \***

ID PCI du périphérique matériel de l’adaptateur.

### <a name="subsysid"></a>subSysId

Type : **uint32_t \***

ID PCI du sous-système matériel de la carte.

### <a name="revision"></a>revision

Type : **uint32_t \***

ID PCI du numéro de révision de la carte.

## <a name="see-also"></a>Voir aussi

[Référence dxcore](../dxcore-reference.md), [utilisation de dxcore pour énumérer des adaptateurs](../dxcore-enum-adapters.md)