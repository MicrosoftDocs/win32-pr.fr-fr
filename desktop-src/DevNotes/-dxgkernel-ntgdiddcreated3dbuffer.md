---
description: Utilisé pour créer une commande de niveau pilote ou une mémoire tampon de vertex de la description spécifiée.
ms.assetid: c65403a1-5686-4c7d-80a4-6e49417c11eb
title: NtGdiDdCreateD3DBuffer, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateD3DBuffer
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 2d402a70822fba094d22c82b8767ee3298b86374
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950437"
---
# <a name="ntgdiddcreated3dbuffer-function"></a>NtGdiDdCreateD3DBuffer fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Utilisé pour créer une commande de niveau pilote ou une mémoire tampon de vertex de la description spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdCreateD3DBuffer(
  _In_    HANDLE               hDirectDraw,
  _Inout_ HANDLE               *hSurface,
  _Inout_ DDSURFACEDESC        *puSurfaceDescription,
  _Inout_ DD_SURFACE_GLOBAL    *puSurfaceGlobalData,
  _Inout_ DD_SURFACE_LOCAL     *puSurfaceLocalData,
  _Inout_ DD_SURFACE_MORE      *puSurfaceMoreData,
  _Inout_ DD_CREATESURFACEDATA *puCreateSurfaceData,
  _Inout_ HANDLE               *puhSurface
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle vers la [**structure \_ \_ globale d’JJ DIRECTDRAW**](/windows/win32/api/ddrawint/ns-ddrawint-dd_directdraw_global) représentant le pilote.

</dd> <dt>

*hSurface* \[ in, out\]
</dt> <dd>

Pointeur vers un tableau de handles de surface. L’appelant peut définir ces handles aux valeurs de handle précédentes si les surfaces sont recréées après un changement de mode. Ce processus est appelé « restauration » dans la documentation de DirectDraw.

</dd> <dt>

*puSurfaceDescription* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**DDSURFACEDESC**](/previous-versions/windows/hardware/drivers/ff550339(v=vs.85)) décrivant la surface ou la mémoire tampon que le pilote doit créer.

</dd> <dt>

*puSurfaceGlobalData* \[ in, out\]
</dt> <dd>

Pointeur vers une [**structure \_ \_ globale de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) qui contient des données de surface partagées globalement avec plusieurs surfaces.

</dd> <dt>

*puSurfaceLocalData* \[ in, out\]
</dt> <dd>

Pointeur désignant une liste de structures [**\_ \_ locales de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) décrivant les objets surface créés par le pilote. Il n’y a généralement qu’une seule entrée dans ce tableau.

</dd> <dt>

*puSurfaceMoreData* \[ in, out\]
</dt> <dd>

Pointeur vers une structure de [**\_ \_ plus grande surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) qui contient des données de surface locales supplémentaires.

</dd> <dt>

*puCreateSurfaceData* \[ in, out\]
</dt> <dd>

Pointeur vers une [**structure \_ CREATESURFACEDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createsurfacedata) qui contient les informations requises pour créer la mémoire tampon.

</dd> <dt>

*puhSurface* \[ in, out\]
</dt> <dd>

Est utilisé par l’API DirectDraw et ne doit pas être renseigné par le pilote.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdCreateD3DBuffer** retourne l’un des codes de rappel suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_pilote DDHAL \_ géré**</dt> </dl>    | Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération. Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction. Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.<br/>                                                                                 |
| <dl> <dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt> </dl> | Le pilote n’a pas de commentaire sur l’opération demandée. Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur. Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.<br/> |



 

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

 

 
