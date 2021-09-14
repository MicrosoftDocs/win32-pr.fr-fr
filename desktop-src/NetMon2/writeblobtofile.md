---
description: La fonction WriteBlobToFile écrit un objet BLOB dans un fichier.
ms.assetid: 0793dced-82c2-4553-90b2-acf594c6749e
title: WriteBlobToFile, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WriteBlobToFile
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5fbf17b76631da6dbff9ef2077776106505a37b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194491"
---
# <a name="writeblobtofile-function"></a>WriteBlobToFile fonction)

La fonction **WriteBlobToFile** écrit un objet BLOB dans un fichier.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WriteBlobToFile(
  _In_       HBLOB hBlob,
  _In_ const char  *pFileName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB.

</dd> <dt>

*pFileName* \[ dans\]
</dt> <dd>

Pointeur vers le nom du fichier dans lequel l’objet BLOB est enregistré.

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



 

 




