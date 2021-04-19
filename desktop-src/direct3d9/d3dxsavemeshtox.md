---
description: Enregistre un maillage dans un fichier. x.
ms.assetid: 6d9cbca8-3847-4e15-95d4-9df3f8269665
title: D3DXSaveMeshToX, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshToX
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 504e7ad69b83c67dad52ebbf0f6d1eef8639a9fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545278"
---
# <a name="d3dxsavemeshtox-function"></a>D3DXSaveMeshToX fonction)

Enregistre un maillage dans un fichier. x.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSaveMeshToX(
  _In_       LPCTSTR            pFilename,
  _In_       LPD3DXMESH         pMesh,
  _In_ const DWORD              *pAdjacency,
  _In_ const D3DXMATERIAL       *pMaterials,
  _In_ const D3DXEFFECTINSTANCE *pEffectInstances,
  _In_       DWORD              NumMaterials,
  _In_       DWORD              Format
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFilename* \[ dans\]
</dt> <dd>

Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom de fichier. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*pMesh* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXMESH**](id3dxmesh.md)**

Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , qui représente le maillage à enregistrer dans un fichier. x.

</dd> <dt>

*pAdjacency* \[ dans\]
</dt> <dd>

Type : **const [**DWORD**](../winprog/windows-data-types.md) \***

Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque face de la maille. Ce paramètre peut avoir la **valeur null**.

</dd> <dt>

*pMaterials* \[ dans\]
</dt> <dd>

Type : **const [**D3DXMATERIAL**](d3dxmaterial.md) \***

Pointeur vers un tableau de structures [**D3DXMATERIAL**](d3dxmaterial.md) , contenant les informations de matériau à enregistrer dans le fichier. x.

</dd> <dt>

*pEffectInstances* \[ dans\]
</dt> <dd>

Type : **const [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md) \***

Pointeur vers un tableau d’instances d’effet, un par groupe d’attributs dans la maille. Ce paramètre peut avoir la **valeur null**. Une instance Effect est une instance particulière d’informations d’état utilisée pour initialiser un effet. Pour plus d’informations, consultez [**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md).

</dd> <dt>

*NumMaterials* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Nombre de structures [**D3DXMATERIAL**](d3dxmaterial.md) dans le tableau *pMaterials* .

</dd> <dt>

*Format* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Combinaison de format de fichier et d’options d’enregistrement lors de l’enregistrement d’un fichier. x. Consultez les [constantes de fichier D3DX X](dx9-graphics-reference-d3dx-x-file-constants.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveMeshToXW. Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveMeshToXA, car les chaînes ANSI sont utilisées.

Le format de fichier par défaut est binaire ; Toutefois, si un fichier est spécifié à la fois comme un fichier binaire et un fichier texte, il sera enregistré en tant que fichier texte. Quel que soit le format de fichier, vous pouvez également utiliser le format compressé pour réduire la taille du fichier.

Voici un exemple de code standard illustrant l’utilisation de cette fonction.


```
ID3DXMesh*    m_pMesh;           // Mesh object to be saved to a .x file
D3DXMATERIAL* m_pMaterials;      // Array of material structs in the mesh
DWORD         m_dwNumMaterials;  // Number of material structs in the mesh
    
DWORD dwFormat = D3DXF_FILEFORMAT_BINARY;  // Binary-format .x file (default)
// DWORD dwFormat = D3DXF_FILEFORMAT_TEXT; // Text-format .x file
    
// Load mesh into m_pMesh and determine values of m_pMaterials and 
// m_dwNumMaterials with calls to D3DXLoadMeshxxx or other D3DX functions
    
// ...
        
D3DXSaveMeshToX(
    L"outputxfilename.x",
    m_pMesh,
    NULL,
    m_pMaterials,
    NULL,
    m_dwNumMaterials,
    dwFormat );
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions de maillage](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[**D3DXEFFECTDEFAULT**](d3dxeffectdefault.md)
</dt> <dt>

[**D3DXEFFECTINSTANCE**](d3dxeffectinstance.md)
</dt> </dl>

 

 
