---
description: Ajoute une chaîne en haut de la liste des derniers fichiers utilisés.
title: AddMRUStringW, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: 4ac72c44b670466f10cd708b81b1a84f93a349afcb0d81473ed5e6578c20617a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117861591"
---
# <a name="addmrustringw-function"></a>AddMRUStringW, fonction

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. \]

Ajoute une chaîne en haut de la liste des derniers fichiers utilisés.

## <a name="syntax"></a>Syntaxe


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMRU* \[ dans\]
</dt> <dd>

Type : **handle**

Handle de la liste MRU.

</dd> <dt>

*szString* \[ dans\]
</dt> <dd>

Type : **LPCTSTR**

Pointeur vers les données. Il peut s’agir d’une chaîne ou, si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , données binaires. Dans le cas de données binaires, la première **valeur DWORD** indique sa taille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Retourne une valeur non négative en cas de réussite,-1 dans le cas contraire.

## <a name="remarks"></a>Remarques

Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque. Il est accessible par le biais de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 401 pour **AddMRUStringW**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

