---
description: Détruit un objet surface Microsoft DirectDraw précédemment alloué en mode noyau.
ms.assetid: 65419fce-9e82-4621-9906-832144888a3b
title: NtGdiDdDestroySurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdDestroySurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 1ec5538e7aea7abd938cb57dc3dfba9c51e7c6c60f81630bf6665c1ee467ed24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956508"
---
# <a name="ntgdidddestroysurface-function"></a>NtGdiDdDestroySurface fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Détruit un objet surface Microsoft DirectDraw précédemment alloué en mode noyau.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdDestroySurface(
  _In_ HANDLE hSurface,
  _In_ BOOL   bRealDestroy
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurface* \[ dans\]
</dt> <dd>

Handle vers l’objet surface en mode noyau précédemment alloué.

</dd> <dt>

*bRealDestroy* \[ dans\]
</dt> <dd>

Spécifie comment détruire l’aire. Il peut s’agir de l’une des valeurs suivantes.

<dt>



 :


</dt> <dd>

Détruisez la surface et la mémoire vidéo libre.

</dd> <dt>



 FAUSSES


</dt> <dd>

Libérez de la mémoire vidéo tout en laissant la surface dans un État non initialisé.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdDestroySurface** retourne l’un des codes de rappel suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_pilote DDHAL \_ géré**</dt> </dl>    | Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération. Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction. Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.<br/>                                                                                 |
| <dl> <dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt> </dl> | Le pilote n’a pas de commentaire sur l’opération demandée. Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur. Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.<br/> |



 

## <a name="remarks"></a>Remarques

Il est recommandé que les applications utilisent les API DirectDraw et Direct3D pour créer et détruire des surfaces au lieu de cette fonction.

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

 

 




