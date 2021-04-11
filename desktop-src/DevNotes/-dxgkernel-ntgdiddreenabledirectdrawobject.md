---
description: Réactive un objet périphérique en mode noyau Microsoft DirectDraw après un changement de mode.
ms.assetid: 26451881-cebf-4db1-aeed-365f0dae6704
title: NtGdiDdReenableDirectDrawObject, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdReenableDirectDrawObject
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: afd736317ecdf802cb418e81063b622db43f0651
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111167"
---
# <a name="ntgdiddreenabledirectdrawobject-function"></a>NtGdiDdReenableDirectDrawObject fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Réactive un objet périphérique en mode noyau Microsoft DirectDraw après un changement de mode.

## <a name="syntax"></a>Syntaxe


```C++
BOOL APIENTRY NtGdiDdReenableDirectDrawObject(
  _In_    HANDLE hDirectDrawLocal,
  _Inout_ BOOL   *pubNewMode
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDrawLocal* \[ dans\]
</dt> <dd>

Objet DirectDraw qui doit être réactivé.

</dd> <dt>

*pubNewMode* \[ in, out\]
</dt> <dd>

Pointeur vers une valeur BOOLÉENNE qui sera remplie avec une valeur qui indique si le mode d’affichage a changé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

En cas de réussite (l’appareil peut être réactivé), cette fonction retourne la **valeur true**. Sinon (par exemple, le pilote d’affichage a été modifié), la **valeur false** est retournée.

## <a name="remarks"></a>Notes

Une fois l’objet réactivé, les fonctionnalités de l’appareil peuvent être interrogées à nouveau via un appel à [**NtGdiDdQueryDirectDrawObject**](-dxgkernel-ntgdiddquerydirectdrawobject.md).

Il est recommandé aux applications d’utiliser les API DirectDraw ou [Direct3D](../direct3d10/d3d10-graphics-reference.md) version 8, qui automatisent et résument ce processus de manière indépendante du système d’exploitation.

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

[**DdReenableDirectDrawObject**](/windows/desktop/api/Ddrawgdi/nf-ddrawgdi-ddreenabledirectdrawobject)
</dt> </dl>

 

 
