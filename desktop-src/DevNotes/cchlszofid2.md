---
description: Décode et stocke une chaîne.
ms.assetid: 6ababd6e-57b7-49eb-98c9-a4bcb558a377
title: CchLszOfId2 fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CchLszOfId2
api_type:
- DllExport
api_location:
- Msjint40.dll
ms.openlocfilehash: 0377b8507507b40c5b17c3d9bb6861e5077f8c7bb763b51c66289ab1819f9cc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119815469"
---
# <a name="cchlszofid2-function"></a>CchLszOfId2 fonction)

Décode et stocke une chaîne.

## <a name="syntax"></a>Syntaxe


```C++
UINT CchLszOfId2(
   UINT  id,
   WCHAR *lsz,
   UINT  cbmax
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*id* 
</dt> <dd>

Identificateur de la chaîne dans le fichier de ressources à décoder et à stocker. La validité de la chaîne n’est pas vérifiée.

</dd> <dt>

*lsz* 
</dt> <dd>

Pointeur vers une mémoire tampon avec une longueur de *Cbmax*. Les chaînes dont la longueur est supérieure à *Cbmax* sont tronquées.

</dd> <dt>

*cbmax* 
</dt> <dd>

Longueur maximale de la chaîne à stocker dans le paramètre *LSZ* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la chaîne décodée.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msjint40.dll</dt> </dl> |



 

 
