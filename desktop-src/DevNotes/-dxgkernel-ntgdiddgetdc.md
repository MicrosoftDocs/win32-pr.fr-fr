---
description: Crée un contexte de périphérique (DC) pour la surface spécifiée.
ms.assetid: c2eaaed6-db19-4dab-ac12-6b4e7eeb58e4
title: NtGdiDdGetDC, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDC
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4f930334f0712107d5651a22b35d6917c7977011
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110670"
---
# <a name="ntgdiddgetdc-function"></a>NtGdiDdGetDC fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Crée un contexte de périphérique (DC) pour la surface spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
HDC APIENTRY NtGdiDdGetDC(
  _In_ HANDLE       hSurface,
  _In_ PALETTEENTRY *puColorTable
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle vers une surface DirectDraw en mode noyau précédemment retournée par [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md) ou [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md).

</dd> <dt>

*puColorTable* \[ dans\]
</dt> <dd>

Pointeur vers une table de couleurs de remplacement pour le contrôleur de périphérique retourné.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne un **HDC** valide ; Sinon, elle retourne la **valeur null**.

## <a name="remarks"></a>Notes

Un seul contrôleur de périphérique est autorisé par surface à un moment donné. Les appels suivants à **NtGdiDdGetDC** échouent tant que le DC précédent n’est pas libéré.

Il est recommandé aux applications d’appeler [IDirectDrawSurface7 :: GetDC](/windows/win32/api/ddraw/nf-ddraw-idirectdrawsurface7-getdc) à la place, ce qui fournit les mêmes fonctionnalités d’une manière indépendante du système d’exploitation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des clients de bas niveau](-dxgkernel-low-level-client-support.md)
</dt> <dt>

[**DdGetDC**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddgetdc)
</dt> </dl>

 

 
