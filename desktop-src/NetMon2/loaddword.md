---
description: La fonction LoadDWORD est appelée par l’analyse pour définir une variable DWORD avec une valeur extraite d’une variable de chaîne de configuration HTML.
ms.assetid: 18a7beba-01f4-4f92-99bf-067f79f25db0
title: LoadDWORD, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadDWORD
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8fa0477122548dad30911948a3581d269b22d8d6eb866273f32aa40a9b427545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778759"
---
# <a name="loaddword-function"></a>LoadDWORD fonction)

La fonction **LoadDWORD** est appelée par l’analyse pour définir une variable **DWORD** avec une valeur extraite d’une variable de chaîne de configuration html.

## <a name="syntax"></a>Syntaxe


```C++
BOOL LoadDWORD(
  _In_ const char  *pConfig,
  _In_ const char  *pVarName,
  _In_       DWORD *pValue
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

*pValue* \[ dans\]
</dt> <dd>

Pointeur vers la variable **DWORD** qui est définie sur la valeur de la variable de chaîne de configuration.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (si le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro), la valeur **DWORD** est insérée et la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




