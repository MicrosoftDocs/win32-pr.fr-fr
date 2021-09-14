---
description: La fonction DestroyBlob libère toute la mémoire associée à l’objet BLOB, puis détruit l’objet BLOB.
ms.assetid: 46cde0b7-1b59-426e-b19b-3c73af3d461a
title: DestroyBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DestroyBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: e90630981c16f38d601d4e06d04f9326174ef721
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127229703"
---
# <a name="destroyblob-function"></a>DestroyBlob fonction)

La fonction **DestroyBlob** libère toute la mémoire associée à l’objet BLOB, puis détruit l’objet BLOB.

## <a name="syntax"></a>Syntaxe


```C++
DWORD DestroyBlob(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers l’objet BLOB qui est détruit.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.

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

[CreateBlob](createblob.md)
</dt> </dl>

 

 




