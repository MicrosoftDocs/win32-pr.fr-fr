---
description: Crée un fichier. x et y enregistre la hiérarchie de maillage et les animations correspondantes.
ms.assetid: 803926fe-8cb7-422a-9920-56f7d0b0d0ea
title: D3DXSaveMeshHierarchyToFile, fonction (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSaveMeshHierarchyToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f2de65f9bc2f9e40a5bc07c6f0b4d00112f0df21
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538511"
---
# <a name="d3dxsavemeshhierarchytofile-function"></a>D3DXSaveMeshHierarchyToFile fonction)

Crée un fichier. x et y enregistre la hiérarchie de maillage et les animations correspondantes.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DXSaveMeshHierarchyToFile(
  _In_       LPCSTR                    pFilename,
  _In_       DWORD                     XFormat,
  _In_ const D3DXFRAME                 *pFrameRoot,
  _In_       LPD3DXANIMATIONCONTROLLER pAnimController,
  _In_       LPD3DXSAVEUSERDATA        pUserDataSaver
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFilename* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Pointeur vers une chaîne qui spécifie le nom du fichier. x identifiant le maillage enregistré. Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR. Dans le cas contraire, le type de données String est résolu en LPCSTR. Consultez la section Notes.

</dd> <dt>

*XFormat* \[ dans\]
</dt> <dd>

Type : **[ **DWORD**](../winprog/windows-data-types.md)**

Format du fichier. x (texte ou binaire, compressé ou non). Consultez D3DXF \_ FILEFORMAT. D3DXF \_ FileFormat \_ Compressed peut être combiné (à l’aide d’un or logique) avec les \_ indicateurs de texte D3DXF FileFormat \_ ou D3DXF \_ FileFormat \_ pour réduire la taille du fichier de sortie.

</dd> <dt>

*pFrameRoot* \[ dans\]
</dt> <dd>

Type : **const [**D3DXFRAME**](d3dxframe.md) \***

Nœud racine de la hiérarchie à enregistrer. Consultez [**D3DXFRAME**](d3dxframe.md).

</dd> <dt>

*pAnimController* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)**

Contrôleur d’animation qui contient les jeux d’animations à stocker. Consultez [**ID3DXAnimationController**](id3dxanimationcontroller.md).

</dd> <dt>

*pUserDataSaver* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXSAVEUSERDATA**](id3dxsaveuserdata.md)**

Interface fournie par l’application qui permet l’enregistrement des données utilisateur. Consultez [**ID3DXSaveUserData**](id3dxsaveuserdata.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la fonction est réussie, la valeur de retour est D3D \_ OK. Si la fonction échoue, la valeur de retour peut être : D3DERR \_ INVALIDCALL.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en D3DXSaveMeshHierarchyToFileW. Dans le cas contraire, l’appel de fonction est résolu en D3DXSaveMeshHierarchyToFileA.

Cette fonction n’enregistre pas les jeux d’animations compressés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions d’animation](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> <dt>

[Référence de fichier X](dx9-graphics-reference-d3dx-x-file.md)
</dt> </dl>

 

 
