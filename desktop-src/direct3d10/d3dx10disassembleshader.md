---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DDisassemble. Cette fonction, qui Désassemble un nuanceur compilé en une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, n’existe plus.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: D3DX10DisassembleShader, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106520302"
---
# <a name="d3dx10disassembleshader-function"></a>D3DX10DisassembleShader fonction)

> [!Note]  
> Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .

 

Cette fonction, qui Désassemble un nuanceur compilé en une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, n’existe plus. Utilisez plutôt [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pShader* \[ dans\]
</dt> <dd>

Type : **const void \***

Pointeur vers le [**nuanceur compilé**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

</dd> <dt>

*BytecodeLength* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

Taille de pShader.

</dd> <dt>

*EnableColorCode* \[ dans\]
</dt> <dd>

Type : **[ **bool**](../winprog/windows-data-types.md)**

Incluez des balises HTML dans la sortie pour coder en couleur le résultat.

</dd> <dt>

*pComments* \[ dans\]
</dt> <dd>

Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**

Chaîne de commentaire en haut du nuanceur qui identifie les constantes et les variables de nuanceur.

</dd> <dt>

*ppDisassembly* \[ à\]
</dt> <dd>

Type : **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***

Adresse d’une mémoire tampon (voir [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient le nuanceur désassemblé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Notes

Ce texte retourné comprend un en-tête avec la version du compilateur HLSL utilisée pour générer cet objet, des commentaires décrivant la disposition mémoire des mémoires tampons constantes utilisées par le nuanceur, les signatures d’entrée et de sortie et les points de liaison de ressources.

Voici un exemple de désassemblage d’un nuanceur compilé. L’exemple suppose que vous démarrez avec un nuanceur compilé (représenté sous la forme *pVSBuf* , que vous pouvez voir dans l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions usage général](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
