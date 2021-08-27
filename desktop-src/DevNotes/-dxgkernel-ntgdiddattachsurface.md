---
description: Attache deux représentations de surface en mode noyau.
ms.assetid: f1b1859f-8b62-4385-9e8a-296086446fe7
title: NtGdiDdAttachSurface, fonction (Ntgdi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtGdiDdAttachSurface
api_type:
- DllExport
api_location:
- Ntgdi.h
- Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
- GDI32.dll
- GDI32Full.dll
ms.openlocfilehash: 8ec07f539cfa2a99338d8366f10f7c3d79dbdd5ef26a6de0ee0296941e2c84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088029"
---
# <a name="ntgdiddattachsurface-function"></a>NtGdiDdAttachSurface fonction)

\[Cette fonction est sujette à modification avec chaque révision du système d’exploitation. Utilisez plutôt Microsoft DirectDraw et Microsoft Direct3DAPIs ; Ces API isolent les applications de ces modifications du système d’exploitation et masquent de nombreuses autres difficultés liées à l’interaction directe avec les pilotes d’affichage.\]

Attache deux représentations de surface en mode noyau.

## <a name="syntax"></a>Syntaxe


```C++
BOOL APIENTRY NtGdiDdAttachSurface(
  _In_ HANDLE hSurfaceFrom,
  _In_ HANDLE hSurfaceTo
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hSurfaceFrom* \[ dans\]
</dt> <dd>

Handle vers l’objet surface en mode noyau qui sera le point de départ de la nouvelle pièce jointe.

</dd> <dt>

*hSurfaceTo* \[ dans\]
</dt> <dd>

Handle vers l’objet surface en mode noyau qui sera le point de terminaison de la nouvelle pièce jointe.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

**NtGdiDdAttachSurface** retourne l’un des éléments suivants :



| Code de retour                                                                          | Description                             |
|--------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**:**</dt> </dl>  | L’appel de fonction a réussi.<br/> |
| <dl> <dt>**FAUSSES**</dt> </dl> | L’appel de fonction a échoué.<br/>    |



 

## <a name="remarks"></a>Remarques

Pour obtenir une description complète des pièces jointes, consultez le kit de développement logiciel (SDK) et le kit de développement de pilotes (DDK) DirectDraw.

> [!Note]  
> Comme pour les autres pièces jointes de surface, la pièce jointe résultante est unidirectionnelle. Une fois cette fonction appelée, *hSurfaceTo* n’est pas attaché à *hSurfaceFrom*.

 

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

 

 




