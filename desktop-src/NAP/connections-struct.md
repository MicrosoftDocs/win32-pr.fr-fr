---
title: Structure des connexions (NapEnforcementClient. h)
description: Contient des informations sur la liste des connexions gérées par un enforceur.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Connexion de la structure NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f91e2dc404ff50c7edc3ba80a3c772ac6be762c1fe49575d8503a783e83bbef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800146"
---
# <a name="connections-structure"></a>Structure des connexions

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

La structure des **connexions** contient des informations sur la liste des connexions gérées par un dispositif d’application.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a>Membres

<dl> <dt>

**count**
</dt> <dd>

Nombre de connexions actives actuellement gérées par un application dans la plage 0 (zéro) à [**maxConnectionCountPerEnforcer**](nap-type-constants.md).

</dd> <dt>

**connexions**
</dt> <dd>

Pointeur COM vers une liste d’interfaces [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) qui représentent des connexions clientes.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                |
| En-tête<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence NAP](nap-reference.md)
</dt> <dt>

[Structures NAP](nap-structures.md)
</dt> <dt>

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





