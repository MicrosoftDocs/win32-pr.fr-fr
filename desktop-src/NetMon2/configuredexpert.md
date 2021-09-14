---
description: La structure CONFIGUREDEXPERT associe un expert à ses données de configuration.
ms.assetid: 96a6650b-6d6f-495e-83bb-385d44ff015d
title: CONFIGUREDEXPERT, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONFIGUREDEXPERT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3f3d40bf5d38c6b5151691a7d15bd93bef01eee5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127222700"
---
# <a name="configuredexpert-structure"></a>CONFIGUREDEXPERT, structure

La structure **CONFIGUREDEXPERT** associe un expert à ses données de configuration.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  HEXPERT       hExpert;
  DWORD         StartupFlags;
  PEXPERTCONFIG pConfig;
} CONFIGUREDEXPERT, *PCONFIGUREDEXPERT;
```



## <a name="members"></a>Membres

<dl> <dt>

**hExpert**
</dt> <dd>

Handle à un expert.

</dd> <dt>

**StartupFlags**
</dt> <dd>

Valeurs de l’indicateur de démarrage de l’expert.

</dd> <dt>

**pConfig**
</dt> <dd>

Pointeur vers une structure [**EXPERTCONFIG**](expertconfig.md) .

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




