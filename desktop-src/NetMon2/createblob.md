---
description: La fonction CreateBlob crée un objet BLOB vide.
ms.assetid: fa31855b-af85-4ab5-b434-e54111731d8f
title: CreateBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 1c5a74a2008993aba40b97e6fce779398132dbeae0428d4c7ae2054640a4159a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744709"
---
# <a name="createblob-function"></a>CreateBlob fonction)

La fonction **CreateBlob** crée un objet BLOB vide.

## <a name="syntax"></a>Syntaxe


```C++
DWORD CreateBlob(
  _Out_ HBLOB *phBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phBlob* \[ à\]
</dt> <dd>

Pointeur vers la variable où le pointeur vers le nouvel objet BLOB est retourné.

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

[DestroyBlob](destroyblob.md)
</dt> </dl>

 

 




