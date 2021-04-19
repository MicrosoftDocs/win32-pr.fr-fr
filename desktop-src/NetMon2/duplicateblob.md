---
description: La fonction DuplicateBlob copie un objet BLOB spécifique.
ms.assetid: d2478f53-328c-4799-890c-7849ce1f22e9
title: DuplicateBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DuplicateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: df0fc00f0bd51e89da432e6f3b0143ce6092cedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540884"
---
# <a name="duplicateblob-function"></a>DuplicateBlob fonction)

La fonction **DuplicateBlob** copie un objet BLOB spécifique.

## <a name="syntax"></a>Syntaxe


```C++
DWORD DuplicateBlob(
  _In_  HBLOB hSrcBlob,
  _Out_ HBLOB *hBlobThatWillBeCreated
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSrcBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB copié.

</dd> <dt>

*hBlobThatWillBeCreated* \[ à\]
</dt> <dd>

Handle vers l’objet BLOB dupliqué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui décrit l’erreur.

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

[CreateBlob](createblob.md)
</dt> <dt>

[DestroyBlob](destroyblob.md)
</dt> </dl>

 

 




