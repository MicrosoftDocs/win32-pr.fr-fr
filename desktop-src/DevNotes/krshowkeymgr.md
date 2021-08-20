---
description: Affiche la boîte de dialogue Gestionnaire de clés dans l’interface utilisateur.
ms.assetid: 65c2763f-42d5-4534-94f7-e753f6486014
title: KRShowKeyMgr fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KRShowKeyMgr
api_type:
- DllExport
api_location:
- Keymgr.dll
ms.openlocfilehash: 58b62b036b1aba7916c2c08cdbdb137e136c85c694dc11210cadcd7fe2a92d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004131"
---
# <a name="krshowkeymgr-function"></a>KRShowKeyMgr fonction)

\[cette fonction est incluse uniquement dans Windows XP. elle n’est pas incluse dans les autres versions de Windows, pas plus qu’elle ne devrait être incluse dans les futures versions de Windows.\]

Affiche la boîte de dialogue Gestionnaire de clés dans l’interface utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
void KRShowKeyMgr(
   HWND      hwParent,
   HINSTANCE hInstance,
   LPWSTR    pszCmdLine,
   int       CmdShow
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hwParent* 
</dt> <dd>

Handle de la fenêtre parente de la boîte de dialogue. Ce paramètre peut être **NULL**.

</dd> <dt>

*hInstance* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*pszCmdLine* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> <dt>

*CmdShow* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit avoir la valeur **null**.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
