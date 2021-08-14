---
description: La fonction SetNPPAddressFilterInBlob définit le filtre d’adresse donné dans l’objet BLOB.
ms.assetid: bdd1482d-8be0-4999-9a7a-16b0400412fb
title: SetNPPAddressFilterInBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPAddressFilterInBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: da2119b30f690acf5deac46d43d9382e75c6caf1c2e9f41784a4b34f7f80e257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363815"
---
# <a name="setnppaddressfilterinblob-function"></a>SetNPPAddressFilterInBlob fonction)

La fonction **SetNPPAddressFilterInBlob** définit le filtre d’adresse donné dans l’objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD SetNPPAddressFilterInBlob(
  _In_ HBLOB          hBlob,
  _In_ LPADDRESSTABLE pAddressTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers un objet BLOB.

</dd> <dt>

*pAddressTable* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**ADDRESSTABLE**](addresstable.md) qui définit la table d’adresses allouées par l’utilisateur.

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

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
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

[SetNPPPatternFilterInBlob](setnpppatternfilterinblob.md)
</dt> <dt>

[SetNPPTriggerInBlob](setnpptriggerinblob.md)
</dt> <dt>

[SetStringInBlob](setstringinblob.md)
</dt> </dl>

 

 




