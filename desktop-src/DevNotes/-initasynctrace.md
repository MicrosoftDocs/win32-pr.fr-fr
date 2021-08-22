---
description: Initialise la trace.
ms.assetid: d2708e29-920d-4b13-8917-a6f2065ba58c
title: InitAsyncTrace fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InitAsyncTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: d64fcf9f787587165c12e675d79cfca641b0ab5086a5cce6b13029da46def974
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956298"
---
# <a name="initasynctrace-function"></a>InitAsyncTrace fonction)

Initialise la trace.

## <a name="syntax"></a>Syntaxe


```C++
BOOL InitAsyncTrace(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Cette fonction retourne la **valeur true** si la fonction est réussie ; Sinon, elle retourne **false**.

## <a name="remarks"></a>Remarques

Exstrace.dll est un composant facultatif qui est installé avec le protocole SMTP (Simple Mail Transfer Protocol) et le protocole NNTP (Network News Transfer Protocol).

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Exstrace.dll</dt> </dl> |



 

 
