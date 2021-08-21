---
description: La fonction LoadMACAddresses est appelée par l’analyse pour remplir une liste d’adresses MAC avec les adresses tirées d’une variable de chaîne de configuration HTML.
ms.assetid: cb7d2812-e234-4858-8b25-f8fc72aeee79
title: LoadMACAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadMACAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2de609ef0a1e820785ee7d62cbbe1e6af32c633aa29b133974f6f5f6f2a649b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119742719"
---
# <a name="loadmacaddresses-function"></a>LoadMACAddresses fonction)

La fonction **LoadMACAddresses** est appelée par l’analyse pour remplir une liste d’adresses Mac avec les adresses tirées d’une variable de chaîne de configuration html.

## <a name="syntax"></a>Syntaxe


```C++
BOOL LoadMACAddresses(
  _In_  const char   *pConfig,
  _In_  const char   *pVarName,
  _Out_       LPBYTE *ppAddresses,
  _Out_       DWORD  *pNumAddresses
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

Pointeur vers un pointeur vers un tableau d’adresses. Si la variable spécifiée dans *pVarName* est trouvée et a une longueur différente de zéro, la fonction alloue suffisamment d’espace (à l’aide de **HeapAllocMemory**) et stocke toutes les adresses Mac sous la forme d’un tableau.

</dd> <dt>

*pNumAddresses* \[ à\]
</dt> <dd>

Pointeur vers la variable **DWORD** qui est définie sur le nombre d’adresses Mac prises à partir de la chaîne de configuration.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, (le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro qui représentait des adresses MAC), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




