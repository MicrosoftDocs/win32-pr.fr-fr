---
description: La fonction SetMacAddressInBlob définit l’adresse MAC demandée d’un objet BLOB.
ms.assetid: f44d0cec-ced7-4d2a-a58e-aeb476bfe800
title: SetMacAddressInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetMacAddressInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 2183f5635dcdb15362a86a77ae2b3c109c71dbd5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194580"
---
# <a name="setmacaddressinblob-function"></a>SetMacAddressInBlob fonction)

La fonction **SetMacAddressInBlob** définit l’adresse Mac demandée d’un objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetMacAddressInBlob(
  _In_       HBLOB hBlob,
  _In_ const char  *pOwnerName,
  _In_ const char  *pCategoryName,
  _In_ const char  *pTagName,
  _In_ const BYTE  *pMacAddress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB qui est défini.

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

*pMacAddress* \[ dans\]
</dt> <dd>

Pointeur vers l’adresse MAC de l’objet BLOB en cours de définition.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[SetBoolInBlob](setboolinblob.md)
</dt> <dt>

[SetClassIDInBlob](setclassidinblob.md)
</dt> <dt>

[SetDwordInBlob](setdwordinblob.md)
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

 

 




