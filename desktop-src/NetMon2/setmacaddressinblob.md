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
ms.openlocfilehash: 20ed4a0358bc0aecada66858f9814bce94252ff9d705c971be947ca5af788ab3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118364057"
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

 

 




