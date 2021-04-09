---
description: Interroge la quantité de mémoire disponible dans tous les segments de mémoire vidéo.
ms.assetid: 6718e8da-0da0-42e3-a02b-6884b141fe24
title: NtGdiDdGetAvailDriverMemory, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdGetAvailDriverMemory
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: c6ec322665b84b3ddad14b7032b8e49245377d40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033676"
---
# <a name="ntgdiddgetavaildrivermemory-function"></a>NtGdiDdGetAvailDriverMemory fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Interroge la quantité de mémoire disponible dans tous les segments de mémoire vidéo.

## <a name="syntax"></a>Syntaxe


```C++
DWORD APIENTRY NtGdiDdGetAvailDriverMemory(
  _In_    HANDLE                       hDirectDraw,
  _Inout_ PDD_GETAVAILDRIVERMEMORYDATA puGetAvailDriverMemoryData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDirectDraw* \[ dans\]
</dt> <dd>

Handle vers l’objet DirectDraw en mode noyau précédemment créé.

</dd> <dt>

*puGetAvailDriverMemoryData* \[ in, out\]
</dt> <dd>

Pointeur vers une [structure \_ GETAVAILDRIVERMEMORYDATA DD](https://msdn.microsoft.com/library/ms794088.aspx) qui contient les informations requises pour exécuter la requête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdGetAvailDriverMemory** retourne l’un des codes de rappel suivants.



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

 

 




