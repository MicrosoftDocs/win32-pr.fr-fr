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
ms.openlocfilehash: fc46b38919b37dc004c1065b0cc8d5f80e65984c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021047"
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

[RegOpenBlobKey](regopenblobkey.md)
</dt> </dl>

 

 




