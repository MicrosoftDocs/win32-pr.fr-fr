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
ms.openlocfilehash: 92b798ef8a5257afcb4e4ad653801bda0d21691057abad970d6e8158f592146e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673179"
---
# <a name="ras_params_format-enumeration"></a>\_Énumération de format des paramètres RAS \_

\[l’énumération de **\_ \_ FORMAT des paramètres RAS** n’est pas prise en charge à partir de Windows Vista.\]

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

 

 





