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
ms.openlocfilehash: 60561e4af54c6d27288d8df311693d51c0b9fc77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740581"
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

 

 





