---
title: Interfaces et classes
description: La liaison de nuanceur dynamique utilise des classes et des interfaces de nuanceur de niveau supérieur (HLSL) qui sont syntaxiquement similaires à leurs équivalents C++.
ms.assetid: 124a358d-30ab-4efe-88ed-1ff277d17b25
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 71410caf7d80cb9dbcd0165c753d75cc8f5cbe00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382391"
---
# <a name="interfaces-and-classes"></a><span data-ttu-id="f5f2f-103">Interfaces et classes</span><span class="sxs-lookup"><span data-stu-id="f5f2f-103">Interfaces and classes</span></span>

<span data-ttu-id="f5f2f-104">La liaison de nuanceur dynamique utilise des classes et des interfaces de nuanceur de niveau supérieur (HLSL) qui sont syntaxiquement similaires à leurs équivalents C++.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-104">Dynamic shader linkage makes use of high-level shader language (HLSL) interfaces and classes that are syntactically similar to their C++ counterparts.</span></span> <span data-ttu-id="f5f2f-105">Cela permet aux nuanceurs de référencer des instances d’interface abstraites au moment de la compilation et de conserver la résolution de ces instances sur des classes concrètes pour l’application au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-105">This allows shaders to reference abstract interface instances at compile time and leave resolution of those instances to concrete classes for the application at runtime.</span></span>

<span data-ttu-id="f5f2f-106">Les sections suivantes détaillent comment configurer un nuanceur pour utiliser des interfaces et des classes et comment initialiser des instances d’interface dans le code d’application.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-106">The following sections detail how to setup a shader to use interfaces and classes and how to initialize interface instances in application code.</span></span>

-   [<span data-ttu-id="f5f2f-107">Déclaration des interfaces</span><span class="sxs-lookup"><span data-stu-id="f5f2f-107">Declaring Interfaces</span></span>](#declaring-interfaces)
-   [<span data-ttu-id="f5f2f-108">Déclaration de classes</span><span class="sxs-lookup"><span data-stu-id="f5f2f-108">Declaring Classes</span></span>](#declaring-classes)
-   [<span data-ttu-id="f5f2f-109">Déclarations d’instance d’interface dans un nuanceur</span><span class="sxs-lookup"><span data-stu-id="f5f2f-109">Interface Instance Declarations in a Shader</span></span>](#interface-instance-declarations-in-a-shader)
-   [<span data-ttu-id="f5f2f-110">Déclarations d’instance de classe dans un nuanceur</span><span class="sxs-lookup"><span data-stu-id="f5f2f-110">Class Instance Declarations in a Shader</span></span>](#class-instance-declarations-in-a-shader)
-   [<span data-ttu-id="f5f2f-111">Initialisation des instances d’interface dans une application</span><span class="sxs-lookup"><span data-stu-id="f5f2f-111">Initializing Interface Instances in an Application</span></span>](#initializing-interface-instances-in-an-application)
-   [<span data-ttu-id="f5f2f-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5f2f-112">Related topics</span></span>](#related-topics)

## <a name="declaring-interfaces"></a><span data-ttu-id="f5f2f-113">Déclarer des interfaces</span><span class="sxs-lookup"><span data-stu-id="f5f2f-113">Declaring interfaces</span></span>

<span data-ttu-id="f5f2f-114">Une interface fonctionne de façon similaire à une classe de base abstraite en C++.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-114">An interface functions in a similar manner to an abstract base class in C++.</span></span> <span data-ttu-id="f5f2f-115">Une interface est déclarée dans un nuanceur à l’aide du mot clé interface et contient uniquement des déclarations de méthode.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-115">An interface is declared in a shader using the interface keyword and only contains method declarations.</span></span> <span data-ttu-id="f5f2f-116">Les méthodes déclarées dans une interface seront toutes des méthodes virtuelles dans toutes les classes dérivées de l’interface.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-116">The methods declared in an interface will all be virtual methods in any classes derived from the interface.</span></span> <span data-ttu-id="f5f2f-117">Les classes dérivées doivent implémenter toutes les méthodes déclarées dans une interface.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-117">Derived classes must implement all methods declared in an interface.</span></span> <span data-ttu-id="f5f2f-118">Notez que les interfaces sont la seule façon de déclarer des méthodes virtuelles, il n’existe pas de mot clé virtuel en C++, et les classes connot déclarent des méthodes virtuelles.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-118">Note that interfaces are the only way to declare virtual methods, there is no virtual keyword as in C++, and classes connot declare virtual methods.</span></span>

<span data-ttu-id="f5f2f-119">L’exemple de code de nuanceur suivant déclare deux interfaces.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-119">The following example shader code declares two interfaces.</span></span>


```
interface iBaseLight
{
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};       

interface iBaseMaterial
{
   float3 GetAmbientColor(float2 vTexcoord);
   
   float3 GetDiffuseColor(float2 vTexcoord);

   int GetSpecularPower();

};
      
```



## <a name="declaring-classes"></a><span data-ttu-id="f5f2f-120">Déclaration de classes</span><span class="sxs-lookup"><span data-stu-id="f5f2f-120">Declaring Classes</span></span>

<span data-ttu-id="f5f2f-121">Une classe se comporte de la même façon que les classes en C++.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-121">A class behaves in a similar manner to classes in C++.</span></span> <span data-ttu-id="f5f2f-122">Une classe est déclarée avec le mot clé class et peut contenir des variables et des méthodes membres.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-122">A class is declared with the class keyword and can contain member variables and methods.</span></span> <span data-ttu-id="f5f2f-123">Une classe peut hériter de zéro ou d’une classe et de zéro ou plusieurs interfaces.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-123">A class can inherit from zero or one class and zero or more interfaces.</span></span> <span data-ttu-id="f5f2f-124">Les classes doivent implémenter ou hériter des implémentations pour toutes les interfaces dans sa chaîne d’héritage ou la classe ne peut pas être instanciée.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-124">Classes must implement or inherit implementations for all interfaces in its inheritance chain or the class cannot be instantiated.</span></span>

<span data-ttu-id="f5f2f-125">L’exemple de code de nuanceur suivant illustre la dérivation d’une classe à partir d’une interface et d’une autre classe.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-125">The following example shader code illustrates deriving a class from an interface and from another class.</span></span>


```
class cAmbientLight : iBaseLight
{
   float3            m_vLightColor;     
   bool     m_bEnable;
   float3 IlluminateAmbient(float3 vNormal);
   float3 IlluminateDiffuse(float3 vNormal);
   float3 IlluminateSpecular(float3 vNormal, int specularPower );
};

class cHemiAmbientLight : cAmbientLight
{
   float4   m_vGroundColor;
   float4   m_vDirUp;
   float3 IlluminateAmbient(float3 vNormal);
};        
      
```



## <a name="interface-instance-declarations-in-a-shader"></a><span data-ttu-id="f5f2f-126">Déclarations d’instance d’interface dans un nuanceur</span><span class="sxs-lookup"><span data-stu-id="f5f2f-126">Interface Instance Declarations in a Shader</span></span>

<span data-ttu-id="f5f2f-127">Une instance d’interface agit comme un espace réservé pour les instances de classe qui fournissent une implémentation des méthodes de l’interface.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-127">An interface instance acts as a place holder for class instances that provide an implementation of the interface's methods.</span></span> <span data-ttu-id="f5f2f-128">L’utilisation d’une instance d’une interface permet au code du nuanceur d’appeler une méthode sans savoir quelle implémentation de cette méthode sera appelée.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-128">Using an instance of an interface allows shader code to call a method without knowing which implementation of that method will be invoked.</span></span> <span data-ttu-id="f5f2f-129">Le code du nuanceur déclare une ou plusieurs instances pour chaque interface qu’il définit.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-129">Shader code declares one or more instances for each interface it defines.</span></span> <span data-ttu-id="f5f2f-130">Ces instances sont utilisées dans le code du nuanceur de la même façon que les pointeurs de classe de base C++.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-130">These instances are used in shader code in a similar manner to C++ base class pointers.</span></span>

<span data-ttu-id="f5f2f-131">L’exemple de code de nuanceur suivant illustre la déclaration de plusieurs instances d’interface et leur utilisation dans le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-131">The following example shader code illustrates declaring several interface instances and using them in shader code.</span></span>


```
// Declare interface instances
iBaseLight     g_abstractAmbientLighting;
iBaseLight     g_abstractDirectLighting;
iBaseMaterial  g_abstractMaterial;

struct PS_INPUT
{
    float4 vPosition : SV_POSITION;
    float3 vNormal   : NORMAL;
    float2 vTexcoord : TEXCOORD0;
};

float4 PSMain( PS_INPUT Input ) : SV_TARGET
{ 
    float3 Ambient = (float3)0.0f;       
    Ambient = g_abstractMaterial.GetAmbientColor( Input.vTexcoord ) *         
        g_abstractAmbientLighting.IlluminateAmbient( Input.vNormal );

    float3 Diffuse = (float3)0.0f;  
    Diffuse += g_abstractMaterial.GetDiffuseColor( Input.vTexcoord ) * 
        g_abstractDirectLighting.IlluminateDiffuse( Input.vNormal );

    float3 Specular = (float3)0.0f;   
    Specular += g_abstractDirectLighting.IlluminateSpecular( Input.vNormal, 
        g_abstractMaterial.GetSpecularPower() );
     
    float3 Lighting = saturate( Ambient + Diffuse + Specular );
     
    return float4(Lighting,1.0f); 
}
```



## <a name="class-instance-declarations-in-a-shader"></a><span data-ttu-id="f5f2f-132">Déclarations d’instance de classe dans un nuanceur</span><span class="sxs-lookup"><span data-stu-id="f5f2f-132">Class Instance Declarations in a Shader</span></span>

<span data-ttu-id="f5f2f-133">Chaque classe qui sera utilisée à la place d’une instance d’interface doit être déclarée en tant que variable dans une mémoire tampon constante ou créée par l’application au moment de l’exécution à l’aide de la méthode [**ID3D11ClassLinkage :: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) .</span><span class="sxs-lookup"><span data-stu-id="f5f2f-133">Each class that will be used in place of an interface instance must either be declared as a variable in a constant buffer or created by the application at runtime using the [**ID3D11ClassLinkage::CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) method.</span></span> <span data-ttu-id="f5f2f-134">Les instances d’interface seront pointées sur les instances de classe dans le code de l’application.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-134">Interface instances will be pointed at class instances in the application code.</span></span> <span data-ttu-id="f5f2f-135">Les instances de classe peuvent être référencées dans le code du nuanceur comme toute autre variable, mais une classe dérivée d’une interface est généralement utilisée uniquement avec une instance d’interface et n’est pas référencée directement par le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-135">Class instances can be referenced in shader code like any other variable, but a class that is derived from an interface will typically only be used with an interface instance and will not be referenced by shader code directly.</span></span>

<span data-ttu-id="f5f2f-136">L’exemple de code de nuanceur suivant illustre la déclaration de plusieurs instances de classe.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-136">The following example shader code illustrates declaring several class instances.</span></span>


```
cbuffer cbPerFrame : register( b0 )
{
   cAmbientLight     g_ambientLight;
   cHemiAmbientLight g_hemiAmbientLight;
   cDirectionalLight g_directionalLight;
   cEnvironmentLight g_environmentLight;
   float4            g_vEyeDir;   
};        
      
```



## <a name="initializing-interface-instances-in-an-application"></a><span data-ttu-id="f5f2f-137">Initialisation des instances d’interface dans une application</span><span class="sxs-lookup"><span data-stu-id="f5f2f-137">Initializing Interface Instances in an Application</span></span>

<span data-ttu-id="f5f2f-138">Les instances d’interface sont initialisées dans le code de l’application en transmettant un tableau de liaison dynamique contenant des assignations d’interface à l’une des méthodes [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-138">Interface instances are initialized in application code by passing a dynamic linkage array containing interface assignments to one of the [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader methods.</span></span>

<span data-ttu-id="f5f2f-139">Pour créer un tableau de liaison dynamique, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="f5f2f-139">To create a dynamic linkage array use the following steps</span></span>

1.  <span data-ttu-id="f5f2f-140">Créez un objet de liaison de classe à l’aide de [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span><span class="sxs-lookup"><span data-stu-id="f5f2f-140">Create a class linkage object using [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).</span></span>
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  <span data-ttu-id="f5f2f-141">Créez le nuanceur qui utilisera la liaison de classe dynamique, en transmettant l’objet de liaison de classe en tant que paramètre à la fonction Create du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-141">Create the shader that will be using dynamic class linking, passing the class linkage object as a parameter to the shader's create function.</span></span>
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  <span data-ttu-id="f5f2f-142">Créez un objet [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) à l’aide de la fonction [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .</span><span class="sxs-lookup"><span data-stu-id="f5f2f-142">Create a [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) object using the [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) function.</span></span>
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  <span data-ttu-id="f5f2f-143">Utilisez l’objet de réflexion du nuanceur pour récupérer le nombre d’instances d’interface dans le nuanceur à l’aide de la méthode [**ID3D11ShaderReflection :: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .</span><span class="sxs-lookup"><span data-stu-id="f5f2f-143">Use the shader reflection object to get the number of interface instances in the shader using the [**ID3D11ShaderReflection::GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) method.</span></span>
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  <span data-ttu-id="f5f2f-144">Créez un tableau suffisamment grand pour contenir le nombre d’instances d’interface dans le nuanceur.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-144">Create an array large enough to hold the number of interface instances in the shader.</span></span>
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  <span data-ttu-id="f5f2f-145">Déterminez l’index dans le tableau qui correspond à chaque instance d’interface à l’aide de [**ID3D11ShaderReflection :: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) et [**ID3D11ShaderReflectionVariable :: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span><span class="sxs-lookup"><span data-stu-id="f5f2f-145">Determine the index in the array that corresponds to each interface instance using [**ID3D11ShaderReflection::GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) and [**ID3D11ShaderReflectionVariable::GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).</span></span>
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  <span data-ttu-id="f5f2f-146">Obtenir une instance de classe pour chaque objet de classe dérivé d’une interface dans le nuanceur à l’aide de [**ID3D11ClassLinkage :: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span><span class="sxs-lookup"><span data-stu-id="f5f2f-146">Get a class instance for each class object derived from an interface in the shader using [**ID3D11ClassLinkage::GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).</span></span>
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  <span data-ttu-id="f5f2f-147">Définissez les instances d’interface sur des instances de classe en définissant l’entrée correspondante dans le tableau de liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-147">Set interface instances to class instances by setting the corresponding entry in the dynamic linkage array.</span></span>
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  <span data-ttu-id="f5f2f-148">Transmettez le tableau de liaison dynamique en tant que paramètre à un appel SetShader.</span><span class="sxs-lookup"><span data-stu-id="f5f2f-148">Pass the dynamic linkage array as a parameter to a SetShader call.</span></span>
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a><span data-ttu-id="f5f2f-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5f2f-149">Related topics</span></span>

[<span data-ttu-id="f5f2f-150">Liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="f5f2f-150">Dynamic Linking</span></span>](overviews-direct3d-11-hlsl-dynamic-linking.md)