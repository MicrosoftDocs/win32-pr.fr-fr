---
description: D3DXLoadMeshHierarchyFromX fonction-charge la première hiérarchie d’images à partir d’un fichier. x.
ms.assetid: 1d446b23-9028-4187-b97c-a61edfe68e39
title: D3DXLoadMeshHierarchyFromX, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadMeshHierarchyFromX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 81a087156de61f7997b5d755eb45c0c7e7736fd2345c219b22e8b642ea44e9dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460368"
---
# <a name="d3dxloadmeshhierarchyfromx-function"></a>D3DXLoadMeshHierarchyFromX fonction)

Charge la première hiérarchie d’images à partir d’un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXLoadMeshHierarchyFromX(
  _In_  LPCTSTR                   Filename,
  _In_  DWORD                     MeshOptions,
  _In_  LPDIRECT3DDEVICE9         pDevice,
  _In_  LPD3DXALLOCATEHIERARCHY   pAlloc,
  _In_  LPD3DXLOADUSERDATA        pUserDataLoader,
  _Out_ LPD3DXFRAME               *ppFrameHierarchy,
  _Out_ LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du fichier* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*MeshOptions* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison d’un ou plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) qui spécifient les options de création du maillage.

</dd> <dt>

*pDevice* \[ dans\]
</dt> <dd>

Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**

Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil associé à la maille.

</dd> <dt>

*pAlloc* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXALLOCATEHIERARCHY**](id3dxallocatehierarchy.md)**

Pointeur vers une interface [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) .

</dd> <dt>

*pUserDataLoader* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXLOADUSERDATA**](id3dxloaduserdata.md)**

Interface fournie par l’application qui permet le chargement des données utilisateur. Consultez [**ID3DXLoadUserData**](id3dxloaduserdata.md).

</dd> <dt>

*ppFrameHierarchy* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXFRAME**](d3dxframe.md)\***

Retourne un pointeur vers la hiérarchie de frames chargée. Consultez [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*ppAnimController* \[ à\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Retourne un pointeur vers le contrôleur d’animation correspondant à l’animation dans le fichier. x. Il est créé avec des suivis et des événements par défaut. Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadMeshHierarchyFromXW. Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadMeshHierarchyFromXA.

Tous les maillages du fichier seront réduits en un seul maillage de sortie. Si le fichier contient une hiérarchie de frames, toutes les transformations sont appliquées à la maille.

**D3DXLoadMeshHierarchyFromX** charge les données d’animation et la hiérarchie d’images à partir d’un fichier. x. Il analyse le fichier. x et génère une hiérarchie d’images et un contrôleur d’animation en fonction de l’objet dérivé de [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md)qui lui est passé par le biais de pAlloc. Le chargement des données nécessite plusieurs étapes, comme suit :

1.  Dérivez [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md), en implémentant chaque méthode. Cela contrôle la manière dont les images et les maillages sont alloués et libérés.
2.  Dérivez [**ID3DXLoadUserData**](id3dxloaduserdata.md), en implémentant chaque méthode. Si votre fichier. x n’a pas de données incorporées définies par l’utilisateur ou si vous n’en avez pas besoin, vous pouvez ignorer cette partie.
3.  Créez un objet de votre classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) , et éventuellement de votre classe LoadUserData. Vous n’avez pas besoin d’appeler les méthodes de ces objets vous-même.
4.  Appelez **D3DXLoadMeshHierarchyFromX**, en passant votre objet [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) et votre objet [**ID3DXLoadUserData**](id3dxloaduserdata.md) (ou **null**) pour créer la hiérarchie d’images et le contrôleur d’animation. Tous les jeux d’animations et les frames sont automatiquement inscrits sur le contrôleur d’animation.

Pendant le chargement, [**CreateFrame**](id3dxallocatehierarchy--createframe.md) et [**LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) sont rappelés sur chaque frame pour contrôler le chargement et l’allocation du frame. L’application définit ces méthodes pour contrôler le mode de stockage des frames. [**CreateMeshContainer**](id3dxallocatehierarchy--createmeshcontainer.md) et [**LoadMeshChildData**](id3dxloaduserdata--loadmeshchilddata.md) sont rappelés sur chaque objet de maillage pour contrôler le chargement et l’allocation des objets de maillage. [**LoadTopLevelData**](id3dxloaduserdata--loadtopleveldata.md) est rappelée pour chaque objet de niveau supérieur qui n’est pas chargé par les autres méthodes.

Pour libérer ces données, appelez ID3DXAnimationController :: Release pour libérer les jeux d’animations et [**D3DXFRAMEDestroy**](d3dxframedestroy.md), en passant le nœud racine de la hiérarchie de frames et un objet de votre classe [**ID3DXAllocateHierarchy**](id3dxallocatehierarchy.md) dérivée. [**DestroyFrame**](id3dxallocatehierarchy--destroyframe.md) et [**DestroyMeshContainer**](id3dxallocatehierarchy--destroymeshcontainer.md) sont appelés pour chaque objet Frame et Mesh dans la hiérarchie d’images. Votre implémentation de **DestroyFrame** doit libérer tout ce qui est alloué par [**CreateFrame**](id3dxallocatehierarchy--createframe.md), et de la même façon pour les méthodes de conteneur de maillage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
