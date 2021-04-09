---
description: Supprime une pièce jointe, créée avec NtGdiDdAttachSurface, entre deux objets surface en mode noyau.
ms.assetid: 28037b42-a00c-4063-93ee-5d71761a95d8
title: NtGdiDdUnattachSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdUnattachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 4513020a40c9b704e0b84e1a8b1c582be95db78f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950434"
---
# <a name="ntgdiddunattachsurface-function"></a>NtGdiDdUnattachSurface fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Supprime une pièce jointe, créée avec [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md), entre deux objets surface en mode noyau.

## <a name="syntax"></a>Syntaxe


```C++
VOID APIENTRY NtGdiDdUnattachSurface(
  _In_ HANDLE hSurface,
  _In_ HANDLE hSurfaceAttached
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Objet surface en mode noyau qui a été passé en tant que paramètre hSurfaceFrom à [**NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md).

</dd> <dt>

*hSurfaceAttached* \[ dans\]
</dt> <dd>

Objet surface en mode noyau qui a été passé en tant que paramètre hSurfaceTo à [ **NtGdiDdAttachSurface**](-dxgkernel-ntgdiddattachsurface.md)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdUnattachSurface** retourne l’un des codes de rappel suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_pilote DDHAL \_ géré**</dt> </dl>    | Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération. Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction. Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.<br/>                                                                                 |
| <dl> <dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt> </dl> | Le pilote n’a pas de commentaire sur l’opération demandée. Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur. Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.<br/> |



 

## <a name="remarks"></a>Notes

Il est recommandé que les applications utilisent l’API DirectDraw, qui gère les pièces jointes de surface de manière plus détaillée.

Il n’est pas nécessaire d’appeler cette fonction, car le noyau détruit automatiquement toutes les pièces jointes lorsque [**NtGdiDdDestroySurface**](-dxgkernel-ntgdidddestroysurface.md) est appelé.

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

 

 




