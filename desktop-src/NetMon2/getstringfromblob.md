---
description: Retourne une chaîne située à une position donnée dans un objet BLOB.
ms.assetid: 5930a30b-f0ed-4d5b-a0ba-6cead55c2fcd
title: GetStringFromBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetStringFromBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 475600fb6128b5dbbaf9333f8c550351831f0a0f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121374"
---
# <a name="getstringfromblob-function"></a>GetStringFromBlob fonction)

La fonction **GetStringFromBlob** retourne une chaîne située à une position donnée dans un objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetStringFromBlob(
  _In_        HBLOB hBlob,
  _In_  const char  *pOwnerName,
  _In_  const char  *pCategoryName,
  _In_  const char  *pTagName,
  _Out_ const char  **ppString
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

Section **propriétaire** de l’objet BLOB dans laquelle se trouve la chaîne.

</dd> <dt>

*pCategoryName* \[ dans\]
</dt> <dd>

Section de **catégorie** BLOB dans laquelle se trouve la chaîne.

</dd> <dt>

*pTagName* \[ dans\]
</dt> <dd>

**Balise** de la chaîne demandée.

</dd> <dt>

*ppString* \[ à\]
</dt> <dd>

Pointeur vers une variable qui pointe vers la chaîne retournée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

Si le **propriétaire**, la **catégorie** ou les données de **balise** spécifiés n’existent pas, la fonction retourne l' **entrée d' \_ objet BLOB NMERR \_ \_ n' \_ \_ existe pas**.

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

[SetStringInBlob](setstringinblob.md)
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

[GetNPPAddressFilterFromBlob](getnppaddressfilterfromblob.md)
</dt> <dt>

[GetNPPPatternFilterFromBlob](getnpppatternfilterfromblob.md)
</dt> <dt>

[GetNPPTriggerFromBlob](getnpptriggerfromblob.md)
</dt> <dt>

[GetStringsFromBlob](getstringsfromblob.md)
</dt> </dl>

 

 




