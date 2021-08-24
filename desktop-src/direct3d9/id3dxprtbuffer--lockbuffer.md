---
description: Verrouille une plage d’exemples de données de vertex ou Texel et obtient un pointeur vers l’emplacement dans la mémoire tampon.
ms.assetid: 8de2725f-507e-41ee-828d-2fb19cc2252c
title: 'ID3DXPRTBuffer :: LockBuffer, méthode (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.LockBuffer
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5d8e3b6310951a5784af99b913298c20d5556baa10b012926f3b68e44d402dbb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606889"
---
# <a name="id3dxprtbufferlockbuffer-method"></a>ID3DXPRTBuffer :: LockBuffer, méthode

Verrouille une plage d’exemples de données de vertex ou Texel et obtient un pointeur vers l’emplacement dans la mémoire tampon.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LockBuffer(
  [in]  UINT  Start,
  [in]  UINT  NumSamples,
  [out] FLOAT **ppData
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Démarrer* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Index de l’exemple de données de vertex ou de Texel.

</dd> <dt>

*Échantillons* \[ dans\]
</dt> <dd>

Type : **[ **uint**](../winprog/windows-data-types.md)**

Nombre de vertex (ou de texels) échantillonnés.

</dd> <dt>

*ppData* \[ à\]
</dt> <dd>

Type : **[ **float**](../winprog/windows-data-types.md)\*\***

Pointeur vers l’emplacement dans la mémoire où commence l’exemple de démarrage. La disposition de la mémoire des données de la mémoire tampon est :


```
float fData[NumberSamples][NumberChannels][NumberCoefficients]      
```



</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur suivante est retournée :

## <a name="remarks"></a>Notes

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Mesh. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXPRTBuffer](id3dxprtbuffer.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumChannels**](id3dxprtbuffer--getnumchannels.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumCoeffs**](id3dxprtbuffer--getnumcoeffs.md)
</dt> <dt>

[**ID3DXPRTBuffer::GetNumSamples**](id3dxprtbuffer--getnumsamples.md)
</dt> </dl>

 

 
