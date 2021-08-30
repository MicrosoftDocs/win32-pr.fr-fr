---
description: Énumère le contenu de la liste des derniers fichiers utilisés. Récupère éventuellement un élément de l’énumération.
title: EnumMRUListW, fonction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumMRUListW
- EnumMRUListW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: 630e5f27-96bf-4e88-b01a-127b301cc051
ms.openlocfilehash: 668b92ad8e89c4b3a4082142c7eb8cdc722b8b2f4ce01827319c0480e0d2e997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942999"
---
# <a name="enummrulistw-function"></a>EnumMRUListW, fonction

\[cette fonction est disponible par le biais de Windows XP avec Service Pack 2 (SP2) et Windows Server 2003. Il peut être modifié ou non disponible dans les versions ultérieures de Windows. \]

Énumère le contenu de la liste des derniers fichiers utilisés. Récupère éventuellement un élément de l’énumération.

## <a name="syntax"></a>Syntaxe


```C++
int EnumMRUListW(
  _In_  HANDLE hMRU,
  _In_  int    nItem,
  _Out_ void   *lpData,
  _In_  UINT   uLen
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMRU* \[ dans\]
</dt> <dd>

Type : **handle**

Handle de la liste MRU, obtenu lors de la création de la liste.

</dd> <dt>

*nItem* \[ dans\]
</dt> <dd>

Type : **int**

Élément à retourner. Si cette valeur est inférieure à 0, la fonction retourne le nombre d’éléments dans la liste MRU.

</dd> <dt>

*lpData* \[ à\]
</dt> <dd>

Type : **void \***

Pointeur vers une mémoire tampon qui reçoit l’élément demandé dans *nItem*. Si *nItem* est inférieur à 0, le contenu de cette mémoire tampon n’est pas modifié.

</dd> <dt>

*uLen* \[ dans\]
</dt> <dd>

Type : **uint**

Taille de la mémoire tampon, y compris le caractère null de fin. Si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , il s’agit de la taille en octets. Dans le cas contraire, il s’agit de la taille en caractères.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **int**

Retourne l’une des valeurs suivantes.

-   Retourne le nombre d’éléments dans l’énumération, si *nItem* est inférieur à 0.
-   Retourne-1 si une erreur s’est produite.
-   Sinon, retourne la taille de la chaîne retournée dans *lpData*, y compris le caractère null de fin. Si la liste MRU a été créée avec l’indicateur **\_ binaire MRU** , il s’agit de la taille en octets. Dans le cas contraire, il s’agit de la taille en caractères.

## <a name="remarks"></a>Remarques

Cette fonction n’est pas incluse dans un en-tête public ou une bibliothèque. Il est accessible par le biais de [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) ou extrait de comctl32.dll par son ordinal, qui est 403 pour **EnumMRUListW**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (version 5,0 ou ultérieure)</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **EnumMRUListW** (Unicode)<br/>                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CreateMRUListW**](createmrulist.md)
</dt> <dt>

[**MRUINFO**](mruinfo.md)
</dt> </dl>

 

 
