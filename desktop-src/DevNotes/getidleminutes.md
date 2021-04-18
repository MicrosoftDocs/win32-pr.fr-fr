---
description: Obtient la durée, en minutes, depuis la dernière activité de l’utilisateur.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: GetIdleMinutes fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533016"
---
# <a name="getidleminutes-function"></a>GetIdleMinutes fonction)

\[Cette fonction n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir. Utilisez plutôt la fonction **GetLastInputInfo** .\]

Obtient la durée, en minutes, depuis la dernière activité de l’utilisateur.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*dwReserved* 
</dt> <dd>

Ce paramètre doit avoir la valeur zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de minutes depuis la dernière activité de l’utilisateur.

## <a name="remarks"></a>Notes

Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) . Cette fonction n’est pas exportée par nom ; Spécifiez l’ordinal 8 lors de l’appel de **GetProcAddress**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Msidle.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**GetLastInputInfo**](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
