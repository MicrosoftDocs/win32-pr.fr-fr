---
description: Enregistre une mémoire tampon de transfert luminance précalculée (PRT) compressée sur le disque.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: D3DXSavePRTCompBufferToFile, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953840"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a>D3DXSavePRTCompBufferToFile fonction)

Enregistre une mémoire tampon de transfert luminance précalculée (PRT) compressée sur le disque.

## <a name="syntax"></a>Syntaxe

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a>Paramètres

*pFileName* \[ dans\]

Type : **[LPCSTR](../winprog/windows-data-types.md)**

Nom du fichier dans lequel la mémoire tampon compressée doit être enregistrée.

*pbuffer* \[ dans\]

Type : **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**

Adresse d’un pointeur vers l’objet [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) d’entrée.

## <a name="return-value"></a>Valeur retournée

Type : **[HRESULT](../com/structure-of-com-error-codes.md)**

Si la méthode est réussie, la valeur de retour est **D3D \_ OK**. Si la méthode échoue, la valeur de retour peut être **D3DERR \_ INVALIDCALL**.

## <a name="remarks"></a>Notes

Le paramètre du compilateur détermine également la version de la fonction. Si Unicode est défini, l’appel de fonction est résolu en [D3DXSavePRTCompBufferToFileW](). Dans le cas contraire, l’appel de fonction est résolu en **D3DXSavePRTCompBufferToFileA**.

Le format de fichier de l’APC est un fichier binaire sous la forme d’un en-tête, puis de deux ou trois blocs de données.

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

Pour le cas de *bIsTex* qui est différent de zéro, *échantillons* doit être égal à `TexWidth * TexHeight` .

Le bloc de données de base qui suit l’en-tête est `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.

Voici le bloc de données de pondérations de l’APC, qui est de `NumPCA * NumSamples * sizeof(float)` octets.

Si *NumClusters* est supérieur à 1, le fichier se termine par le bloc de données des ID de cluster d' `NumSamples * sizeof(UINT)` octets.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |

## <a name="see-also"></a>Voir aussi

[Fonctions de transfert luminance précalculées](dx9-graphics-reference-d3dx-functions-prt.md)
