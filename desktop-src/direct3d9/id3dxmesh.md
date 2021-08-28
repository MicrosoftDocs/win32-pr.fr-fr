---
description: Les applications utilisent les méthodes de l’interface ID3DXMesh pour manipuler les objets de maillage.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Interface ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3e6617287a9465384b3c260aebe384f4764bbd0f41a673408f48d36c450597f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119629469"
---
# <a name="id3dxmesh-interface"></a>Interface ID3DXMesh

Les applications utilisent les méthodes de l’interface ID3DXMesh pour manipuler les objets de maillage.

## <a name="members"></a>Membres

L’interface **ID3DXMesh** hérite de [**ID3DXBaseMesh**](id3dxbasemesh.md). **ID3DXMesh** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DXMesh** possède ces méthodes.



| Méthode                                                            | Description                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**LockAttributeBuffer**](id3dxmesh--lockattributebuffer.md)     | Verrouille la mémoire tampon de maillage qui contient les données d’attribut de maillage et retourne un pointeur vers celle-ci.<br/>                                   |
| [**Optimiser**](id3dxmesh--optimize.md)                           | Génère un nouveau maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin.<br/>                                     |
| [**OptimizeInplace**](id3dxmesh--optimizeinplace.md)             | Génère un maillage avec des faces et des sommets réorganisés pour optimiser les performances du dessin. Cette méthode réorganise la maille existante.<br/> |
| [**SetAttributeTable**](id3dxmesh--setattributetable.md)         | Définit la table d’attributs pour un maillage et le nombre d’entrées stockées dans la table.<br/>                                          |
| [**UnlockAttributeBuffer**](id3dxmesh--unlockattributebuffer.md) | Déverrouille une mémoire tampon d’attribut.<br/>                                                                                                |



 

## <a name="remarks"></a>Remarques

Pour obtenir l’interface **ID3DXMesh** , appelez la fonction [**D3DXCreateMesh**](d3dxcreatemesh.md) ou [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .

Cette interface hérite des fonctionnalités supplémentaires de l’interface [**ID3DXBaseMesh**](id3dxbasemesh.md) .

Le type LPD3DXMESH est défini comme un pointeur vers l’interface **ID3DXMesh** .


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID3DXBaseMesh**](id3dxbasemesh.md)
</dt> <dt>

[Interfaces D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




