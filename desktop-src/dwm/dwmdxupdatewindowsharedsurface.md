---
description: Notifie le DWM d’une mise à jour entrante à une surface partagée de fenêtre.
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface fonction)
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 7649e96fb3a16458b518d0fc2c6dd09725a4b0ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528131"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>DwmDxUpdateWindowSharedSurface fonction)

Notifie le DWM d’une mise à jour entrante à une surface partagée de fenêtre.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>Paramètres

`hwnd`

[**HWND**](/windows/desktop/winprog/windows-data-types) spécifiant la fenêtre en cours de mise à jour.

`uiUpdateId`

ID de mise à jour extrait de [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md).

`dwFlags`

Réservé.

`hmonitorAssociation`

Réservé.

`prc`

Rectangle de la fenêtre en cours de mise à jour, dans l’espace de coordonnées de la fenêtre. Un rectangle NULL indique qu’aucune région n’a été mise à jour.

## <a name="return-value"></a>Valeur retournée

**S \_ OK** en cas de réussite, sinon un HRESULT en échec **.**

## <a name="remarks"></a>Notes

Cette API est destinée à l’implémentation d’un pilote ou d’un Runtime Graphics. Une application ne peut pas appeler cette méthode. Cette documentation n’est valide que pour Windows 7, et il n’est pas garanti que cette API existe et qu’elle se comporte de manière similaire sur d’autres versions de Windows. Cette fonction n’est pas présente dans un en-tête ou une bibliothèque de liens statiques, et elle se trouve à l’ordinal 101 dans dwmapi.dll.

Cette méthode ne doit être appelée qu’une fois que [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) a retourné la valeur **\_ OK** et qu’elle doit être appelée dans ce scénario, que la surface soit mise à jour ou non.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | Applications de \[ Bureau Windows 7 uniquement\] |
| Serveur minimal pris en charge | Aucun pris en charge |
| Fin de la prise en charge des clients | Windows 7 |
| En-tête | N/A |
| DLL | Dwmapi.dll |
