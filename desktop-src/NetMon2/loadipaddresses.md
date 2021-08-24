---
description: La fonction LoadIPAddresses est appelée par l’analyse pour remplir une liste d’adresses IP avec les adresses tirées d’une variable de chaîne de configuration HTML.
ms.assetid: d0b5d686-5a98-4d61-aa28-24ea71fcb06b
title: LoadIPAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2f56517fd0caf4762be2848ac9a6f3094ed5e3194b2eb84123bf2fcc2bf67bcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742669"
---
# <a name="loadipaddresses-function"></a>LoadIPAddresses fonction)

La fonction **LoadIPAddresses** est appelée par l’analyse pour remplir une liste d’adresses IP avec les adresses tirées d’une variable de chaîne de configuration html.

## <a name="syntax"></a>Syntaxe


```C++
BOOL LoadIPAddresses(
  _In_  const char  *pConfig,
  _In_  const char  *pVarName,
  _Out_       DWORD **ppAddresses,
  _Out_       DWORD *pNumAddresses
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pConfig* \[ dans\]
</dt> <dd>

Pointeur vers la chaîne de configuration HTML transmise à l’analyse par la méthode [Imonitor ::D oconfigure](imonitor-doconfigure.md) .

</dd> <dt>

*pVarName* \[ dans\]
</dt> <dd>

Pointeur vers le nom de la variable dans la chaîne de configuration.

</dd> <dt>

*ppAddresses* \[ à\]
</dt> <dd>

Pointeur vers un pointeur vers un tableau d’adresses. Si la variable spécifiée dans *pVarName* est trouvée et a une longueur différente de zéro, la fonction alloue suffisamment d’espace et stocke toutes les adresses IP sous la forme d’un tableau.

</dd> <dt>

*pNumAddresses* \[ à\]
</dt> <dd>

Pointeur vers la variable **DWORD** qui est définie sur le nombre d’adresses IP prises à partir de la chaîne de configuration.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro qui représentait des adresses IP), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

Les adresses IP doivent être au format x. x. x (par exemple, 127.0.0.1).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




