---
title: Interfaces et classes dans Effects
description: Il existe de nombreuses façons d’utiliser des classes et des interfaces dans Effects 11.
ms.assetid: 526d477b-fc1f-4bd0-a620-ce9b78147f68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b067b8e03b2d43ea44ccab6164424cbc84c7237
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382160"
---
# <a name="interfaces-and-classes-in-effects"></a>Interfaces et classes dans Effects

Il existe de nombreuses façons d’utiliser des classes et des interfaces dans Effects 11. Pour connaître la syntaxe de la classe et de l’interface, consultez [interfaces et classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).

Les sections suivantes détaillent comment spécifier des instances de classe à un nuanceur qui utilise des interfaces. Nous allons utiliser l’interface et les classes suivantes dans les exemples :


```
interface IColor
{
  float4 GetColor();
};

class CRed : IColor
{
  float4 GetColor() { return float4(1,0,0,1); }
};
class CGreen : IColor
{
  float4 GetColor() { return float4(0,1,0,1); }
};

CRed pRed;
CGreen pGreen;
IColor pIColor;
IColor pIColor2 = pRed;
```



Notez que les instances d’interface peuvent être initialisées à des instances de classe. Les tableaux d’instances de classe et d’interface sont également pris en charge et peuvent être initialisés comme dans l’exemple suivant :


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a>Paramètres d’interface uniformes

Tout comme les autres types de données uniformes, les paramètres d’interface uniformes doivent être spécifiés dans l’appel CompileShader. Les paramètres d’interface peuvent être assignés à des instances d’interface globales ou à des instances de classes globales. Lorsqu’il est assigné à une instance d’interface globale, le nuanceur est dépendant de l’instance d’interface, ce qui signifie qu’il doit être défini sur une instance de classe. Lorsqu’il est assigné à des instances de classe globales, le compilateur spécialise le nuanceur (comme avec d’autres types de données uniformes) pour utiliser cette classe. Cela est important pour deux scénarios :

1.  Les nuanceurs avec une \_ cible 4 x peuvent utiliser des paramètres d’interface si ces paramètres sont uniformes et affectés à des instances de classes globales (donc aucune liaison dynamique n’est utilisée).
2.  Les utilisateurs peuvent décider d’avoir de nombreux nuanceurs spécialisés et compilés sans liaison dynamique ou peu de nuanceurs compilés avec une liaison dynamique.


```
float4 PSUniform( uniform IColor color ) : SV_Target
{
  return color;
}

technique11
{
  pass
  {
    SetPixelShader( CompileShader( ps_4_0, PSUniform(pRed) ) );
  }
  pass
  {
    SetPixelShader( CompileShader( ps_5_0, PSUniform(pIColor2) ) );
  }
}
```



Si pIColor2 reste inchangé par le biais de l’API, les deux passes précédentes sont fonctionnellement équivalentes, mais la première utilise un \_ \_ nuanceur statique PS 4 0, tandis que la seconde utilise un \_ \_ nuanceur PS 5 0 avec une liaison dynamique. Si pIColor2 est modifié par le biais de l’API Effects (voir définition des instances de classe ci-dessous), le comportement du nuanceur de pixels de la deuxième passe peut changer.

## <a name="non-uniform-interface-parameters"></a>Paramètres d’interface non uniformes

Les paramètres d’interface non uniformes créent des dépendances d’interface pour les nuanceurs. Lors de l’application d’un nuanceur avec des paramètres d’interface, ces paramètres doivent être assignés dans avec l’appel BindInterfaces. Les instances d’interface globales et les instances de classe globales peuvent être spécifiées dans l’appel BindInterfaces.


```
float4 PSAbstract( IColor color ) : SV_Target
{
  return color;
}

PixelShader pPSAbstract = CompileShader( ps_5_0, PSAbstract(pRed) );

technique11
{
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pRed ) );
  }
  pass
  {
    SetPixelShader( BindInterfaces( pPSAbstract, pIColor2 ) );
  }
}
```



Si pIColor2 reste inchangé par le biais de l’API, les deux passes précédentes sont fonctionnellement équivalentes et utilisent toutes les deux la liaison dynamique. Si pIColor2 est modifié par le biais de l’API Effects (voir définition des instances de classe ci-dessous), le comportement du nuanceur de pixels de la deuxième passe peut changer.

## <a name="setting-class-instances"></a>Définition des instances de classe

Lors de la définition d’un nuanceur avec une liaison de nuanceur dynamique sur l’appareil Direct3D 11, les instances de classe doivent également être spécifiées. La définition d’un nuanceur de ce type avec une instance de classe **null** est une erreur. Par conséquent, toutes les instances d’interface auxquelles un nuanceur fait référence doivent avoir une instance de classe associée.

L’exemple suivant montre comment obtenir une variable d’instance de classe à partir d’un effet et la définir sur une variable d’interface :


```
ID3DX11EffectPass* pPass = pEffect->GetTechniqueByIndex(0)->GetPassByIndex(1);

ID3DX11EffectInterfaceVariable* pIface = pEffect->GetVariableByName( "pIColor2" )->AsInterface();
ID3DX11EffectClassInstanceVariable* pCI = pEffect->GetVariableByName( "pGreen" )->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );

// Apply the same pass with a different class instance
pCI = pEffect->GetVariableByName( "pRedArray" )->GetElement(1)->AsClassInstance();
pIface->SetClassInstance( pCI );
pPass->Apply( 0, pDeviceContext );
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Effets (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 