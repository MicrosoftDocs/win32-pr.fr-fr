---
description: Crée un objet surface en mode noyau qui représente l’objet surface en mode utilisateur référencé par puSurfaceLocal.
ms.assetid: 1b2886a8-279b-4bec-9fb8-b88a68ded25b
title: NtGdiDdCreateSurfaceObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateSurfaceObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 5aef9a70897f5a8a46f9c966242d8842c54f9946
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033603"
---
# <a name="ntgdiddcreatesurfaceobject-function"></a>NtGdiDdCreateSurfaceObject fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Crée un objet surface en mode noyau qui représente l’objet surface en mode utilisateur référencé par *puSurfaceLocal*.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE APIENTRY NtGdiDdCreateSurfaceObject(
  _In_ HANDLE             hDirectDrawLocal,
  _In_ HANDLE             hSurface,
  _In_ PDD_SURFACE_LOCAL  puSurfaceLocal,
  _In_ PDD_SURFACE_MORE   puSurfaceMore,
  _In_ PDD_SURFACE_GLOBAL puSurfaceGlobal,
  _In_ BOOL               bComplete
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDrawLocal* \[ dans\]
</dt> <dd>

Handle vers l’objet DirectDraw en mode noyau.

</dd> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle précédent à la même surface. Utilisé si la surface est recréée après un basculement de mode.

</dd> <dt>

*puSurfaceLocal* \[ dans\]
</dt> <dd>

Pointeur vers la structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui représente l’objet de surface de mode utilisateur DirectDraw avec lequel associer la mémoire allouée. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*puSurfaceMore* \[ dans\]
</dt> <dd>

Pointeur vers la structure de [**\_ \_ plus de surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_more) qui contient des données locales supplémentaires pour chaque objet surface individuel. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*puSurfaceGlobal* \[ dans\]
</dt> <dd>

Pointeur vers la [**structure \_ \_ globale de la surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_global) qui contient les données de surface partagées globalement avec plusieurs surfaces. Pour plus d’informations, consultez la documentation du DDK.

</dd> <dt>

*bComplete* \[ dans\]
</dt> <dd>

Indicateur de fin de l’objet en mode noyau. Il peut s’agir de l’une des valeurs suivantes.

<dt>



 :


</dt> <dd>

Terminez tout le traitement concernant la représentation en mode noyau.

</dd> <dt>



 FAUSSES


</dt> <dd>

Créez l’objet, mais ne configurez pas de données internes telles que le pointeur de mémoire. Les objets créés à l’aide de la **valeur false** peuvent être joints à l’aide de [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md) et sont terminés par un appel à [**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md).

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite, cette fonction retourne un handle vers la représentation sous forme de surface en mode noyau. Sinon, elle retourne la **valeur null**.

## <a name="remarks"></a>Notes

Il est recommandé aux applications d’utiliser les API DirectDraw et [Direct3D](../direct3d10/d3d10-graphics-reference.md) pour créer et gérer des objets d’appareils graphiques. Ces constructions résument le processus de création d’appareils de façon simplifiée et indépendante du système d’exploitation.

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

[**DdCreateSurfaceObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddcreatesurfaceobject)
</dt> <dt>

[**NtGdiDdDeleteSurfaceObject**](-dxgkernel-ntgdidddeletesurfaceobject.md)
</dt> <dt>

[**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)
</dt> <dt>

[**NtGdiDdCreateSurface**](-dxgkernel-ntgdiddcreatesurface.md)
</dt> </dl>

 

 
