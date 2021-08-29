---
description: Verrouille une zone spécifiée de la mémoire de surface et fournit un pointeur valide vers un bloc de mémoire associé à une surface.
ms.assetid: 02810576-73d8-431d-ab41-3244dcff311f
title: NtGdiDdLock, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdLock
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8cd16008c01a5099b3bb85ecc97127edd5fb3f3941d469a2fbc7c4a11caccb49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956318"
---
# <a name="ntgdiddlock-function"></a>NtGdiDdLock fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Verrouille une zone spécifiée de la mémoire de surface et fournit un pointeur valide vers un bloc de mémoire associé à une surface.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdLock(
  _In_    HANDLE       hSurface,
  _Inout_ PDD_LOCKDATA puLockData,
  _In_    HDC          hdcClip
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle vers une structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui décrit la surface associée à la région de mémoire à verrouiller.

</dd> <dt>

*puLockData* \[ in, out\]
</dt> <dd>

Pointeur vers une [**structure \_ LOCKDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_lockdata) qui contient les informations requises pour effectuer le verrouillage.

</dd> <dt>

*hdcClip* \[ dans\]
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdLock** retourne l’un des codes de rappel suivants.



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

 

 
