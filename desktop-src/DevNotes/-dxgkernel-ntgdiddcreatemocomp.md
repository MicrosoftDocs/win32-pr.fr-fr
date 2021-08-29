---
description: Avertit le pilote qu’un décodeur logiciel va commencer à utiliser la compensation de mouvement avec le GUID spécifié.
ms.assetid: c9a55428-7fe6-45dd-987a-d9ab8ae8a1cb
title: NtGdiDdCreateMoComp, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdCreateMoComp
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 71edcfcc82922fb5070ffb3836afc8692cc4e076c59dcfac08ed8290e29cc0a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956588"
---
# <a name="ntgdiddcreatemocomp-function"></a>NtGdiDdCreateMoComp fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Avertit le pilote qu’un décodeur logiciel va commencer à utiliser la compensation de mouvement avec le GUID spécifié.

## <a name="syntax"></a>Syntaxe


```C++
HANDLE APIENTRY NtGdiDdCreateMoComp(
  _In_    HANDLE               hDirectDraw,
  _Inout_ PDD_CREATEMOCOMPDATA puCreateMoCompData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle vers un objet en mode noyau DirectDraw précédemment créé pour l’appareil sur lequel la compensation de mouvement doit être utilisée.

</dd> <dt>

*puCreateMoCompData* \[ in, out\]
</dt> <dd>

Pointeur vers une [**structure \_ CREATEMOCOMPDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_createmocompdata) qui contient les informations requises pour commencer à utiliser la compensation de mouvement.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdCreateMoComp** retourne l’un des codes de rappel suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_pilote DDHAL \_ géré**</dt> </dl>    | Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération. Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction. Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.<br/>                                                                                 |
| <dl> <dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt> </dl> | Le pilote n’a pas de commentaire sur l’opération demandée. Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur. Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.<br/> |



 

## <a name="remarks"></a>Remarques

Pour plus d’informations, consultez Microsoft DirectX Video Acceleration Driver Development Kit (DDK).

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

 

 
