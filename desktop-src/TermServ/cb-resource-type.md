---
title: Énumération CB_RESOURCE_TYPE (Cbclient. h)
description: Spécifie le type de ressource auquel la connexion entrante est connectée.
ms.assetid: 80D921BF-2D84-4A18-9544-50087B81F177
ms.tgt_platform: multiple
keywords:
- Énumération CB_RESOURCE_TYPE Services Bureau à distance
topic_type:
- apiref
api_name:
- CB_RESOURCE_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63dfce0f575147233735dd943645eb51c26141cacaaa61c044698b29b8d118e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139112"
---
# <a name="cb_resource_type-enumeration"></a>\_Énumération de type de ressource CB \_

Spécifie le type de ressource auquel la connexion entrante est connectée. Cette énumération est utilisée avec la structure d' [**\_ \_ informations de connexion CB**](cb-connection-info.md) .

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _CB_RESOURCE_TYPE { 
  CB_RESOURCE_UNDEFINED  = 0,
  CB_RESOURCE_SESSION    = 1,
  CB_RESOURCE_VM
} CB_RESOURCE_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="CB_RESOURCE_UNDEFINED"></span><span id="cb_resource_undefined"></span>**\_ressource CB \_ non définie**
</dt> <dd>

Le type de ressource n’est pas défini.

</dd> <dt>

<span id="CB_RESOURCE_SESSION"></span><span id="cb_resource_session"></span>**\_session de ressources CB \_**
</dt> <dd>

La ressource est une session à distance.

</dd> <dt>

<span id="CB_RESOURCE_VM"></span><span id="cb_resource_vm"></span>**\_ \_ machine virtuelle de la ressource CB**
</dt> <dd>

La ressource est une machine virtuelle.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                        |
| En-tête<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_informations de connexion CB \_**](cb-connection-info.md)
</dt> </dl>

 

 





