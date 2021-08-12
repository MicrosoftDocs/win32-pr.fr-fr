---
description: Récupère la surface partagée DirectX qui stocke une fenêtre donnée. Cette surface peut être écrite pour mettre à jour le contenu de la fenêtre.
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface fonction)
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 47f8c75ee55521c0f1da4151f5161cf44a63dc51aab5658edbca288cb8edce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280129"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>DwmDxGetWindowSharedSurface fonction)

Récupère la surface partagée DirectX qui stocke une fenêtre donnée. Cette surface peut être écrite pour mettre à jour le contenu de la fenêtre.

## <a name="syntax"></a>Syntaxe

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a>Paramètres

`hwnd`

[**HWND**](/windows/desktop/winprog/windows-data-types) spécifiant la fenêtre à mettre à jour.

`luidAdapter`

[**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) de l’adaptateur dans lequel la surface doit être localisée.

`hmonitorAssociation`

Réservé.

`dwFlags`

Ce paramètre peut avoir l’une des valeurs suivantes, ou une combinaison au niveau du bit ou une combinaison de plusieurs valeurs, le cas échéant.

| Valeur | Signification |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_ Attente de l' \_ indicateur \_ de redirection**</dt> <dt>0</dt> </dl> | Provoque le blocage de la fonction jusqu’à ce qu’une synchronisation verticale (VSync) soit passée depuis la dernière fois que la fonction a été appelée avec succès. |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_ \_ \_ Prise en charge des indicateurs \_ de redirection présents \_ dans \_ GDI \_ surface**</dt> <dt>0x10</dt> </dl> | Indique que l’application appelante peut présenter à une surface partagée GDI. |

`pfmtWindow`

En entrée, le format souhaité de la surface. Lors de la sortie, le format réel de la surface retournée.

`phDxSurface`

À la sortie, handle partagé vers la surface.

`puiUpdateId`

À la sortie, ID de la mise à jour.

## <a name="return-value"></a>Valeur renvoyée

Cette fonction peut retourner l’une de ces valeurs.

| Code de retour | Description |
|-|-|
| **\_OK** | L’appel a réussi, et vous devez mettre à jour la surface, en veillant à transmettre l’ID de mise à jour à [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (dans le membre **PresentHistoryToken** de la structure de **\_ rendu D3DKMT** lorsque la mise à jour est envoyée, puis [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) doit être appelé avec le même ID de mise à jour. Notez que **DwmDxUpdateWindowSharedSurface** doit être appelé, que la surface ait ou non été réellement mise à jour. |
| **\_ \_ \_ la surface de redirection GDI du DWM S \_** | L’appel a réussi, et vous devez mettre à jour la surface en appelant [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)et en définissant le **modèle** du membre **PRESENTHISTORYTOKEN** sur **D3DKMT \_ PM \_ Redirigé \_**, et en fournissant l’ID de mise à jour dans le membre **BLT** de l’Union. Cette valeur est retournée uniquement si la **\_ \_ \_ prise en charge de l’indicateur de redirection DWM \_ présente \_ à la \_ \_ surface GDI** a été spécifiée dans *dwFlags*. |
| **\_adaptateur DWM \_ E \_ \_ introuvable** | La valeur de *luidAdapter* n’est pas valide. |
| **DWM \_ E \_ COMPOSITIONDISABLED** | DWM n’est pas activé actuellement, et l’application doit présenter une autre méthode. |

## <a name="remarks"></a>Notes

Cette API est destinée à l’implémentation d’un pilote ou d’un Runtime Graphics. Une application ne peut pas appeler cette méthode. cette documentation n’est valide que pour Windows 7, et il n’est pas garanti que cette API existe et qu’elle se comporte de manière similaire sur les autres versions de Windows. Cette fonction n’est pas présente dans un en-tête ou une bibliothèque de liens statiques, et elle se trouve à l’ordinal 100 dans dwmapi.dll.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| Client minimal pris en charge | applications de \[ bureau Windows 7 uniquement\] |
| Serveur minimal pris en charge | Aucun pris en charge |
| Fin de la prise en charge des clients | Windows 7 |
| En-tête | N/A |
| DLL | Dwmapi.dll |
