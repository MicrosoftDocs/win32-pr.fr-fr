---
title: DXCoreHardwareID
description: Représente les éléments d’ID de matériel PnP pour un adaptateur.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 68cdb130dd6f0c0338e5b94da2f68c58f98bb91d404871e18ac82e817881117c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118626"
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