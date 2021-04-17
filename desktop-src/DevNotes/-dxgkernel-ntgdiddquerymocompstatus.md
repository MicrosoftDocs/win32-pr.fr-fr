---
description: Interroge l’état de l’opération de rendu la plus récente à la surface spécifiée.
ms.assetid: bc7f8f84-119e-4c09-87f5-6b122e9f9821
title: NtGdiDdQueryMoCompStatus, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdQueryMoCompStatus
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 7795602e29d565022d532a0ebd51be1c4249a02e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523975"
---
# <a name="ntgdiddquerymocompstatus-function"></a>NtGdiDdQueryMoCompStatus fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Interroge l’état de l’opération de rendu la plus récente à la surface spécifiée.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdQueryMoCompStatus(
  _In_    HANDLE                    hMoComp,
  _Inout_ PDD_QUERYMOCOMPSTATUSDATA puQueryMoCompStatusData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hMoComp* \[ dans\]
</dt> <dd>

Pointeur vers une [**structure \_ \_ locale DD MOTIONCOMP**](/windows/win32/api/ddrawint/ns-ddrawint-dd_motioncomp_local) qui contient une description de la compensation de mouvement demandée.

</dd> <dt>

*puQueryMoCompStatusData* \[ in, out\]
</dt> <dd>

Pointeur vers une [**structure \_ QUERYMOCOMPSTATUSDATA DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_querymocompstatusdata) qui contient les informations nécessaires pour interroger l’État.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdQueryMoCompStatus** retourne l’un des codes de rappel suivants.



| Code de retour                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_pilote DDHAL \_ géré**</dt> </dl>    | Le pilote a effectué l’opération et a retourné un code de retour valide pour cette opération. Si ce code est JJ \_ OK, DirectDraw ou Direct3D continue avec la fonction. Dans le cas contraire, DirectDraw ou Direct3D retourne le code d’erreur fourni par le pilote et abandonne la fonction.<br/>                                                                                 |
| <dl> <dt>**DDHAL de \_ pilote \_ NOTHANDLED**</dt> </dl> | Le pilote n’a pas de commentaire sur l’opération demandée. Si le pilote doit avoir implémenté un rappel particulier, DirectDraw ou Direct3D signale une condition d’erreur. Dans le cas contraire, DirectDraw ou Direct3D gère l’opération comme si le rappel de pilote n’avait pas été défini par l’exécution de l’implémentation de DirectDraw ou de l’implémentation indépendante du périphérique Direct3D.<br/> |



 

## <a name="remarks"></a>Notes

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

 

 
