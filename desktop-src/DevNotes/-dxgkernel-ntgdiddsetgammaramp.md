---
description: Définit la rampe gamma de l’appareil.
ms.assetid: 92ea0247-6eec-4c5f-9ea7-65f6b97dde1e
title: NtGdiDdSetGammaRamp, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdSetGammaRamp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 0c5efba67eedbd6e70f1e0682f42c1855948cecd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110122"
---
# <a name="ntgdiddsetgammaramp-function"></a>NtGdiDdSetGammaRamp fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Définit la rampe gamma de l’appareil.

## <a name="syntax"></a>Syntaxe


```C++
BOOL APIENTRY NtGdiDdSetGammaRamp(
  _In_ HANDLE hDirectDraw,
  _In_ HDC    hdc,
  _In_ LPVOID lpGammaRamp
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle de l’objet de pilote en mode noyau pour lequel la rampe doit être définie.

</dd> <dt>

*HDC* \[ dans\]
</dt> <dd>

Réservé.

</dd> <dt>

*lpGammaRamp* \[ dans\]
</dt> <dd>

Pointeur vers un tableau de structures **DDGAMMARAMP** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est **true** si la fonction réussit. Dans le cas contraire, la **valeur est null**.

## <a name="remarks"></a>Notes

Il est recommandé que les applications utilisent plutôt les méthodes **IDirectDrawGammaControl :: SetGammaRamp** ou [**IDirect3DDevice9 :: SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) , car ces méthodes offrent les mêmes fonctionnalités indépendamment du système d’exploitation.

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

 

 
