---
description: 'Calcule un vecteur de transfert qui mappe les luminance sources pour quitter les luminance résultant de la diffusion sous-surface, à l’aide de l’échantillonnage adaptatif et des propriétés de matériau définies par ID3DXPRTEngine :: SetMeshMaterials.'
ms.assetid: 34e42271-703b-4b67-8153-2eca3f8dde92
title: 'ID3DXPRTEngine :: ComputeSSAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeSSAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 198a597020a0bfcbc789cc741e42048bd89eb95f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106542201"
---
# <a name="id3dxprtenginecomputessadaptive-method"></a>ID3DXPRTEngine :: ComputeSSAdaptive, méthode

Calcule un vecteur de transfert qui mappe les luminance sources pour quitter les luminance résultant de la diffusion sous-surface, à l’aide de l’échantillonnage adaptatif et des propriétés de matériau définies par [**ID3DXPRTEngine :: SetMeshMaterials**](id3dxprtengine--setmeshmaterials.md). La méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé. Cette méthode peut être utilisée uniquement pour les matériaux définis par vertex dans un objet de maillage.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeSSAdaptive(
  [in]      LPD3DXPRTBUFFER pDataIn,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut,
  [in, out] LPD3DXPRTBUFFER pDataTotal
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pDataIn* \[ dans\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée qui représente l’objet 3D du retour de lumière précédent. Cette mémoire tampon d’entrée doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> <dt>

*AdaptiveThresh* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Seuil sur le vecteur PRT à utiliser pour la subdivision des sommets et des visages de maillage. Si cette valeur est inférieure à 1e-6F, la valeur par défaut de 1e-6F est spécifiée.

</dd> <dt>

*MinEdgeLength* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif. Si la méthode détermine que la valeur est trop petite, une valeur dépendante du modèle est spécifiée.

</dd> <dt>

*MaxSubdiv* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif. Si la valeur est zéro, la valeur par défaut 4 est spécifiée.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise un rebond unique de la lumière diffusée sous-surface. Cette mémoire tampon de sortie doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Notes

Pour modéliser la diffusion sous-surface, appelez cette méthode pour chaque rebond de lumière après l’appel d’une méthode [**ID3DXPRTEngine :: ComputeDirectLightingSHAdaptive**](id3dxprtengine--computedirectlightingshadaptive.md) .

La sortie de cette méthode n’inclut pas Albedo, et seule la lumière entrante est intégrée dans le simulateur. En ne multipliant pas Albedo, vous pouvez modéliser la variation Albedo à une échelle plus fine que le luminance source, ce qui donne des résultats plus précis de la compression.

Appelez [**ID3DXPRTEngine :: MultiplyAlbedo**](id3dxprtengine--multiplyalbedo.md) pour multiplier chaque vecteur PRT par le Albedo.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::ComputeBounce**](id3dxprtengine--computebounce.md)
</dt> <dt>

[**ID3DXPRTEngine :: en d’autres**](id3dxprtengine--computess.md)
</dt> </dl>

 

 
