---
description: La fonction MergeBlob copie toutes les entrées de l’objet BLOB source dans un objet BLOB de destination.
ms.assetid: 7521ce0c-fd02-4002-bdae-0d74a2e4a646
title: MergeBlob, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MergeBlob
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5c0ce93235a0c46286b9bfbef0773a5584f3db774aa52991b4e0eaa9dd38352f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119677189"
---
# <a name="mergeblob-function"></a>MergeBlob fonction)

La fonction **MergeBlob** copie toutes les entrées de l’objet BLOB source dans un objet blob de destination.

## <a name="syntax"></a>Syntaxe


```C++
DWORD MergeBlob(
  _Inout_ HBLOB hDstBlob,
  _In_    HBLOB hSrcBlob
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDstBlob* \[ in, out\]
</dt> <dd>

Handle vers l’objet BLOB de destination. En entrée, cet objet BLOB contient ses informations d’origine. En sortie, cet objet BLOB contient ses informations d’origine, ainsi que toutes les informations de l’objet BLOB source.

</dd> <dt>

*hSrcBlob* \[ dans\]
</dt> <dd>

Handle de l’objet BLOB source.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="remarks"></a>Remarques

Les entrées communes aux fichiers source et de destination seront remplacées par les données de l’objet BLOB source.

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




