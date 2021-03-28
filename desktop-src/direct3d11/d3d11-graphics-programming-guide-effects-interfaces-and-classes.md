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
# <a name="interfaces-and-classes-in-effects"></a><span data-ttu-id="b5750-103">Interfaces et classes dans Effects</span><span class="sxs-lookup"><span data-stu-id="b5750-103">Interfaces and Classes in Effects</span></span>

<span data-ttu-id="b5750-104">Il existe de nombreuses façons d’utiliser des classes et des interfaces dans Effects 11.</span><span class="sxs-lookup"><span data-stu-id="b5750-104">There are many ways to use classes and interfaces in Effects 11.</span></span> <span data-ttu-id="b5750-105">Pour connaître la syntaxe de la classe et de l’interface, consultez [interfaces et classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="b5750-105">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="b5750-106">Les sections suivantes détaillent comment spécifier des instances de classe à un nuanceur qui utilise des interfaces.</span><span class="sxs-lookup"><span data-stu-id="b5750-106">The following sections detail how to specify class instances to a shader which uses interfaces.</span></span> <span data-ttu-id="b5750-107">Nous allons utiliser l’interface et les classes suivantes dans les exemples :</span><span class="sxs-lookup"><span data-stu-id="b5750-107">We will use the following interface and classes in the examples:</span></span>


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



<span data-ttu-id="b5750-108">Notez que les instances d’interface peuvent être initialisées à des instances de classe.</span><span class="sxs-lookup"><span data-stu-id="b5750-108">Note that interface instances can be initialized to class instances.</span></span> <span data-ttu-id="b5750-109">Les tableaux d’instances de classe et d’interface sont également pris en charge et peuvent être initialisés comme dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="b5750-109">Arrays of class and interface instances are also supported and they can be initialized as in the following example:</span></span>


```
CRed pRedArray[2];
IColor pIColor3 = pRedArray[1];
IColor pIColorArray[2] = {pRed, pGreen};
IColor pIColorArray2[2] = pRedArray;
```



## <a name="uniform-interface-parameters"></a><span data-ttu-id="b5750-110">Paramètres d’interface uniformes</span><span class="sxs-lookup"><span data-stu-id="b5750-110">Uniform Interface Parameters</span></span>

<span data-ttu-id="b5750-111">Tout comme les autres types de données uniformes, les paramètres d’interface uniformes doivent être spécifiés dans l’appel CompileShader.</span><span class="sxs-lookup"><span data-stu-id="b5750-111">Just like other uniform data types, uniform interface parameters must be specified in the CompileShader call.</span></span> <span data-ttu-id="b5750-112">Les paramètres d’interface peuvent être assignés à des instances d’interface globales ou à des instances de classes globales.</span><span class="sxs-lookup"><span data-stu-id="b5750-112">Interface parameters can be assigned to global interface instances or global class instances.</span></span> <span data-ttu-id="b5750-113">Lorsqu’il est assigné à une instance d’interface globale, le nuanceur est dépendant de l’instance d’interface, ce qui signifie qu’il doit être défini sur une instance de classe.</span><span class="sxs-lookup"><span data-stu-id="b5750-113">When assigned to a global interface instance, the shader will have a dependency on the interface instance, which means that it must be set to a class instance.</span></span> <span data-ttu-id="b5750-114">Lorsqu’il est assigné à des instances de classe globales, le compilateur spécialise le nuanceur (comme avec d’autres types de données uniformes) pour utiliser cette classe.</span><span class="sxs-lookup"><span data-stu-id="b5750-114">When assigned to global class instances, the compiler specializes the shader (as with other uniform data types) to use that class.</span></span> <span data-ttu-id="b5750-115">Cela est important pour deux scénarios :</span><span class="sxs-lookup"><span data-stu-id="b5750-115">This is important for two scenarios:</span></span>

1.  <span data-ttu-id="b5750-116">Les nuanceurs avec une \_ cible 4 x peuvent utiliser des paramètres d’interface si ces paramètres sont uniformes et affectés à des instances de classes globales (donc aucune liaison dynamique n’est utilisée).</span><span class="sxs-lookup"><span data-stu-id="b5750-116">Shaders with a 4\_x target can use interface parameters if these parameters are uniform and assigned to global class instances (so no dynamic linkage is used).</span></span>
2.  <span data-ttu-id="b5750-117">Les utilisateurs peuvent décider d’avoir de nombreux nuanceurs spécialisés et compilés sans liaison dynamique ou peu de nuanceurs compilés avec une liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="b5750-117">Users can decide to have many compiled, specialized shaders with no dynamic linkage or few compiled shaders with dynamic linkage.</span></span>


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



<span data-ttu-id="b5750-118">Si pIColor2 reste inchangé par le biais de l’API, les deux passes précédentes sont fonctionnellement équivalentes, mais la première utilise un \_ \_ nuanceur statique PS 4 0, tandis que la seconde utilise un \_ \_ nuanceur PS 5 0 avec une liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="b5750-118">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent, but the first uses a ps\_4\_0 static shader while the second uses a ps\_5\_0 shader with dynamic linkage.</span></span> <span data-ttu-id="b5750-119">Si pIColor2 est modifié par le biais de l’API Effects (voir définition des instances de classe ci-dessous), le comportement du nuanceur de pixels de la deuxième passe peut changer.</span><span class="sxs-lookup"><span data-stu-id="b5750-119">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="non-uniform-interface-parameters"></a><span data-ttu-id="b5750-120">Paramètres d’interface non uniformes</span><span class="sxs-lookup"><span data-stu-id="b5750-120">Non-Uniform Interface Parameters</span></span>

<span data-ttu-id="b5750-121">Les paramètres d’interface non uniformes créent des dépendances d’interface pour les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="b5750-121">Non-uniform interface parameters create interface dependencies for the shaders.</span></span> <span data-ttu-id="b5750-122">Lors de l’application d’un nuanceur avec des paramètres d’interface, ces paramètres doivent être assignés dans avec l’appel BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="b5750-122">When applying a shader with interface parameters, these parameters must be assigned in with the BindInterfaces call.</span></span> <span data-ttu-id="b5750-123">Les instances d’interface globales et les instances de classe globales peuvent être spécifiées dans l’appel BindInterfaces.</span><span class="sxs-lookup"><span data-stu-id="b5750-123">Global interface instances and global class instances can be specified in the BindInterfaces call.</span></span>


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



<span data-ttu-id="b5750-124">Si pIColor2 reste inchangé par le biais de l’API, les deux passes précédentes sont fonctionnellement équivalentes et utilisent toutes les deux la liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="b5750-124">If pIColor2 remains unchanged through the API, then the previous two passes are functionally equivalent and both use dynamic linkage.</span></span> <span data-ttu-id="b5750-125">Si pIColor2 est modifié par le biais de l’API Effects (voir définition des instances de classe ci-dessous), le comportement du nuanceur de pixels de la deuxième passe peut changer.</span><span class="sxs-lookup"><span data-stu-id="b5750-125">If pIColor2 is changed through the effects API (see Setting Class Instances below), then the behavior of the pixel shader in the second pass may change.</span></span>

## <a name="setting-class-instances"></a><span data-ttu-id="b5750-126">Définition des instances de classe</span><span class="sxs-lookup"><span data-stu-id="b5750-126">Setting Class Instances</span></span>

<span data-ttu-id="b5750-127">Lors de la définition d’un nuanceur avec une liaison de nuanceur dynamique sur l’appareil Direct3D 11, les instances de classe doivent également être spécifiées.</span><span class="sxs-lookup"><span data-stu-id="b5750-127">When setting a shader with dynamic shader linkage to the Direct3D 11 device, class instances must also be specified.</span></span> <span data-ttu-id="b5750-128">La définition d’un nuanceur de ce type avec une instance de classe **null** est une erreur.</span><span class="sxs-lookup"><span data-stu-id="b5750-128">It is an error to set such a shader with a **NULL** class instance.</span></span> <span data-ttu-id="b5750-129">Par conséquent, toutes les instances d’interface auxquelles un nuanceur fait référence doivent avoir une instance de classe associée.</span><span class="sxs-lookup"><span data-stu-id="b5750-129">Therefore, all interface instances which a shader references must have an associated class instance.</span></span>

<span data-ttu-id="b5750-130">L’exemple suivant montre comment obtenir une variable d’instance de classe à partir d’un effet et la définir sur une variable d’interface :</span><span class="sxs-lookup"><span data-stu-id="b5750-130">The following example shows how to get a class instance variable from an effect and set it to an interface variable:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b5750-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b5750-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5750-132">Effets (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="b5750-132">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 