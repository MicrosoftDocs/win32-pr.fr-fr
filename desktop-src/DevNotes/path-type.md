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
ms.openlocfilehash: 1e5602aa7384c8de6c33b407e9a536141d8d002b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104522951"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




