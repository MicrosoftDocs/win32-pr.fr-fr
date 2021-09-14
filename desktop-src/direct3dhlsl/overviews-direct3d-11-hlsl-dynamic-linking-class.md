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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915292"
---
# <a name="interfaces-and-classes"></a>Interfaces et classes

La liaison de nuanceur dynamique utilise des classes et des interfaces de nuanceur de niveau supérieur (HLSL) qui sont syntaxiquement similaires à leurs équivalents C++. Cela permet aux nuanceurs de référencer des instances d’interface abstraites au moment de la compilation et de conserver la résolution de ces instances sur des classes concrètes pour l’application au moment de l’exécution.

Les sections suivantes détaillent comment configurer un nuanceur pour utiliser des interfaces et des classes et comment initialiser des instances d’interface dans le code d’application.

-   [Déclaration des interfaces](#declaring-interfaces)
-   [Déclaration de classes](#declaring-classes)
-   [Déclarations d’instance d’interface dans un nuanceur](#interface-instance-declarations-in-a-shader)
-   [Déclarations d’instance de classe dans un nuanceur](#class-instance-declarations-in-a-shader)
-   [Initialisation des instances d’interface dans une application](#initializing-interface-instances-in-an-application)
-   [Rubriques connexes](#related-topics)

## <a name="declaring-interfaces"></a>Déclarer des interfaces

Une interface fonctionne de façon similaire à une classe de base abstraite en C++. Une interface est déclarée dans un nuanceur à l’aide du mot clé interface et contient uniquement des déclarations de méthode. Les méthodes déclarées dans une interface seront toutes des méthodes virtuelles dans toutes les classes dérivées de l’interface. Les classes dérivées doivent implémenter toutes les méthodes déclarées dans une interface. Notez que les interfaces sont la seule façon de déclarer des méthodes virtuelles, il n’existe pas de mot clé virtuel en C++, et les classes connot déclarent des méthodes virtuelles.

L’exemple de code de nuanceur suivant déclare deux interfaces.


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



## <a name="declaring-classes"></a>Déclaration de classes

Une classe se comporte de la même façon que les classes en C++. Une classe est déclarée avec le mot clé class et peut contenir des variables et des méthodes membres. Une classe peut hériter de zéro ou d’une classe et de zéro ou plusieurs interfaces. Les classes doivent implémenter ou hériter des implémentations pour toutes les interfaces dans sa chaîne d’héritage ou la classe ne peut pas être instanciée.

L’exemple de code de nuanceur suivant illustre la dérivation d’une classe à partir d’une interface et d’une autre classe.


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



## <a name="interface-instance-declarations-in-a-shader"></a>Déclarations d’instance d’interface dans un nuanceur

Une instance d’interface agit comme un espace réservé pour les instances de classe qui fournissent une implémentation des méthodes de l’interface. L’utilisation d’une instance d’une interface permet au code du nuanceur d’appeler une méthode sans savoir quelle implémentation de cette méthode sera appelée. Le code du nuanceur déclare une ou plusieurs instances pour chaque interface qu’il définit. Ces instances sont utilisées dans le code du nuanceur de la même façon que les pointeurs de classe de base C++.

L’exemple de code de nuanceur suivant illustre la déclaration de plusieurs instances d’interface et leur utilisation dans le code du nuanceur.


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



## <a name="class-instance-declarations-in-a-shader"></a>Déclarations d’instance de classe dans un nuanceur

Chaque classe qui sera utilisée à la place d’une instance d’interface doit être déclarée en tant que variable dans une mémoire tampon constante ou créée par l’application au moment de l’exécution à l’aide de la méthode [**ID3D11ClassLinkage :: CreateClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-createclassinstance) . Les instances d’interface seront pointées sur les instances de classe dans le code de l’application. Les instances de classe peuvent être référencées dans le code du nuanceur comme toute autre variable, mais une classe dérivée d’une interface est généralement utilisée uniquement avec une instance d’interface et n’est pas référencée directement par le code du nuanceur.

L’exemple de code de nuanceur suivant illustre la déclaration de plusieurs instances de classe.


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



## <a name="initializing-interface-instances-in-an-application"></a>Initialisation des instances d’interface dans une application

Les instances d’interface sont initialisées dans le code de l’application en transmettant un tableau de liaison dynamique contenant des assignations d’interface à l’une des méthodes [**ID3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext) SetShader.

Pour créer un tableau de liaison dynamique, procédez comme suit :

1.  Créez un objet de liaison de classe à l’aide de [**CreateClassLinkage**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createclasslinkage).
    ```
    ID3D11ClassLinkage* g_pPSClassLinkage = NULL;            
    pd3dDevice->CreateClassLinkage( &g_pPSClassLinkage );
              
    ```

    

2.  Créez le nuanceur qui utilisera la liaison de classe dynamique, en transmettant l’objet de liaison de classe en tant que paramètre à la fonction Create du nuanceur.
    ```
    pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
        pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader ) );            
              
    ```

    

3.  Créez un objet [**ID3D11ShaderReflection**](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11shaderreflection) à l’aide de la fonction [**D3DReflect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect) .
    ```
    ID3D11ShaderReflection* pReflector = NULL; 
    D3DReflect( pPixelShaderBuffer->GetBufferPointer(),                  
        pPixelShaderBuffer->GetBufferSize(), 
        IID_ID3D11ShaderReflection, (void**) &pReflector) );            
              
    ```

    

4.  Utilisez l’objet de réflexion du nuanceur pour récupérer le nombre d’instances d’interface dans le nuanceur à l’aide de la méthode [**ID3D11ShaderReflection :: GetNumInterfaceSlots**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getnuminterfaceslots) .
    ```
    g_iNumPSInterfaces = pReflector->GetNumInterfaceSlots();             
              
    ```

    

5.  Créez un tableau suffisamment grand pour contenir le nombre d’instances d’interface dans le nuanceur.
    ```
    ID3D11ClassInstance** g_dynamicLinkageArray = NULL;            
    g_dynamicLinkageArray = 
        (ID3D11ClassInstance**) malloc( sizeof(ID3D11ClassInstance*) * g_iNumPSInterfaces );            
              
    ```

    

6.  Déterminez l’index dans le tableau qui correspond à chaque instance d’interface à l’aide de [**ID3D11ShaderReflection :: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) et [**ID3D11ShaderReflectionVariable :: GetInterfaceSlot**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getinterfaceslot).
    ```
    ID3D11ShaderReflectionVariable* pAmbientLightingVar = 
        pReflector->GetVariableByName("g_abstractAmbientLighting");
        g_iAmbientLightingOffset = pAmbientLightingVar->GetInterfaceSlot(0);            
              
    ```

    

7.  Obtenir une instance de classe pour chaque objet de classe dérivé d’une interface dans le nuanceur à l’aide de [**ID3D11ClassLinkage :: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance).
    ```
    g_pPSClassLinkage->GetClassInstance( "g_hemiAmbientLight", 0, 
        &g_pHemiAmbientLightClass );            
              
    ```

    

8.  Définissez les instances d’interface sur des instances de classe en définissant l’entrée correspondante dans le tableau de liaison dynamique.
    ```
    g_dynamicLinkageArray[g_iAmbientLightingOffset] = g_pHemiAmbientLightClass;            
              
    ```

    

9.  Transmettez le tableau de liaison dynamique en tant que paramètre à un appel SetShader.
    ```
    pd3dImmediateContext->PSSetShader( g_pPixelShader, g_dynamicLinkageArray, g_iNumPSInterfaces );            
              
    ```

    

## <a name="related-topics"></a>Rubriques connexes

[Liaison dynamique](overviews-direct3d-11-hlsl-dynamic-linking.md)