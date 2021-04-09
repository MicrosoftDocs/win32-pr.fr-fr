---
description: Génère le rendu des primitives et retourne l’état de rendu mis à jour.
ms.assetid: ef28ee62-a7ad-406c-a892-ffee14123d16
title: NtGdiD3DDrawPrimitives2, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiD3DDrawPrimitives2
api_type:
- HeaderDef
api_location:
- Ntgdi.h
ms.openlocfilehash: ebde2fd5adf3b0892606d0ebbc1c7d5f6b55d9cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033623"
---
# <a name="ntgdid3ddrawprimitives2-function"></a>NtGdiD3DDrawPrimitives2 fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Génère le rendu des primitives et retourne l’état de rendu mis à jour.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiD3DDrawPrimitives2(
  _In_    HANDLE                         hCmdBuf,
  _In_    HANDLE                         hVBuf,
  _Inout_ LPD3DNTHAL_DRAWPRIMITIVES2DATA pded,
  _Inout_ FLATPTR                        *pfpVidMemCmd,
  _Inout_ DWORD                          *pdwSizeCmd,
  _Inout_ FLATPTR                        *pfpVidMemVtx,
  _Inout_ DWORD                          *pdwSizeVtx
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hCmdBuf* \[ dans\]
</dt> <dd>

Handle de la [**structure \_ \_ locale de la surface DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui identifie la surface DirectDraw contenant les données de commande.

</dd> <dt>

*hVBuf* \[ dans\]
</dt> <dd>

Handle vers la structure de [**\_ surface \_ locale DD**](/windows/win32/api/ddrawint/ns-ddrawint-dd_surface_local) qui identifie la surface DirectDraw contenant les données de vertex.

</dd> <dt>

*PDED* \[ in, out\]
</dt> <dd>

Pointeur vers une structure [**D3DNTHAL \_ DRAWPRIMITIVES2DATA**](/windows-hardware/drivers/ddi/) qui contient les informations requises pour que le pilote restitue une ou plusieurs Primitives.

</dd> <dt>

*pfpVidMemCmd* \[ in, out\]
</dt> <dd>

Nouveau pointeur vers la mémoire vidéo si le pilote a remplacé le tampon de commande.

</dd> <dt>

*pdwSizeCmd* \[ in, out\]
</dt> <dd>

Spécifie le nombre minimal d’octets par lequel le pilote doit augmenter la mémoire tampon de la commande swap.

</dd> <dt>

*pfpVidMemVtx* \[ in, out\]
</dt> <dd>

Nouveau pointeur vers la mémoire vidéo si le pilote a remplacé la mémoire tampon de vertex.

</dd> <dt>

*pdwSizeVtx* \[ in, out\]
</dt> <dd>

Spécifie le nombre minimal d’octets que le pilote doit allouer pour la mémoire tampon de vertex swap.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiD3DDrawPrimitives2** retourne l’un des codes de rappel suivants.



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

 

 
