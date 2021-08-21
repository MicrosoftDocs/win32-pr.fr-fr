---
title: Différences entre les effets 10 et les effets 11
description: Cette rubrique présente les différences entre les effets 10 et 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b488015deae8cc93b9bc692c49d66ff1510bcc5639047fe253265be5b382a85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990119"
---
# <a name="differences-between-effects-10-and-effects-11"></a>Différences entre les effets 10 et les effets 11

Cette rubrique présente les différences entre les effets 10 et 11.

## <a name="device-contexts-threading-and-cloning"></a>Contextes de périphérique, Threading et clonage

L’interface ID3D10Device a été divisée en deux interfaces dans Direct3D 11 : ID3D11Device et ID3D11DeviceContext. Vous pouvez créer plusieurs ID3D11DeviceContexts pour faciliter l’exécution simultanée sur plusieurs threads. Effects 11 étend ce concept à l’infrastructure Effects.

Le runtime Effects 11 est monothread. Pour cette raison, vous ne devez pas utiliser une seule instance ID3DX11Effect avec plusieurs threads simultanément.

Pour utiliser le runtime Effects 11 sur plusieurs instances, vous devez créer des instances ID3DX11Effect distinctes. Étant donné que le ID3D11DeviceContext est également à thread unique, vous devez passer différentes instances ID3D11DeviceContext à chaque instance Effect à l’application. Vous pouvez utiliser ces contextes de périphérique distincts pour créer des listes de commandes afin que le thread de rendu puisse les appliquer dans le contexte de périphérique immédiat.

Le moyen le plus simple de créer plusieurs effets qui encapsulent la même fonctionnalité, pour une utilisation sur plusieurs threads, est de créer un effet, puis de créer des copies clonées. Le clonage présente les avantages suivants par rapport à la création de plusieurs copies à partir de zéro :

1.  La routine de clonage est plus rapide que la routine de création.
2.  Les effets clonés partagent les nuanceurs, les blocs d’État et les instances de classe créés (ils n’ont donc pas besoin d’être recréés).
3.  Les effets clonés peuvent partager des mémoires tampons constantes.
4.  Les effets clonés commencent par l’État qui correspond à l’effet actuel (valeurs des variables, qu’elles aient été optimisées ou non).

Pour plus d’informations, consultez [clonage d’un effet](d3d11-graphics-programming-guide-effects-cloning.md) .

## <a name="effect-pools-and-groups"></a>Pools et groupes d’effets

De loin, l’utilisation la plus répandue des pools d’effets dans Direct3D 10 consistait à regrouper les matériaux. Les pools d’effets ont été supprimés des effets 11 et les groupes ont été ajoutés, ce qui constitue une méthode plus efficace de regroupement de matériaux.

Un groupe d’effets est simplement un ensemble de techniques. Pour plus d’informations [, consultez Syntaxe du groupe Effect (Direct3D 11)](d3d11-effect-group-syntax.md) .

Considérez la hiérarchie d’effets suivante avec quatre effets enfants et un pool d’effets :


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



Vous pouvez obtenir la même fonctionnalité dans Effects 11 à l’aide de groupes :


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a>Nouvelles étapes de nuanceur

Il existe trois nouvelles étapes de nuanceur dans Direct3D 11 : le nuanceur de coque, le nuanceur de domaine et le nuanceur de calcul. Les effets 11 les traitent de la même façon que les nuanceurs de vertex, les nuanceurs de géométrie et les nuanceurs de pixels.

Trois nouveaux types de variables ont été ajoutés aux effets 11 :

-   HullShader
-   DomainShader
-   ComputeShader

Si vous utilisez ces nuanceurs dans une technique, vous devez étiqueter cette technique « technique11 », et non pas « technique10 ». Le nuanceur de calcul ne peut pas être défini dans le même test que les autres États graphiques (autres nuanceurs, blocs d’État ou cibles de rendu).

## <a name="new-texture-types"></a>Nouveaux types de texture

Direct3D 11 prend en charge les types de textures suivants :

-   [AppendStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [ByteAddressBuffer](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [ConsumeStructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [StructuredBuffer](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a>Vues d’accès non ordonnées

Effects 11 prend en charge l’obtention et la définition des nouveaux types de vues d’accès non ordonnés. Cela fonctionne de la même façon que les textures.

Considérez cet exemple HLSL :


```
  
RWTexture1D<float> myUAV;
```



Vous pouvez définir cette variable en C++ comme suit :


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



Direct3D 11 prend en charge les types de vues d’accès non triés suivants :

-   RWBuffer
-   RWByteAddressBuffer
-   RWStructuredBuffer
-   RWTexture1D
-   RWTexture1DArray
-   RWTexture2D
-   RWTexture2DArray
-   RWTexture3D

## <a name="interfaces-and-class-instances"></a>Interfaces et instances de classe

Pour connaître la syntaxe de la classe et de l’interface, consultez [interfaces et classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Pour utiliser des interfaces et des classes dans Effects, consultez [interfaces et classes dans Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).

## <a name="addressable-stream-out"></a>Flux adressable

Dans Direct3D 10, les nuanceurs de géométrie peuvent générer un flux de données vers l’unité de sortie de flux et l’unité de rastérisation. Dans Direct3D11, les nuanceurs de géométrie peuvent générer jusqu’à quatre flux de données vers l’unité de sortie de flux, et au plus l’un de ces flux vers l’unité de rastérisation. L’intrinsèque **ConstructGSWithSO** a été mis à jour pour refléter cette nouvelle fonctionnalité.

Pour plus d’informations, consultez [syntaxe de flux sortant](d3d11-graphics-reference-effect-streamout.md) .

## <a name="setting-and-unsetting-device-state"></a>Définition et désactivation de l’état de l’appareil

Dans Effects 10, vous pouviez rendre des mémoires tampons constantes et des mémoires tampons de texture gérées par l’utilisateur à l’aide des fonctions [**ID3D10EffectConstantBuffer :: SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) et [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) . Une fois que vous avez appelé ces fonctions, les effets 10 Runtime ne gèrent plus la mémoire tampon constante ou la mémoire tampon de texture et l’utilisateur doit remplir les données à l’aide de l’interface ID3D10Device.

Dans Effects 11, vous pouvez également faire en sorte que les blocs d’État (état de fusion, état du rastériseur, état du gabarit de profondeur et état de l’échantillonneur) soient gérés par l’utilisateur à l’aide des appels suivants :

-   [**ID3DX11EffectBlendVariable::SetBlendState**](id3dx11effectblendvariable-setblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::SetRasterizerState**](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::SetSampler**](id3dx11effectsamplervariable-setsampler.md)

Une fois que vous avez appelé ces fonctions, le runtime Effects 11 ne gère plus les variables de bloc d’État, et les valeurs resteront inchangées. Notez que dans la mesure où les blocs d’État sont immuables, l’utilisateur doit définir un nouveau bloc d’État pour modifier les valeurs.

Vous pouvez également rétablir les mémoires tampons constantes, les mémoires tampons de texture et les blocs d’État à l’état non géré par l’utilisateur. Si vous annulez ces variables, le runtime Effects 11 continuera à les mettre à jour si nécessaire. Vous pouvez utiliser les appels suivants pour annuler les variables gérées par l’utilisateur :

-   [**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [**ID3DX11EffectBlendVariable::UndoSetBlendState**](id3dx11effectblendvariable-undosetblendstate.md)
-   [**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [**ID3DX11EffectSamplerVariable::UndoSetSampler**](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a>Ordinateur virtuel Effects

La machine virtuelle Effects, qui a évalué des expressions complexes en dehors des fonctions, a été supprimée.

Les exemples suivants d’expressions complexes ne sont pas pris en charge :

1.  SetPixelShader (myPSArray (i \* 3 + j));
2.  SetPixelShader (myPSArray ((float) i);
3.  FILTRE = i + 2 ;

Les exemples suivants d’expressions non complexes sont pris en charge :

1.  SetPixelShader( myPS );
2.  SetPixelShader (myPS \[ i \] );
3.  SetPixelShader (myPS \[ uIndex \] );//uIndex est une variable uint
4.  FILTRE = i ;
5.  FILTRE = ANISOTROPE ;

Ces expressions peuvent apparaître dans des expressions de bloc d’État (par exemple, filtre) et des expressions de passe (par exemple, SetPixelShader).

## <a name="source-availability-and-location"></a>Disponibilité et emplacement de la source

Effects 10 a été distribué dans D3D10.dll. effects 11 est distribué en tant que source, avec les solutions de Visual Studio correspondantes pour le compiler. Lorsque vous créez des applications de type Effects, nous vous recommandons d’inclure la source Effects 11 directement dans ces applications.

Vous pouvez obtenir les effets 11 des [effets de la mise à jour de Direct3D 11](https://github.com/Microsoft/FX11).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 