---
description: La fonction LoadIPXAddresses est appelée par l’analyse pour remplir une liste d’adresses IPX tirée d’une variable de chaîne de configuration HTML.
ms.assetid: d8ffd00b-2741-49e8-a90d-d41e56ee7101
title: LoadIPXAddresses, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadIPXAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f6e25e7afa80c3a3c4113723937c623baacd2a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210046"
---
# <a name="loadipxaddresses-function"></a>LoadIPXAddresses fonction)

La fonction **LoadIPXAddresses** est appelée par l’analyse pour remplir une liste d’adresses IPX tirée d’une variable de chaîne de configuration html.

## <a name="syntax"></a>Syntaxe


```C++
BOOL LoadIPXAddresses(
  _In_  const char        *pConfig,
  _In_  const char        *pVarName,
  _Out_       IPX_ADDRESS **ppAddresses,
  _Out_       DWORD       *pNumAddresses
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

Pointeur vers un pointeur vers un tableau d’adresses. Si la variable spécifiée dans *pVarName* est trouvée et a une longueur différente de zéro, un espace suffisant est alloué (à l’aide de **HeapAllocMemory**), et toutes les adresses IPX sont stockées sous la forme d’un tableau.

</dd> <dt>

*pNumAddresses* \[ à\]
</dt> <dd>

Pointeur vers la variable **DWORD** qui est définie sur le nombre d’adresses IPX prises à partir de la chaîne de configuration.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro qui représente des adresses IPX), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




