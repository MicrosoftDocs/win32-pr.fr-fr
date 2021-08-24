---
description: Cette fonction, qui crée un objet Shader-Reflection pour la récupération d’informations sur un nuanceur compilé, n’existe plus. Au lieu de cela, utilisez D3DReflect ou D3D11Reflect.
ms.assetid: 7090418c-1940-4f07-b075-937e3399613c
title: D3DX10ReflectShader, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10ReflectShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 7694aa0dcfcc256358993f29c9ed448c1648b35768e5844a959726a6737c2371
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753079"
---
# <a name="d3dx10reflectshader-function"></a>D3DX10ReflectShader fonction)

Cette fonction, qui crée un objet Shader-Reflection pour la récupération d’informations sur un nuanceur compilé, n’existe plus. Au lieu de cela, utilisez [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) ou [**D3D11Reflect**](../direct3dhlsl/d3d11reflect.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT D3DX10ReflectShader(
  _In_  const void                    *pShaderBytecode,
  _In_        SIZE_T                  BytecodeLength,
  _Out_       ID3D10ShaderReflection1 **ppReflector
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pShaderBytecode* \[ dans\]
</dt> <dd>

Type : **const void \***

Pointeur vers le nuanceur compilé. Pour obtenir ce pointeur, consultez [obtention d’un pointeur vers un nuanceur compilé](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

</dd> <dt>

*BytecodeLength* \[ dans\]
</dt> <dd>

Type : **[ **taille \_ T**](../winprog/windows-data-types.md)**

Longueur de pShaderBytecode.

</dd> <dt>

*ppReflector* \[ à\]
</dt> <dd>

Type : **[ **ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1)\*\***

Adresse d’une interface de réflexion du nuanceur (voir [**interface ID3D10ShaderReflection1**](/windows/desktop/api/D3D10_1Shader/nn-d3d10_1shader-id3d10shaderreflection1).)

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.

## <a name="remarks"></a>Remarques

Voici un exemple de création d’un objet Shader-Reflection. L’exemple suppose que vous démarrez avec un nuanceur compilé (représenté sous la forme


```
pVSBuf
```



ce que vous pouvez voir dans l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).


```
ID3D10ShaderReflection1* pIShaderReflection1 = NULL;
D3D10_SHADER_DESC desc;
hr = D3D10ReflectShader( (void*) pVSBuf->GetBufferPointer(), pVSBuf->GetBufferSize(),
    &pIShaderReflection1 );
if( pIShaderReflection1 )
{
    pIShaderReflection1->GetDesc( &desc );
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

 

 
