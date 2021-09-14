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
ms.openlocfilehash: 6ea28f5bb6f337b20858baa544c890d5f71bf0c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127194663"
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

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est NMERR \_ Success.

Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.

## <a name="remarks"></a>Notes

Les entrées communes aux fichiers source et de destination seront remplacées par les données de l’objet BLOB source.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Npptools. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Npptools.dll</dt> </dl> |



 

 




