---
description: La fonction RegOpenBlobKey récupère un objet BLOB stocké à la clé de Registre donnée.
ms.assetid: f6b16c07-c705-47f1-a21c-6155368551c7
title: RegOpenBlobKey, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RegOpenBlobKey
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 24d788c8c4b69525d6c0be374845b44f804982bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021043"
---
# <a name="regopenblobkey-function"></a>RegOpenBlobKey fonction)

La fonction **RegOpenBlobKey** récupère un objet BLOB stocké à la clé de Registre donnée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD RegOpenBlobKey(
  _In_        HKEY  hkey,
  _In_  const char  *szBlobName,
  _Out_       HBLOB *phBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HKEY* \[ dans\]
</dt> <dd>

Handle de la clé de Registre qui contient l’objet BLOB.

</dd> <dt>

*szBlobName* \[ dans\]
</dt> <dd>

Nom qui identifie l’objet BLOB donné dans le registre.

</dd> <dt>

*phBlob* \[ à\]
</dt> <dd>

Pointeur vers l’objet BLOB qui est récupéré.

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

[RegCreateBlobKey](regcreateblobkey.md)
</dt> </dl>

 

 




