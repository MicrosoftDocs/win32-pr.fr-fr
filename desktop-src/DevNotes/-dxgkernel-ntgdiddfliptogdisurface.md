---
description: avertit le pilote lorsque Microsoft DirectDraw bascule vers ou à partir d’une surface Windows Graphics Device Interface (GDI).
ms.assetid: e79be33a-24bc-477b-bc67-395fff74309c
title: NtGdiDdFlipToGDISurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdFlipToGDISurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8fe1966958b21441f76eb392f2616b22014b6810cb5384ca5a1f79b4ddcb2a9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956388"
---
# <a name="ntgdiddfliptogdisurface-function"></a>NtGdiDdFlipToGDISurface fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez à la place DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

avertit le pilote lorsque Microsoft DirectDraw bascule vers ou à partir d’une surface Windows Graphics Device Interface (GDI).

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdFlipToGDISurface(
  _In_    HANDLE                   hDirectDraw,
  _Inout_ PDD_FLIPTOGDISURFACEDATA puFlipToGDISurfaceData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle vers l’objet DirectDraw en mode noyau précédemment créé.

</dd> <dt>

*puFlipToGDISurfaceData* \[ in, out\]
</dt> <dd>

Pointeur vers une [structure \_ FLIPTOGDISURFACEDATA DD](https://msdn.microsoft.com/library/ms793922.aspx) qui contient les informations de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdFlipToGDISurface** retourne l’un des codes de rappel suivants.



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

 

 




