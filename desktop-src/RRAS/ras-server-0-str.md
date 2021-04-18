---
title: Structure RAS_SERVER_0 (rassapi. h)
description: La \_ structure du serveur RAS \_ 0 est utilisée par la fonction RasAdminServerGetInfo pour retourner des informations sur les ports configurés sur un serveur RAS.
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 de la structure RAS
- Point d’accès RAS du pointeur de structure PRAS_SERVER_0
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509124"
---
# <a name="ras_server_0-structure"></a>\_Structure du serveur RAS \_ 0

\[La structure du **\_ serveur RAS \_ 0** n’est pas prise en charge à partir de Windows Vista.\]

La structure du **\_ serveur RAS \_ 0** est utilisée par la fonction [**RasAdminServerGetInfo**](rasadminservergetinfo.md) pour retourner des informations sur les ports configurés sur un serveur RAS.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a>Membres

<dl> <dt>

**TotalPorts**
</dt> <dd>

Spécifie le nombre total de ports configurés sur le serveur RAS et disponibles pour la connexion des clients distants. Par exemple, si le nombre total de ports configurés pour la connexion à un serveur est de quatre, mais que l’un des ports est actuellement utilisé pour la numérotation, **TotalPorts** est trois.

</dd> <dt>

**PortsInUse**
</dt> <dd>

Spécifie le nombre de ports actuellement utilisés par les clients distants.

</dd> <dt>

**RasVersion**
</dt> <dd>

Spécifie la version du serveur RAS. Utilisez ces informations pour prendre une mesure propre à la version. Ce membre est l’une des valeurs suivantes.



| Valeur                                                                                                                                                                  | Signification                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <dt>**RASDOWNLEVEL**</dt> </dl>              | Indique un serveur RAS LAN Manager version 1,0.<br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <dt>**RASADMIN \_ 35**</dt> </dl>                | Indique un serveur ou un client RAS Windows NT Server 3,51 et antérieur.<br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <dt>**RASADMIN \_ actuel**</dt> </dl> | Indique un client ou un serveur RAS Windows NT 4,0.<br/>                     |



 

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| Fin de la prise en charge des clients<br/>    | Windows XP<br/>                                                                |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2003<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble du service d’accès à distance (RAS)](about-remote-access-service.md)
</dt> <dt>

[Structures d’administration de serveur RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminServerGetInfo**](rasadminservergetinfo.md)
</dt> </dl>

 

 





