---
description: Envoie une chaîne Unicode au débogueur pour l’affichage.
ms.assetid: 26cf4750-8ca1-4a9a-8378-d65ed288b358
title: OutputDebugStringWrapW, fonction (Shlwapip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OutputDebugStringWrapW
api_type:
- DllExport
api_location:
- Shlwapi.dll
ms.openlocfilehash: cce8754b01ddf156951964b7189b4a7189759c52cdcd08e08091ca62b2e950bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858788"
---
# <a name="outputdebugstringwrapw-function"></a>OutputDebugStringWrapW fonction)

\[cette fonction peut être utilisée dans Windows XP. Elle n’est peut-être pas disponible dans les versions ultérieures. Utilisez [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) à la place.\]

Envoie une chaîne Unicode au débogueur pour l’affichage.

> [!Note]  
> **OutputDebugStringWrapW** est un wrapper pour la fonction **OutputDebugStringW** . Pour plus d’informations sur les remarques d’utilisation, consultez la page [**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) .

 

## <a name="syntax"></a>Syntaxe


```C++
void OutputDebugStringWrapW(
  _In_ LPCWSTR lpOutputString
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lpOutputString* \[ dans\]
</dt> <dd>

Type : **LPCWSTR**

Pointeur vers la chaîne Unicode terminée par le caractère null à afficher.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

**OutputDebugStringWrapW** offre la possibilité d’utiliser des chaînes Unicode dans les systèmes d’exploitation antérieurs à Windows XP. La méthode recommandée consiste à utiliser [**OutputDebugStringW**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa) conjointement avec la couche Microsoft pour Unicode (MSLU).

**OutputDebugStringWrapW** doit être appelé directement à partir de Shlwapi.dll, à l’aide de l’ordinal 115.

Si l’application n’a pas de débogueur, le débogueur système affiche la chaîne. Si l’application n’a pas de débogueur et que le débogueur système n’est pas actif, **OutputDebugStringWrapW** ne fait rien.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Shlwapip. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shlwapi.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**OutputDebugString**](/windows/win32/api/debugapi/nf-debugapi-outputdebugstringa)
</dt> </dl>

 

 
