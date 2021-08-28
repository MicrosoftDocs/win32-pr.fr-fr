---
description: Récupère une valeur booléenne nommée à partir d’un objet BLOB.
ms.assetid: 26acfd2a-5b17-47ad-8f7b-7793174a13c3
title: GetBoolFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBoolFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: ec9f5333e3f85f92b30d52689288c971ca04437df647a7a7e5fe89379e06533e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743919"
---
# <a name="getboolfromblob-function"></a>GetBoolFromBlob fonction)

La fonction **GetBoolFromBlob** récupère une valeur booléenne nommée à partir d’un objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetBoolFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_       BOOL  *pBool
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle d’un objet BLOB.

</dd> <dt>

*pOwnerName* \[ dans\]
</dt> <dd>

Pointeur vers le nom du propriétaire de l’objet BLOB.

</dd> <dt>

*pCategoryName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de la catégorie d’objet BLOB.

</dd> <dt>

*pTagName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de la balise d’objet BLOB.

</dd> <dt>

*pBool* \[ à\]
</dt> <dd>

Pointeur vers la valeur booléenne de l’objet BLOB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




