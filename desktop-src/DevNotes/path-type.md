---
description: Représente le type de chemin d’accès utilisé comme argument.
ms.assetid: f308c638-b383-432e-9dd3-edc33b792139
title: Énumération PATH_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATH_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: c05e71e485eaaf3ff309dc3a0df3d792ccd18c1438964d387afe969adbfd3fc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058599"
---
# <a name="path_type-enumeration"></a>\_Énumération de type de chemin

Représente le type de chemin d’accès utilisé comme argument.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _PATH_TYPE { 
  DOS_PATH,
  NT_PATH
} PATH_TYPE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="DOS_PATH"></span><span id="dos_path"></span>**\_chemin dos**
</dt> <dd>

Chemin standard.

</dd> <dt>

<span id="NT_PATH"></span><span id="nt_path"></span>**\_chemin d’accès NT**
</dt> <dd>

Chemin d’accès interne.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




