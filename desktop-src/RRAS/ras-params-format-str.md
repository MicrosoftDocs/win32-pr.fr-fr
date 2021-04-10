---
title: Énumération RAS_PARAMS_FORMAT (rassapi. h)
description: Le \_ \_ type d’énumération de format params RAS est utilisé dans la \_ structure de paramètres RAS pour indiquer le type de données associé à une clé spécifique au média.
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT d’énumération RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104392"
---
# <a name="ras_params_format-enumeration"></a>\_Énumération de format des paramètres RAS \_

\[L’énumération de **\_ \_ format des paramètres RAS** n’est pas prise en charge par Windows Vista.\]

Le type d’énumération de **\_ \_ format params RAS** est utilisé dans la structure de [**\_ paramètres RAS**](ras-parameters-str.md) pour indiquer le type de données associé à une clé spécifique au média.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**
</dt> <dd>

Indique que les données associées à la clé sont un nombre.

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**
</dt> <dd>

Indique que les données associées à la clé sont une chaîne.

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

[Énumérations de l’administration du serveur RAS](ras-server-administration-enumerations.md)
</dt> <dt>

[**\_paramètres RAS**](ras-parameters-str.md)
</dt> </dl>

 

 





