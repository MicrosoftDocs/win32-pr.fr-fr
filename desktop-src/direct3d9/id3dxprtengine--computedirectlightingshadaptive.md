---
description: Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation d’harmonique sphérique (SH), à l’aide de l’échantillonnage adaptatif.
ms.assetid: 792d8460-d608-4384-ac1c-556435074580
title: 'ID3DXPRTEngine :: ComputeDirectLightingSHAdaptive, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeDirectLightingSHAdaptive
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8abbcfd955fa909166b53f6e050b9aff5837508d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762374"
---
# <a name="id3dxprtenginecomputedirectlightingshadaptive-method"></a>ID3DXPRTEngine :: ComputeDirectLightingSHAdaptive, méthode

Calcule la contribution de l’éclairage direct aux objets 3D où le luminance source est représenté par une approximation d’harmonique sphérique (SH), à l’aide de l’échantillonnage adaptatif. Cette méthode génère de nouveaux vertex et des visages sur la maille pour rapprocher plus précisément le signal de transfert luminance (PRT) précalculé.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeDirectLightingSHAdaptive(
  [in]      UINT            Order,
  [in]      FLOAT           AdaptiveThresh,
  [in]      FLOAT           MinEdgeLength,
  [in]      UINT            MaxSubdiv,
  [in, out] LPD3DXPRTBUFFER pDataOut
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Commande* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Ordre de l’évaluation SH. La valeur doit être comprise entre [D3DXSH \_ MINORDER](other-d3dx-constants.md) et D3DXSH \_ MAXORDER, inclus. L’évaluation génère des coefficients de commande ². Le degré de l’évaluation est Order-1.

</dd> <dt>

*AdaptiveThresh* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Seuil sur le vecteur PRT à utiliser pour la subdivision des sommets et des visages de maillage. Si cette valeur est inférieure à 1e-6F, la valeur par défaut de 1e-6F est spécifiée.

</dd> <dt>

*MinEdgeLength* \[ dans\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)**

Longueur minimale du bord de face qui sera générée dans l’échantillonnage adaptatif. Si la méthode détermine que la valeur est trop petite, une valeur dépendante du modèle est spécifiée. Si la valeur est zéro, la valeur par défaut 4 est spécifiée.

</dd> <dt>

*MaxSubdiv* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Niveau maximal de subdivision d’un visage qui sera utilisé dans l’échantillonnage adaptatif.

</dd> <dt>

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie. Cette mémoire tampon doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTEngine](id3dxprtengine.md)
</dt> <dt>

[**ID3DXPRTEngine::RobustMeshRefine**](id3dxprtengine--robustmeshrefine.md)
</dt> </dl>

 

 
