---
title: Structure RAS_PARAMETERS (rassapi. h)
description: La \_ structure des paramètres RAS est utilisée par la fonction RasAdminPortGetInfo pour retourner le nom et la valeur d’un paramètre spécifique au média associé à un port sur un serveur RAS.
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS de la structure RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fffaefa8a6f2cffb895cc18882ed8fc0c382a4bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509070"
---
# <a name="ras_parameters-structure"></a>\_Structure des paramètres RAS

\[La structure des **\_ paramètres RAS** n’est pas prise en charge par Windows Vista.\]

La structure des **\_ paramètres RAS** est utilisée par la fonction [**RasAdminPortGetInfo**](rasadminportgetinfo.md) pour retourner le nom et la valeur d’un paramètre spécifique au média associé à un port sur un serveur RAS.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>Membres

<dl> <dt>

**\_Clé P**
</dt> <dd>

Spécifie le nom de la clé qui représente le paramètre spécifique au média, par exemple MAXCONNECTBPS.

</dd> <dt>

**\_Type P**
</dt> <dd>

Identifie le type de données associé au paramètre. Ce membre peut être l’une des valeurs suivantes de l’énumération de [**\_ \_ format des paramètres RAS**](ras-params-format-str.md) .



| Valeur                                                                                                                                                                                | Signification                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | Indique que les données associées à la clé sont un nombre.<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | Indique que les données associées à la clé sont une chaîne.<br/> |



 

</dd> <dt>

**\_Attributs P**
</dt> <dd>

Réservé.

</dd> <dt>

**\_Valeur P**
</dt> <dd>

Spécifie la valeur associée au paramètre. Ce membre est une Union de [**\_ \_ valeurs de paramètre RAS**](ras-params-value-str.md) . Si le membre de **\_ type P** est ParamNumber, le membre **Number** de l’Union contient la valeur. Si **P \_ type** est ParamString, le membre **String** de l’Union contient la valeur.

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

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





