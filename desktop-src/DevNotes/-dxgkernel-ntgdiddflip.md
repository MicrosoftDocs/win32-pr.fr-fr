---
description: Provoque l’échange de la mémoire de surface associée aux surfaces cibles et actuelles.
ms.assetid: 2c557393-079e-48e5-b3a6-1157265d88e3
title: NtGdiDdFlip, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlip
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 18113c841c22b31c9768d42491a63ead8cafee3c3b598bc46f442068592e67b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956488"
---
# <a name="ntgdiddflip-function"></a>NtGdiDdFlip fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Provoque l’échange de la mémoire de surface associée aux surfaces cibles et actuelles.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdFlip(
  _In_    HANDLE       hSurfaceCurrent,
  _In_    HANDLE       hSurfaceTarget,
  _In_    HANDLE       hSurfaceCurrentLeft,
  _In_    HANDLE       hSurfaceTargetLeft,
  _Inout_ PDD_FLIPDATA puFlipData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurfaceCurrent* \[ dans\]
</dt> <dd>

Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant l’aire actuelle.

</dd> <dt>

*hSurfaceTarget* \[ dans\]
</dt> <dd>

Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant la surface cible ; autrement dit, la surface vers laquelle le pilote doit retourner.

</dd> <dt>

*hSurfaceCurrentLeft* \[ dans\]
</dt> <dd>

Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant la surface gauche actuelle.

</dd> <dt>

*hSurfaceTargetLeft* \[ dans\]
</dt> <dd>

Handle de la [structure \_ \_ locale de la surface DD](https://msdn.microsoft.com/library/ms793861.aspx) décrivant la surface cible gauche à retourner.

</dd> <dt>

*puFlipData* \[ in, out\]
</dt> <dd>

Pointeur vers une [structure \_ FLIPDATA DD](https://msdn.microsoft.com/library/ms794213.aspx) qui contient les informations requises pour effectuer le retournement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdFlip** retourne l’un des codes de rappel suivants.



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

 

 




