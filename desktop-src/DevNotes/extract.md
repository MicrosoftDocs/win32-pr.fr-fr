---
description: La fonction Extract extrait les fichiers d’un fichier CAB.
ms.assetid: c6a79d81-7adf-4b8e-a1ef-fec868f7fdbf
title: Extraire une fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Extract
api_type:
- DllExport
api_location:
- Cabinet.dll
ms.openlocfilehash: cbcb53aae008423ac56bb489d43f6fd78016a9b1f716be21390a6dfc1de00404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162063"
---
# <a name="extract-function"></a>Extraire une fonction

\[Cette fonction n’étant plus prise en charge, son comportement ne peut pas être garanti.\]

La fonction **extract** extrait les fichiers d’un fichier CAB.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT Extract(
   PSESSION ps,
   LPCSTR   lpCabName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ps* 
</dt> <dd>

Pointeur vers une structure de [**session**](session.md) qui contient des informations sur la session active.

</dd> <dt>

*lpCabName* 
</dt> <dd>

Pointeur vers le nom du fichier cab à partir duquel les fichiers doivent être extraits.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction est réussie, elle retourne **S \_ OK**; sinon, elle retourne un code d’erreur.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cabinet.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DeleteExtractedFiles**](deleteextractedfiles.md)
</dt> <dt>

[**ERF**](/windows/win32/api/fdi_fci_types/ns-fdi_fci_types-erf)
</dt> <dt>

[**SESSION**](session.md)
</dt> </dl>

 

 
