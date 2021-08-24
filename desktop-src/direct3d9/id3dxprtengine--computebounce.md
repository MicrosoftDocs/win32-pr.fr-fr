---
description: Calcule le luminance source résultant d’un rebond unique de la lumière interreflete. Cette méthode peut être utilisée pour n’importe quelle scène éclairée, y compris un modèle de transfert luminance (PRT) à base d’harmonique sphérique (SH).
ms.assetid: 91a6b503-acd2-459b-9d60-de68c879c61b
title: 'ID3DXPRTEngine :: ComputeBounce, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.ComputeBounce
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: cc4f362555c8cc86857733ecc3e75279dc68cc6b339f641f70c592f0e3576a96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847419"
---
# <a name="id3dxprtenginecomputebounce-method"></a>ID3DXPRTEngine :: ComputeBounce, méthode

Calcule le luminance source résultant d’un rebond unique de la lumière interreflete. Cette méthode peut être utilisée pour n’importe quelle scène éclairée, y compris un modèle de transfert luminance (PRT) à base d’harmonique sphérique (SH).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ComputeBounce(
  [in]      LPD3DXPRTBUFFER pDataIn,
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

*pDataOut* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) de sortie qui modélise un rebond unique de la lumière interreflete. Cette mémoire tampon de sortie doit avoir le nombre approprié de canaux de couleur alloués pour la simulation.

</dd> <dt>

*pDataTotal* \[ in, out\]
</dt> <dd>

Type : **[ **LPD3DXPRTBUFFER**](id3dxprtbuffer.md)**

Pointeur vers un objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) facultatif qui est la somme cumulée de toutes les sorties pDataOut précédentes. Peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est D3D \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.

## <a name="remarks"></a>Remarques

Utilisez la séquence d’appel suivante pour modéliser plusieurs rebonds de lumière avec éclairage direct.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;

ComputeDirectLightingSH( SHOrder, pDataA );
// The accumulation buffer, pDataC, needs to be 
// initialized to the direct lighting result.

pDataC->AddBuffer( pDataA );
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // first bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // second bounce
hr = m_pPRTEngine->ComputeBounce( pDataA, pDataB, pDataC ); // third bounce
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, pDataC ); // fourth bounce
```



Utilisez la séquence d’appel suivante pour modéliser plusieurs rebonds de lumière avec la diffusion sous-surface.


```
LPD3DXPRTBUFFER pDataA, pDataB, pDataC; // initialization
ID3DXPRTEngine* m_pPRTEngine;
ComputeDirectLightingSH( SHOrder, pDataA );

// *pDataC should be set to zero. The ComputeSS call will add together     
// the direct lighting results from pDataA for non-subsurface scattering 
// elements and subsurface scattering results for the subsurface scattering
// elements. Perform proper error handling for each call.
    
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // first bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
hr = m_pPRTEngine->ComputeBounce( pDataB, pDataA, NULL   ); // second bounce
hr = m_pPRTEngine->ComputeSS    ( pDataA, pDataB, pDataC );
```



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

[**ID3DXPRTEngine :: en d’autres**](id3dxprtengine--computess.md)
</dt> </dl>

 

 




