---
description: La fonction IsRemoteNPP indique si l’objet BLOB donné spécifie un NPP distant.
ms.assetid: 66ee0a9a-3199-479f-baec-da6ae6b46c65
title: IsRemoteNPP, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsRemoteNPP
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: ec91b5e2d4602df6aa264a27adf46e47cec24683fc65dace358649eeba76643a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890329"
---
# <a name="isremotenpp-function"></a>IsRemoteNPP fonction)

La fonction **IsRemoteNPP** indique si l’objet BLOB donné spécifie un NPP distant.

## <a name="syntax"></a>Syntaxe


```C++
BOOL IsRemoteNPP(
  _In_ HBLOB hBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hBlob* \[ dans\]
</dt> <dd>

Handle vers un objet BLOB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est **true**.

## <a name="remarks"></a>Remarques

Utilisez cette fonction pour tester si une catégorie distante existe.

Assurez-vous que les noms des ordinateurs locaux et distants sont différents.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




