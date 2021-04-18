---
description: Dessinez plusieurs instances du même sous-ensemble d’une maille.
ms.assetid: 2a17ecdb-c6f3-401c-b7ed-8a42fe159de0
title: ID3DX10Mesh ::D méthode rawSubsetInstanced (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.DrawSubsetInstanced
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 314f85d896be629254def560e55ce6a05bfe1fbd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525898"
---
# <a name="id3dx10meshdrawsubsetinstanced-method"></a>ID3DX10Mesh ::D méthode rawSubsetInstanced

Dessinez plusieurs instances du même sous-ensemble d’une maille.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DrawSubsetInstanced(
  [in] UINT AttribId,
  [in] UINT InstanceCount,
  [in] UINT StartInstanceLocation
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AttribId* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Spécifie le sous-ensemble du maillage à dessiner. Cette valeur est utilisée pour différencier les visages d’un maillage comme appartenant à un ou plusieurs groupes d’attributs. Consultez la section Remarques.

</dd> <dt>

*InstanceCount* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre d’instances à restituer.

</dd> <dt>

*StartInstanceLocation* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

L’instance à partir de laquelle commencer l’extraction dans chaque mémoire tampon marquée comme des données d’instance.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

La valeur de retour est l’une des valeurs indiquées dans les [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Notes

Une maille contient une table d’attributs. La table d’attributs peut diviser un maillage en sous-ensembles, où chaque sous-ensemble est identifié par un ID d’attribut. Par exemple, un maillage avec 200 faces, divisé en trois sous-ensembles, peut avoir une table d’attributs qui ressemble à ceci :



|            |                 |
|------------|-----------------|
| AttribID 0 | Visages 0 ~ 50    |
| AttribID 1 | Visages 51 ~ 125  |
| AttribID 2 | Visages 126 ~ 200 |



 

L’instanciation peut étendre les performances en réutilisant la même géométrie pour dessiner plusieurs objets dans une scène. Un exemple d’instanciation pourrait consister à dessiner le même objet avec des positions et des couleurs différentes. L’indexation requiert plusieurs mémoires tampons de vertex : au moins une pour les données par vertex et une deuxième mémoire tampon pour les données par instance.

Les instances de dessin avec DrawSubsetInstanced sont très similaires au processus utilisé avec [**ID3D10Device ::D rawindexedinstanced**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-drawindexedinstanced) décrit dans [exemple d’instanciation](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx). La principale différence lors de l’utilisation de DrawSubsetInstanced est que les mémoires tampons de vertex et d’index doivent être extraites de l’objet d' [**interface ID3DX10Mesh**](id3dx10mesh.md) avant que les données d’instanciation puissent être combinées.

Le code suivant illustre l’extraction des tampons de vertex et d’index à partir de l’objet de maillage.


```
      ID3D10Buffer* vertexBuffer;
      pDeviceObj->pMesh->GetDeviceVertexBuffer(0, &vertexBuffer);
      ID3D10Buffer* indexBuffer;
      pDeviceObj->pMesh->GetDeviceIndexBuffer(&indexBuffer);
      
```



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

 

 
