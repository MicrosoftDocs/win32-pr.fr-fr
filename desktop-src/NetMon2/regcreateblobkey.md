---
description: La fonction RegCreateBlobKey stocke un objet BLOB à la clé de Registre donnée.
ms.assetid: 14f3763e-aa04-4d51-b388-81ebf0d3952c
title: RegCreateBlobKey, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegCreateBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 3267fd0ba5e6fe56b99b5d465f69718fe5509a7ead58acf1d8dafb642397af5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119889649"
---
# <a name="regcreateblobkey-function"></a>RegCreateBlobKey fonction)

La fonction **RegCreateBlobKey** stocke un objet blob à la clé de Registre donnée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RegCreateBlobKey(
  _Out_       HKEY  hkey,
  _In_  const char  *szBlobName,
  _In_        HBLOB hBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HKEY* \[ à\]
</dt> <dd>

Handle de la clé de Registre dans laquelle l’objet BLOB sera stocké.

</dd> <dt>

*szBlobName* \[ dans\]
</dt> <dd>

Nom (défini par l’application) qui représente l’objet BLOB dans le registre.

</dd> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB enregistré.

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

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




