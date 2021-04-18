---
description: La fonction LoadTCHAR est appelée par les analyses pour définir une variable de chaîne sur une chaîne tirée d’une chaîne de configuration HTML.
ms.assetid: 515a1053-d575-4b7c-92a7-4a8039f1b2ac
title: LoadTCHAR, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadTCHAR
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 25437ae5ad6c23209540194f8c658e275c7041b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106543091"
---
# <a name="loadtchar-function"></a>LoadTCHAR fonction)

La fonction **LoadTCHAR** est appelée par les analyses pour définir une variable de chaîne sur une chaîne tirée d’une chaîne de configuration html.

## <a name="syntax"></a>Syntaxe


```C++
BOOL LoadTCHAR(
  _In_  const char *pConfig,
  _In_  const char *pVarName,
  _Out_       char **ppszString
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

*ppszString* \[ à\]
</dt> <dd>

Pointeur vers un pointeur de chaîne. Si le nom de la variable demandée est trouvé, la chaîne est allouée et assignée à ce pointeur. L’utilisateur est responsable de libérer la mémoire associée à la chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit (si le nom de la variable a été trouvé et avait une chaîne de longueur différente de zéro), la valeur de retour est **true**.

Si la fonction échoue, la valeur de retour est **false**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Bibliothèque<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




