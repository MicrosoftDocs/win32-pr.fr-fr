---
description: Définit une chaîne à un emplacement donné au sein d’un objet BLOB.
ms.assetid: 645e6b8b-aaaf-429f-ad2f-bf4364ef4e80
title: SetStringInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetStringInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 293aabf86769a8cfa678df79a04b5158b9c1d19c80d660b144c4a33cbf32c56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363678"
---
# <a name="setstringinblob-function"></a>SetStringInBlob fonction)

La fonction **SetStringInBlob** définit une chaîne à un emplacement donné au sein d’un objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetStringInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const char  *pString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB.

</dd> <dt>

*pOwnerName* \[ dans\]
</dt> <dd>

Pointeur vers la section **propriétaire** de l’objet BLOB, où la chaîne est définie.

</dd> <dt>

*pCategoryName* \[ dans\]
</dt> <dd>

Pointeur vers la section de **catégorie** de l’objet BLOB, où la chaîne est définie.

</dd> <dt>

*pTagName* \[ dans\]
</dt> <dd>

Pointeur vers la **balise** de la chaîne demandée.

</dd> <dt>

*pString* \[ dans\]
</dt> <dd>

Pointeur vers la variable où un pointeur vers la chaîne sera retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique le problème.

Si les informations de **propriétaire**, de **catégorie** ou de **balise** spécifiées n’existent pas, la valeur de retour est NMERR l' \_ entrée d’objet BLOB \_ \_ n' \_ \_ existe pas.

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

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
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
</dt> </dl>

 

 




