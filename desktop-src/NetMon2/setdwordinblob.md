---
description: La fonction SetDwordInBlob définit la valeur DWORD nommée d’un objet BLOB.
ms.assetid: 9174cd5c-4442-4fbe-8dc7-f8a74e1cc85d
title: SetDwordInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetDwordInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: a0fdc05052542c8606bf72d7250e29086a59b6cc69761229df4800abdc781027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364047"
---
# <a name="setdwordinblob-function"></a>SetDwordInBlob fonction)

La fonction **SetDwordInBlob** définit la valeur **DWORD** nommée d’un objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetDwordInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_       DWORD Dword
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle d’un objet BLOB en cours de définition.

</dd> <dt>

*pOwnerName* \[ dans\]
</dt> <dd>

Pointeur vers le nom du **propriétaire** de l’objet BLOB qui est défini.

</dd> <dt>

*pCategoryName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de **catégorie** d’objet BLOB qui est défini.

</dd> <dt>

*pTagName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de **balise** d’objet BLOB qui est défini.

</dd> <dt>

*Valeur DWORD* \[ dans\]
</dt> <dd>

Valeur **DWORD** de l’objet BLOB qui est défini.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

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

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetMacAddressInBlob](setmacaddressinblob.md)
</dt> <dt>

[SetNetworkInfoInBlob](setnetworkinfoinblob.md)
</dt> <dt>

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




