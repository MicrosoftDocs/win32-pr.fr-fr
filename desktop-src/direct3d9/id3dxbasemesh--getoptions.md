---
description: Récupère les options de maillage activées pour ce maillage au moment de la création.
ms.assetid: 4be990d7-77ab-4273-b852-e6283a89ac6c
title: 'ID3DXBaseMesh :: GetOptions, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.GetOptions
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a751230b4ccfc537f651846ed455b62d7c7f8262
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527122"
---
# <a name="id3dxbasemeshgetoptions-method"></a>ID3DXBaseMesh :: GetOptions, méthode

Récupère les options de maillage activées pour ce maillage au moment de la création.

## <a name="syntax"></a>Syntaxe


```C++
DWORD GetOptions();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Retourne une combinaison d’un ou plusieurs des indicateurs suivants, indiquant les options activées pour ce maillage au moment de la création.



| Valeur                   | Description                                                                                                                                                                                      |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_32 bits D3DXMESH         | Utilisez des index 32 bits.                                                                                                                                                                              |
| D3DXMESH \_ DONOTCLIP     | Utilisez l' \_ indicateur d’utilisation D3DUSAGE DONOTCLIP pour les mémoires tampons de vertex et d’index.                                                                                                                             |
| D3DXMESH \_ dynamique       | Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Dynamic et D3DXMESH \_ IB \_ Dynamic.                                                                                                                   |
| D3DXMESH \_ RTPATCHES     | Utilisez l' \_ indicateur d’utilisation D3DUSAGE RTPATCHES pour les mémoires tampons de vertex et d’index.                                                                                                                             |
| D3DXMESH \_ NPATCHES      | Si cet indicateur est spécifié, la mémoire tampon de vertex et d’index du maillage est créée avec l' \_ indicateur D3DUSAGE NPATCHES. Cela est obligatoire si l’objet Mesh doit être rendu à l’aide de l’amélioration N-patch. |
| Géré par D3DXMESH \_       | Équivaut à spécifier à la fois D3DXMESH \_ VB \_ Managed et D3DXMESH \_ IB \_ Managed.                                                                                                                   |
| POINTS de D3DXMESH \_        | Utilisez l' \_ indicateur d’utilisation de points D3DUSAGE pour les mémoires tampons de vertex et d’index.                                                                                                                                |
| D3DXMESH \_ IB \_ dynamique   | Utilisez l' \_ indicateur d’utilisation dynamique D3DUSAGE pour les mémoires tampons d’index.                                                                                                                                          |
| D3DXMESH \_ IB \_ géré   | Utilisez la \_ classe de mémoire managée D3DPOOL pour les mémoires tampons d’index.                                                                                                                                         |
| D3DXMESH \_ IB \_ SYSTEMMEM | Utilisez la \_ classe de mémoire D3DPOOL SYSTEMMEM pour les mémoires tampons d’index.                                                                                                                                       |
| D3DXMESH \_ IB \_ WRITEONLY | Utilisez l' \_ indicateur d’utilisation WRITEONLY D3DUSAGE pour les mémoires tampons d’index.                                                                                                                                        |
| D3DXMESH \_ SYSTEMMEM     | Équivaut à spécifier à la fois D3DXMESH \_ VB \_ SYSTEMMEM et D3DXMESH \_ IB \_ SYSTEMMEM.                                                                                                               |
| D3DXMESH \_ VB \_ dynamique   | Utilisez l' \_ indicateur d’utilisation dynamique D3DUSAGE pour les mémoires tampons de vertex.                                                                                                                                         |
| D3DXMESH \_ VB \_ managé   | Utilisez la \_ classe de mémoire managée D3DPOOL pour les mémoires tampons de vertex.                                                                                                                                        |
| D3DXMESH \_ VB \_ SYSTEMMEM | Utilisez la \_ classe de mémoire D3DPOOL SYSTEMMEM pour les mémoires tampons de vertex.                                                                                                                                      |
| D3DXMESH \_ VB \_ WRITEONLY | Utilisez l' \_ indicateur d’utilisation WRITEONLY D3DUSAGE pour les mémoires tampons de vertex.                                                                                                                                       |
| D3DXMESH \_ WRITEONLY     | Équivaut à spécifier à la fois D3DXMESH \_ VB \_ WRITEONLY et D3DXMESH \_ IB \_ WriteOnly.                                                                                                               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXBaseMesh](id3dxbasemesh.md)
</dt> </dl>

 

 
