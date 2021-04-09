---
description: Ajoute des données d’adjacence à la mémoire tampon d’index du maillage. Lorsque la maille doit être envoyée à un nuanceur Geometry qui accepte les données d’contiguïté, il est nécessaire que le tampon d’index du maillage contienne les données d’contiguïté.
ms.assetid: 8e587620-a4b6-4415-8fe7-9ec22f253b16
title: 'ID3DX10Mesh :: GenerateGSAdjacency, méthode (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GenerateGSAdjacency
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d47747acfa97fbe843dabf527c8f94742db78d6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043138"
---
# <a name="id3dx10meshgenerategsadjacency-method"></a>ID3DX10Mesh :: GenerateGSAdjacency, méthode

Ajoute des données d’adjacence à la mémoire tampon d’index du maillage. Lorsque la maille doit être envoyée à un nuanceur Geometry qui accepte les données d’contiguïté, il est nécessaire que le tampon d’index du maillage contienne les données d’contiguïté.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GenerateGSAdjacency();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DX10Mesh](id3dx10mesh.md)
</dt> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




