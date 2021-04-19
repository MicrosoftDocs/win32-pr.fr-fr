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
ms.openlocfilehash: 59b6b38cf7e78755c7d5c481a22a0a8b3854c8a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530284"
---
# <a name="krshowkeymgr-function"></a>KRShowKeyMgr fonction)

\[Cette fonction est incluse uniquement dans Windows XP. Il n’est pas inclus dans les autres versions de Windows et ne devrait pas être inclus dans les futures versions de Windows.\]

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

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Keymgr.dll</dt> </dl> |



 

 
