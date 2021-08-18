---
description: Retourne le handle de l’API Microsoft DirectX en mode noyau à utiliser dans les appels suivants aux points d’entrée en mode noyau qui contrôlent le mécanisme de l’API DirectX.
ms.assetid: c95cb188-305f-4b60-be55-0511b57f0597
title: NtGdiDdGetDxHandle, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetDxHandle
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 13234c7ebe350f096164f0a5de0bde7a60e819e80899aa87258a76727855b869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331919"
---
# <a name="ntgdiddgetdxhandle-function"></a>NtGdiDdGetDxHandle fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Retourne le handle de l’API Microsoft DirectX en mode noyau à utiliser dans les appels suivants aux points d’entrée en mode noyau qui contrôlent le mécanisme de l’API DirectX.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdGetDxHandle(
  _In_ HANDLE hDirectDraw,
  _In_ HANDLE hSurface,
  _In_ BOOL   bRelease
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle de l’objet DirectDraw propriétaire de l’aire. Ce paramètre est facultatif et peut avoir la valeur **null**.

</dd> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle vers la surface pour laquelle retourner un handle d’API DirectX en mode noyau. Ce paramètre est facultatif et peut avoir la valeur **null**.

</dd> <dt>

*bRelease* \[ dans\]
</dt> <dd>

Affectez la valeur **true** si l’interface du mode noyau de l’API DirectX doit être libérée. Sinon, **false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Handle d’API DirectX utilisé dans les points d’entrée de noyau orientés API DirectX suivants.

## <a name="remarks"></a>Remarques

Si *hDirectDraw* et *hSurface* sont tous les deux spécifiés, *hSurface* est ignoré.

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

 

 




