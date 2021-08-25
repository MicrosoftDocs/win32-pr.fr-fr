---
title: RAS_PARAMS_VALUE Union (rassapi. h)
description: La \_ \_ valeur Union des paramètres RAS est utilisée dans la \_ structure de paramètres RAS pour stocker les données associées à un paramètre spécifique au média.
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS RAS_PARAMS_VALUE Union
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07453b707012c966fc298cc61973cb056b42d741d861a22204c17eec5265317f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909599"
---
# <a name="ras_params_value-union"></a>Union des valeurs des \_ paramètres RAS \_

\[l’union des **\_ \_ valeurs des paramètres RAS** n’est pas prise en charge à partir de Windows Vista.\]

La **\_ \_ valeur** Union des paramètres RAS est utilisée dans la structure de [**\_ paramètres RAS**](ras-parameters-str.md) pour stocker les données associées à un paramètre spécifique au média. Le membre de **\_ type P** de la structure de **\_ paramètres RAS** utilise une valeur de l’énumération de [**\_ \_ format params**](ras-params-format-str.md) des paramètres d’accès distant pour indiquer le type de valeur actuellement stocké dans la **\_ \_ valeur** des paramètres RAS.

## <a name="syntax"></a>Syntaxe


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a>Membres

<dl> <dt>

**Nombre**
</dt> <dd>

Si le membre de **\_ type P** de la structure de [**\_ paramètres ras**](ras-parameters-str.md) est ParamNumber, le membre **Number** contient la valeur du paramètre spécifique au média. Par exemple, le paramètre MAXCONNECTBPS est de type ParamNumber, et la valeur peut être 19200.

Si le membre de **\_ type P** de la structure de [**\_ paramètres ras**](ras-parameters-str.md) est ParamNumber, le membre **Number** contient la valeur du paramètre spécifique au média. Par exemple, le paramètre MAXCONNECTBPS est de type ParamNumber, et la valeur peut être 19200.

</dd> <dt>

**Chaîne**
</dt> <dd>

Si le membre de **\_ type P** de la structure de [**\_ paramètres RAS**](ras-parameters-str.md) est ParamString, le membre de **chaîne** contient la valeur du paramètre spécifique au média.

<dl> <dt>

**Durée**
</dt> <dd>

Spécifie la longueur, en caractères, de la chaîne vers laquelle pointe le membre de **données** .

</dd> <dt>

**Données**
</dt> <dd>

Pointeur vers une mémoire tampon qui contient la valeur de chaîne d’un paramètre spécifique au média.

</dd> </dl> </dd> </dl>

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

[Union d’administration du serveur RAS](ras-server-administration-union.md)
</dt> <dt>

[**\_paramètres RAS**](ras-parameters-str.md)
</dt> <dt>

[**\_format des paramètres \_ RAS**](ras-params-format-str.md)
</dt> </dl>

 

 





