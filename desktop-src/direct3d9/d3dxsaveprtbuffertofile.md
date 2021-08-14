---
description: Enregistre une mémoire tampon de transfert luminance (PRT) précalculée sur le disque.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: D3DXSavePRTBufferToFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0bfa3d06970d138ff1c868403c20bb41cf14f0a5cbb7116cbe0f0843a51258dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118524529"
---
# <a name="d3dxsaveprtbuffertofile-function"></a>D3DXSavePRTBufferToFile fonction)

Enregistre une mémoire tampon de transfert luminance (PRT) précalculée sur le disque.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a>Paramètres

*pFileName* \[ dans\]

Type : **[LPCSTR](../winprog/windows-data-types.md)**

Nom du fichier dans lequel la mémoire tampon doit être enregistrée.

*pbuffer* \[ dans\]

Type : **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**

Adresse d’un pointeur vers l’objet [**ID3DXPRTBuffer**](id3dxprtbuffer.md) d’entrée.

## <a name="return-value"></a>Valeur retournée

Type : **[HRESULT](../com/structure-of-com-error-codes.md)**

Si la méthode est réussie, la valeur de retour est **D3D \_ OK**. Si la méthode échoue, la valeur de retour peut être **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Remarques

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en [D3DXSavePRTBufferToFileW](). Dans le cas contraire, l’appel de fonction est résolu en **D3DXSavePRTBufferToFileA**.

Le format de fichier PRT est un fichier binaire sous la forme d’un en-tête, puis d’un bloc de données.

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

Pour le cas de *bIsTex* qui est différent de zéro, *échantillons* doit être égal à `TexWidth * TexHeight` .

Le bloc de données qui suit l’en-tête est `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Voir aussi

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
