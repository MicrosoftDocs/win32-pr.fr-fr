---
description: NtGdiDdCreateSurface fonction-attache une surface à une autre surface.
ms.assetid: 4fd757c7-9e32-4737-b666-3226f6cf29fa
title: NtGdiDdCreateSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: bf8e13cff80ddea4e102c045c174565e7e835274
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085777"
---
# <a name="ntgdiddcreatesurface-function"></a>NtGdiDdCreateSurface fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Attache une surface à une autre surface.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdCreateSurface(
  _In_    HANDLE               hDirectDraw,
  _In_    HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Out_   HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle vers la [**structure \_ \_ globale d’JJ DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) représentant le pilote.

</dd> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle précédent à la même surface. Utilisé si la surface est recréée après un basculement de mode.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Pointeur vers la structure [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) décrivant la surface ou la mémoire tampon que le pilote doit créer.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Pointeur vers la [**structure \_ \_ globale de la surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) qui contient des données de surface partagées globalement avec plusieurs surfaces.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Pointeur désignant une liste de structures [**\_ \_ locales de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) décrivant les objets surface créés par le pilote.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ plus grande surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) qui contient des données de surface locales supplémentaires.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Pointeur vers une [**structure \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) qui contient les informations requises pour créer une surface.

</dd> <dt>

*puhSurface* \[ à\]
</dt> <dd>

Est utilisé par l’API DirectDraw et ne doit pas être renseigné par le pilote.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

**NtGdiDdCreateSurface** retourne l’un des codes de rappel suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_pilote DDHAL \_ géré**</dt> </dl>    | Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération. Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction. Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.<br/>                                                                                 |
| <dl> <dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt> </dl> | Le pilote n’a pas de commentaire sur l’opération demandée. Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur. Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.<br/> |



 

## <a name="remarks"></a>Notes 

Il est recommandé que votre application appelle [IDirectDraw7 :: CreateSurface](/windows/win32/api/ddraw/nf-ddraw-idirectdraw7-createsurface) au lieu d’utiliser cette fonction.

Lors de la création d’une chaîne de surfaces attachées, telle qu’une chaîne de permutation ou une chaîne ou des mipmaps, [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) doit être appelé pour chaque surface en premier. Appelez ensuite [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) pour les attacher. Enfin, appelez **NtGdiDdCreateSurface** pour la première surface de la chaîne uniquement. Dans ce cas, *hSurface* serait le handle retourné par **NtGdiDdCreateSurfaceObject** pour la première surface de la chaîne.

**NtGdiDdCreateSurface** doit être appelé uniquement pour créer des surfaces dans la mémoire vidéo locale et non locale. Il ne doit jamais être appelé pour créer des surfaces de mémoire système. Pour créer des surfaces de mémoire système, utilisez [**NtGdiDdCreateSurfaceObject**](-dxgkernel-ntgdiddcreatesurfaceobject.md) à la place.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Ntgdi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Prise en charge des clients de bas niveau](-dxgkernel-low-level-client-support.md)
</dt> </dl>

 

 
