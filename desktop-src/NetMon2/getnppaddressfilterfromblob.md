---
description: La fonction GetNPPAddressFilterFromBlob remplit le filtre d’adresse donné avec les informations stockées dans l’objet BLOB.
ms.assetid: b34e0e52-1b2a-4d61-b60c-f1b19ff8ff38
title: GetNPPAddressFilterFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPAddressFilterFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 944821620123d63f654e286a77018232c79981e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952885"
---
# <a name="getnppaddressfilterfromblob-function"></a>GetNPPAddressFilterFromBlob fonction)

La fonction **GetNPPAddressFilterFromBlob** remplit le filtre d’adresse donné avec les informations stockées dans l’objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetNPPAddressFilterFromBlob(
  _In_    HBLOB          hBlob,
  _Inout_ LPADDRESSTABLE pAddressTable,
  _Out_   HBLOB          hErrorBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers un objet BLOB.

</dd> <dt>

*pAddressTable* \[ in, out\]
</dt> <dd>

Pointeur vers la table d’adresses allouées par l’utilisateur.

</dd> <dt>

*hErrorBlob* \[ à\]
</dt> <dd>

Handle vers un objet BLOB d’erreurs qui spécifie où l’erreur (le cas échéant) dans l’objet BLOB d’origine s’est produite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.

## <a name="remarks"></a>Notes

Les informations d’adresse sont stockées dans la section de **configuration** de la catégorie **propriétaire** de l’objet BLOB NPP.

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

[SetNPPAddressFilterInBlob](setnppaddressfilterinblob.md)
</dt> <dt>

[GetBoolFromBlob](getboolfromblob.md)
</dt> <dt>

[GetClassIDFromBlob](getclassidfromblob.md)
</dt> <dt>

[GetDwordFromBlob](getdwordfromblob.md)
</dt> <dt>

[GetMacAddressFromBlob](getmacaddressfromblob.md)
</dt> <dt>

[GetNetworkInfoFromBlob](getnetworkinfofromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringFromBlob](getstringfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




