---
description: Inscrit des modèles personnalisés.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'ID3DXFile :: RegisterTemplates, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522363"
---
# <a name="id3dxfileregistertemplates-method"></a>ID3DXFile :: RegisterTemplates, méthode

Inscrit des modèles personnalisés.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pvData* \[ dans\]
</dt> <dd>

Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**

Pointeur vers une mémoire tampon qui se compose d’un fichier. x au format texte ou binaire qui contient des modèles.

</dd> <dt>

*cbSize* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

Taille de la mémoire tampon vers laquelle pointe pvData, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Si la méthode est réussie, la valeur de retour est S \_ OK. Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Notes

Le fragment de code suivant fournit un exemple d’appel à **RegisterTemplates** et des exemples de contenu pour la mémoire tampon vers laquelle **pvData** pointe.


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



Tous les modèles doivent spécifier un nom et un UUID.

Cette méthode appelle la méthode [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) , en obtenant un pointeur d’interface [**ID3DXFileEnumObject**](id3dxfileenumobject.md) en appelant [**CreateEnumObject**](id3dxfile--createenumobject.md) avec **pvData** comme premier paramètre.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
