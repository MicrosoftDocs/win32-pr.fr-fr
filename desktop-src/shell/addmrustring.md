---
description: Ajoute une chaîne en haut de la liste des derniers fichiers utilisés.
title: AddMRUStringW fonction)
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
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841190"
---
# <a name="addmrustringw-function"></a>AddMRUStringW fonction)

\[Cette fonction est disponible via Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. \]

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

## <a name="return-value"></a>Valeur renvoyée

Type : **int**

Retourne une valeur non négative en cas de réussite,-1 dans le cas contraire.

## <a name="remarks"></a>Notes

Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque. Il est accessible par le biais de [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 401 pour **AddMRUStringW**.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **AddMRUStringW** (Unicode)<br/>                                                                         |



 

