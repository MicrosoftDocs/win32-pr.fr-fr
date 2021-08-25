---
description: Interroge la quantité de mémoire disponible dans le segment de mémoire géré par le pilote.
ms.assetid: d7f8792b-a515-4e70-9474-6a3474b6612b
title: NtGdiD3DContextDestroyAll, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DContextDestroyAll
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: 7b44eae1e28938dacff2b82d3b82babe2dc7e5a773c0d2ec4b476765aa9de4b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824959"
---
# <a name="ntgdid3dcontextdestroyall-function"></a>NtGdiD3DContextDestroyAll fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Interroge la quantité de mémoire disponible dans le segment de mémoire géré par le pilote.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiD3DContextDestroyAll(void);
```



## <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

**NtGdiD3DContextDestroyAll** retourne l’un des codes de rappel suivants.



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

 

 




