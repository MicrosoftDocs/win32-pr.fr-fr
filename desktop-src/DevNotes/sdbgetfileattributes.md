---
description: Récupère les données d’attribut pour le fichier spécifié.
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109918"
---
# <a name="sdbgetfileattributes-function"></a>SdbGetFileAttributes fonction)

Récupère les données d’attribut pour le fichier spécifié.

## <a name="syntax"></a>Syntaxe


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpwszFileName* \[ dans\]
</dt> <dd>

Chemin d'accès au fichier.

</dd> <dt>

*ppAttrInfo* \[ à\]
</dt> <dd>

Tableau de structures [**ATTRINFO**](attrinfo.md) qui contiennent les données d’attribut.

</dd> <dt>

*lpdwAttrCount* \[ à\]
</dt> <dd>

Nombre d'attributs.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La fonction retourne **true** en cas de réussite ou **false** en cas d’échec.

## <a name="remarks"></a>Notes

Une fois les données terminées, libérez-les à l’aide de la fonction [**SdbFreeFileAttributes**](sdbfreefileattributes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




