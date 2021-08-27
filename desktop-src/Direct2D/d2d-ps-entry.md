---
title: D2D_PS_ENTRY fonction (D2d1effecthelpers. h)
description: Macro qui définit un point d’entrée de nuanceur de pixels avec le nom de fonction donné.
ms.assetid: 4C87369A-EF51-46BA-9CA4-386630A7F866
keywords:
- D2D_PS_ENTRY fonction Direct2D
topic_type:
- apiref
api_name:
- D2D_PS_ENTRY
api_location:
- d2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26369ef5be8c9dea81bf95e60c09ca0041d4275114c8892b85b6b5525f45504b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087782"
---
# <a name="d2d_ps_entry-function"></a>Fonction d’entrée de la \_ PS D2D \_

Macro qui définit un point d’entrée de nuanceur de pixels avec le nom de fonction donné.

## <a name="syntax"></a>Syntaxe

``` syntax
void WINAPI D2D_PS_ENTRY(
  in string Entryname
);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Entryname* \[ dans\]
</dt> <dd>

Nom du point d’entrée du nuanceur de pixels.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Utilisez cette macro au lieu de spécifier la signature d’entrée de point d’entrée de manière normale : tous les paramètres sont implicites et ajoutés par Direct2D pendant la compilation selon le type de cible de compilation (nuanceur complet ou fonction d’exportation).

``` syntax
#define D2D_INPUT_COUNT 1 
#define D2D_INPUT0_SIMPLE 
#include  d2d1effectauthor.hlsli  

D2D_PS_ENTRY(LinkingCompatiblePixelShader) 
{ 
    float4 input = D2DGetInput(0);  

    input.rgb *= input.a; 

    return input; 
} 
```

Dans cet exemple bref, Notez qu’aucun paramètre de fonction n’est déclaré, que le nombre d’entrées et le type de chaque entrée sont déclarés avant la fonction d’entrée, que l’entrée est récupérée en appelant [D2DGetInput](d2dgetinput.md), et que les directives de préprocesseur doivent être définies avant l’inclusion du fichier d’assistance.

Un nuanceur compatible avec la liaison doit fournir un nuanceur de pixels à passage unique standard et une fonction d’exportation de nuanceur. La macro d’entrée de la \_ PS D2D \_ permet de générer chacune d’elles à partir du même code, quand elles sont utilisées conjointement avec le script de compilation du nuanceur.

Lors de la compilation d’un nuanceur complet, les macros sont développées dans le code suivant, qui a une signature d’entrée compatible avec les effets D2D.

``` syntax
Texture2D<float4> InputTexture0; 
SamplerState InputSampler0; 

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,   
    float4 posScene : SCENE_POSITION,    
    float4 uv0  : TEXCOORD0 
    ) : SV_Target 
{ 
    float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);  

    input.rgb *= input.a; 

    return input; 
} 
```

Lors de la compilation d’une version de fonction d’exportation du même code, le code suivant est généré :

``` syntax
// Shader function version 
export float4 LinkingCompatiblePixelShader_Function( 
    float4 input0 : INPUT0 
    ) 
{ 
    input.rgb *= input.a; 

    return input; 
} 
```

Notez que l’entrée de texture, normalement récupérée par l’échantillonnage d’un Texture2D, a été remplacée par un input0 d’entrée de fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>D2d1effecthelpers. hlsli</dt> </dl> |
| DLL<br/>    | <dl> <dt>D2d1.dll</dt> </dl>                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liaison de nuanceurs d’effet](effect-shader-linking.md)
</dt> <dt>

[Applications auxiliaires HLSL](hlsl-helpers.md)
</dt> </dl>

 

 





