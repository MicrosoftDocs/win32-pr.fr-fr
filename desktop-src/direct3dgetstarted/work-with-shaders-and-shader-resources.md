---
title: Utiliser des nuanceurs et des ressources de nuanceur
description: Il est temps d’apprendre à utiliser des nuanceurs et des ressources de nuanceur dans le développement de votre jeu Microsoft DirectX pour Windows 8.
ms.assetid: 25a11983-e3f6-4bd3-86f1-d660edc4cd4b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ac147971221b04b02f2a45af8e8d4f6855a5e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382154"
---
# <a name="work-with-shaders-and-shader-resources"></a>Utiliser des nuanceurs et des ressources de nuanceur

Il est temps d’apprendre à utiliser des nuanceurs et des ressources de nuanceur dans le développement de votre jeu Microsoft DirectX pour Windows 8. Nous avons vu comment configurer le périphérique graphique et les ressources, et peut-être même avoir commencé à modifier son pipeline. Examinons maintenant les nuanceurs de pixels et vertex.

Si vous n’êtes pas familiarisé avec les langages de nuanceur, une discussion rapide est dans l’ordre. Les nuanceurs sont de petits programmes de bas niveau qui sont compilés et exécutés à des étapes spécifiques du pipeline Graphics. Leurs spécialisations sont des opérations mathématiques à virgule flottante très rapides. Les programmes nuanceurs les plus courants sont les suivants :

-   **Vertex shader**— exécuté pour chaque vertex d’une scène. Ce nuanceur opère sur les éléments de mémoire tampon de vertex qui lui sont fournis par l’application appelante, et produit au minimum un vecteur de position à 4 composants qui sera pixellisé en position de pixel.
-   **Nuanceur de pixels**: exécution pour chaque pixel dans une cible de rendu. Ce nuanceur reçoit les coordonnées pixellisées des précédentes étapes de nuanceur (dans les pipelines les plus simples, il s’agit du nuanceur de sommets) et retourne une couleur (ou une autre valeur de 4 composants) pour cette position de pixel, qui est ensuite écrite dans une cible de rendu.

Cet exemple comprend des nuanceurs de sommets et de pixels très basiques qui dessinent uniquement la géométrie et des nuanceurs plus complexes qui ajoutent des calculs d’éclairage de base.

Les programmes de nuanceur sont écrits en HLSL (High Level Shader Language). La syntaxe HLSL ressemble beaucoup à C, mais sans les pointeurs. Les programmes de nuanceur doivent être très compacts et efficaces. Si votre nuanceur est compilé en trop d’instructions, il ne peut pas être exécuté et une erreur est retournée. (Notez que le nombre exact d’instructions autorisées fait partie du [niveau de fonctionnalité Direct3D](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro).)

Dans Direct3D, les nuanceurs ne sont pas compilés au moment de l’exécution ; elles sont compilées lors de la compilation du reste du programme. Quand vous compilez votre application avec Microsoft Visual Studio 2013, les fichiers HLSL sont compilés en fichiers CSO (. CSO) que votre application doit charger et placer dans la mémoire GPU avant le dessin. Veillez à inclure ces fichiers CSO avec votre application lorsque vous l’Empaquetez ; Il s’agit de ressources, comme les maillages et les textures.

## <a name="understand-hlsl-semantics"></a>Comprendre la sémantique HLSL

Il est important de prendre un moment pour aborder la sémantique HLSL avant de continuer, car ils sont souvent un point de confusion pour les nouveaux développeurs Direct3D. La sémantique HLSL est une chaîne qui identifie une valeur transmise entre l’application et un programme Shader. Bien qu’il puisse s’agir de l’une des nombreuses chaînes possibles, il est recommandé d’utiliser une chaîne comme `POSITION` ou `COLOR` qui indique l’utilisation. Vous assignez ces sémantiques lorsque vous construisez une mémoire tampon constante ou une disposition d’entrée. Vous pouvez aussi ajouter un nombre compris entre 0 et 7 à la sémantique afin d’utiliser des registres séparés pour des valeurs similaires. Par exemple : COLOR0, COLOR1, COLOR2…

Les sémantiques précédées de « SV \_ » sont des sémantiques de *valeurs système* qui sont écrites par votre programme de nuanceur ; votre jeu (en cours d’exécution sur le processeur) ne peut pas les modifier. En règle générale, ces sémantiques contiennent des valeurs qui sont des entrées ou sorties d’une autre étape de nuanceur dans le pipeline graphique, ou qui sont entièrement générées par le GPU.

En outre, `SV_` la sémantique a des comportements différents lorsqu’ils sont utilisés pour spécifier une entrée ou une sortie à partir d’une étape de nuanceur. Par exemple, `SV_POSITION` (output) contient les données de vertex transformées pendant l’étape du nuanceur de sommets, et `SV_POSITION` (*Input*) contient les valeurs de position de pixel interpolées par le GPU pendant l’étape de pixellisation.

Voici quelques sémantiques HLSL courantes :

-   `POSITION`(*n*) pour les données de mémoire tampon de vertex. `SV_POSITION` fournit une position de pixel au nuanceur de pixels et ne peut pas être écrite par votre jeu.
-   `NORMAL`(*n*) pour les données normales fournies par la mémoire tampon de vertex.
-   `TEXCOORD`(*n*) pour les données de coordonnée UV de texture fournies à un nuanceur.
-   `COLOR`(n) pour les données de couleur RVBA fournies à un nuanceur. Notez qu’elle est traitée de la même façon pour coordonner les données, y compris l’interpolation de la valeur lors de la pixellisation. la sémantique vous aide simplement à identifier qu’il s’agit de données de couleur.
-   `SV_Target`\[n \] pour écrire à partir d’un nuanceur de pixels vers une texture cible ou une autre mémoire tampon de pixels.

Nous verrons des exemples de sémantique HLSL à mesure que nous examinerons l’exemple.

## <a name="read-from-the-constant-buffers"></a>Lire à partir des mémoires tampons constantes

Tout nuanceur peut lire à partir d’une mémoire tampon constante si ce tampon est attaché à son étape en tant que ressource. Dans cet exemple, seul le nuanceur vertex reçoit une mémoire tampon constante.

La mémoire tampon constante est déclarée à deux emplacements : dans le code C++, et dans les fichiers HLSL correspondants qui y accèdent.

Voici comment la structure de mémoire tampon constante est déclarée dans le code C++.


```C++
typedef struct _constantBufferStruct {
    DirectX::XMFLOAT4X4 world;
    DirectX::XMFLOAT4X4 view;
    DirectX::XMFLOAT4X4 projection;
} ConstantBufferStruct;
```



Lors de la déclaration de la structure pour la mémoire tampon constante dans votre code C++, assurez-vous que toutes les données sont correctement alignées sur des limites de 16 octets. Le moyen le plus simple consiste à utiliser des types [DirectXMath](/windows/desktop/dxmath/directxmath-portal) , comme **XMFLOAT4** ou **XMFLOAT4X4**, comme indiqué dans l’exemple de code. Vous pouvez également vous prémunir contre les mémoires tampons mal alignées en déclarant une assertion statique :


```C++
// Assert that the constant buffer remains 16-byte aligned.
static_assert((sizeof(ConstantBufferStruct) % 16) == 0, "Constant Buffer size must be 16-byte aligned");
```



Cette ligne de code génère une erreur au moment de la compilation si **ConstantBufferStruct** n’est pas aligné sur 16 octets. Pour plus d’informations sur l’alignement et la compression de la mémoire tampon constante, consultez [règles de compression pour les variables constantes](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-packing-rules).

Voici à présent comment la mémoire tampon constante est déclarée dans le nuanceur de vertex HLSL.


```C++
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix mWorld;      // world matrix for object
    matrix View;        // view matrix
    matrix Projection;  // projection matrix
};
```



Toutes les mémoires tampons (constante, texture, échantillonneur ou autre) doivent avoir un registre défini pour que le GPU puisse y accéder. Chaque étape de nuanceur autorise jusqu’à 15 mémoires tampons constantes, et chaque mémoire tampon peut contenir jusqu’à 4 096 variables constantes. La syntaxe de la déclaration d’utilisation des registres est la suivante :

-   **b * * *\#* : Registre pour une mémoire tampon constante (** CBuffer * *).
-   **t * * *\#* : Registre pour une mémoire tampon de texture (** tbuffer * *).
-   **s * \#** * : registre d’un échantillonneur. (Un échantillonneur définit le comportement de recherche des texels dans la ressource de texture.)

Par exemple, le HLSL pour un nuanceur de pixels peut prendre une texture et un échantillonneur comme entrée avec une déclaration comme celle-ci.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);
```

C’est à vous d’assigner des mémoires tampons constantes aux registres : lorsque vous configurez le pipeline, vous attachez une mémoire tampon constante au même emplacement que celui auquel vous l’avez attribuée dans le fichier HLSL. Par exemple, dans la rubrique précédente, l’appel à [**VSSetConstantBuffers**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetconstantbuffers) indique « 0 » pour le premier paramètre. Cela indique à Direct3D d’attacher la ressource de mémoire tampon constante pour inscrire 0, ce qui correspond à l’affectation de la mémoire tampon à **Register (B0)** dans le fichier HLSL.

## <a name="read-from-the-vertex-buffers"></a>Lire à partir des mémoires tampons de vertex

La mémoire tampon de vertex fournit les données de triangle pour les objets de scène aux nuanceurs de sommets. Comme avec la mémoire tampon constante, le struct de mémoire tampon de vertex est déclaré dans le code C++, à l’aide de règles de compression similaires.


```C++
typedef struct _vertexPositionColor
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 color;
} VertexPositionColor;
```



Il n’existe pas de format standard pour les données de vertex dans Direct3D 11. Au lieu de cela, nous définissons notre propre disposition des données de vertex à l’aide d’un descripteur. les champs de données sont définis à l’aide d’un tableau d' [**\_ éléments d’entrée d3d11 structures \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_input_element_desc) . Ici, nous affichons une disposition d’entrée simple qui décrit le même format de vertex que le struct précédent :


```C++
D3D11_INPUT_ELEMENT_DESC iaDesc [] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "COLOR", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayout
    );
```



Si vous ajoutez des données au format de vertex lorsque vous modifiez l’exemple de code, veillez à mettre à jour également la disposition d’entrée, sinon le nuanceur ne pourra pas l’interpréter. Vous pouvez modifier la disposition du vertex comme suit :


```C++
typedef struct _vertexPositionColorTangent
{
    DirectX::XMFLOAT3 pos;
    DirectX::XMFLOAT3 normal;
    DirectX::XMFLOAT3 tangent;
} VertexPositionColorTangent;
```



Dans ce cas, vous devez modifier la définition de la disposition d’entrée comme suit.


```C++
D3D11_INPUT_ELEMENT_DESC iaDescExtended[] =
{
    { "POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 0, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },

    { "TANGENT", 0, DXGI_FORMAT_R32G32B32_FLOAT,
    0, 12, D3D11_INPUT_PER_VERTEX_DATA, 0 },
};

hr = device->CreateInputLayout(
    iaDesc,
    ARRAYSIZE(iaDesc),
    bytes,
    bytesRead,
    &m_pInputLayoutExtended
    );
```



Chacune des définitions d’élément de disposition d’entrée est précédée d’une chaîne, telle que « POSITION » ou « normale », qui est la sémantique que nous avons abordée précédemment dans cette rubrique. C’est comme un handle qui aide le GPU à identifier cet élément lors du traitement du vertex. Choisissez des noms communs et explicites pour vos éléments vertex.

Tout comme avec la mémoire tampon constante, le nuanceur de sommets a une définition de tampon correspondante pour les éléments de vertex entrants. (C’est pourquoi nous avons fourni une référence à la ressource de nuanceur de vertex lors de la création de la disposition d’entrée-Direct3D valide la disposition des données par vertex avec le struct d’entrée du nuanceur.) Notez comment la sémantique correspond à la définition de la disposition d’entrée et à cette déclaration de tampon HLSL. Toutefois, `COLOR` a un « 0 » ajouté. Il n’est pas nécessaire d’ajouter le 0 si vous n’avez qu’un seul `COLOR` élément déclaré dans la disposition, mais il est recommandé de l’ajouter au cas où vous choisiriez d’ajouter d’autres éléments de couleur à l’avenir.


```C++
struct VS_INPUT
{
    float3 vPos   : POSITION;
    float3 vColor : COLOR0;
};
```



## <a name="pass-data-between-shaders"></a>Transmettre des données entre les nuanceurs

Les nuanceurs prennent des types d’entrée et retournent des types de sortie à partir de leurs fonctions principales lors de l’exécution. Pour le nuanceur de sommets défini dans la section précédente, le type d’entrée était la \_ structure d’entrée de Visual Studio et nous avons défini une disposition d’entrée correspondante et un struct C++. Un tableau de ce struct est utilisé pour créer une mémoire tampon de vertex dans la méthode **CreateCube** .

Le nuanceur vertex retourne une \_ structure d’entrée PS, qui doit contenir au minimum la position du vertex final à 4 composants (float4). Cette valeur de position doit avoir la sémantique de valeur système, `SV_POSITION` , déclarée pour celle-ci, afin que le GPU dispose des données dont il a besoin pour effectuer l’étape de dessin suivante. Notez qu’il n’y a pas de correspondance 1:1 entre la sortie du nuanceur de sommets et l’entrée de nuanceur de pixels ; le nuanceur vertex retourne une structure pour chaque vertex auquel il est donné, mais le nuanceur de pixels s’exécute une fois pour chaque pixel. Cela est dû au fait que les données par vertex passent d’abord par l’étape de pixellisation. Cette étape détermine les pixels qui « couvrent » la géométrie que vous dessinez, calcule les données interpolées par vertex pour chaque pixel, puis appelle le nuanceur de pixels une fois pour chacun de ces pixels. L’interpolation est le comportement par défaut lors de la pixellisation des valeurs de sortie et est essentielle en particulier pour le traitement correct des données de vecteur de sortie (vecteurs légers, normales et tangentes par vertex, etc.).


```C++
struct PS_INPUT
{
    float4 Position : SV_POSITION;  // interpolated vertex position (system value)
    float4 Color    : COLOR0;       // interpolated diffuse color
};
```



## <a name="review-the-vertex-shader"></a>Examiner le nuanceur de sommets

L’exemple de nuanceur vertex est très simple : prenez un vertex (position et couleur), transformez la position des coordonnées de modèle en coordonnées projetées de perspective, puis retournez-la (avec la couleur) au rastériseur. Notez que la valeur de couleur est interpolée avec les données de position, fournissant une valeur différente pour chaque pixel, même si le nuanceur vertex n’a pas effectué de calculs sur la valeur de couleur.


```C++
VS_OUTPUT main(VS_INPUT input) // main is the default function name
{
    VS_OUTPUT Output;

    float4 pos = float4(input.vPos, 1.0f);

    // Transform the position from object space to homogeneous projection space
    pos = mul(pos, mWorld);
    pos = mul(pos, View);
    pos = mul(pos, Projection);
    Output.Position = pos;

    // Just pass through the color data
    Output.Color = float4(input.vColor, 1.0f);

    return Output;
}
```



Un nuanceur de sommets plus complexe, comme celui qui configure les sommets d’un objet pour l’ombrage Phong, peut ressembler à ce qui suit. Dans ce cas, nous tirant parti du fait que les vecteurs et les normales sont interpolés pour se rapprocher d’une surface lisse.

``` syntax
// A constant buffer that stores the three basic column-major matrices for composing geometry.
cbuffer ModelViewProjectionConstantBuffer : register(b0)
{
    matrix model;
    matrix view;
    matrix projection;
};

cbuffer LightConstantBuffer : register(b1)
{
    float4 lightPos;
};

struct VertexShaderInput
{
    float3 pos : POSITION;
    float3 normal : NORMAL;
};

// Per-pixel color data passed through the pixel shader.

struct PixelShaderInput
{
    float4 position : SV_POSITION; 
    float3 outVec : POSITION0;
    float3 outNormal : NORMAL0;
    float3 outLightVec : POSITION1;
};

PixelShaderInput main(VertexShaderInput input)
{
    // Inefficient -- doing this only for instruction. Normally, you would
 // premultiply them on the CPU and place them in the cbuffer.
    matrix mvMatrix = mul(model, view);
    matrix mvpMatrix = mul(mvMatrix, projection);

    PixelShaderInput output;

    float4 pos = float4(input.pos, 1.0f);
    float4 normal = float4(input.normal, 1.0f);
    float4 light = float4(lightPos.xyz, 1.0f);

    // 
    float4 eye = float4(0.0f, 0.0f, -2.0f, 1.0f);

    // Transform the vertex position into projected space.
    output.gl_Position = mul(pos, mvpMatrix);
    output.outNormal = mul(normal, mvMatrix).xyz;
    output.outVec = -(eye - mul(pos, mvMatrix)).xyz;
    output.outLightVec = mul(light, mvMatrix).xyz;

    return output;
}
```

## <a name="review-the-pixel-shader"></a>Examiner le nuanceur de pixels

Ce nuanceur de pixels dans cet exemple est très probablement la quantité minimale absolue de code que vous pouvez avoir dans un nuanceur de pixels. Elle prend les données de couleur de pixel interpolées générées pendant la pixellisation et les retourne en sortie, où elles sont écrites dans une cible de rendu. Comment l’alésage !


```C++
PS_OUTPUT main(PS_INPUT In)
{
    PS_OUTPUT Output;

    Output.RGBColor = In.Color;

    return Output;
}
```



La partie importante est la `SV_TARGET` sémantique de valeur système sur la valeur de retour. Elle indique que la sortie doit être écrite dans la cible de rendu principale, qui est la mémoire tampon de texture fournie à la chaîne de permutation pour l’affichage. Cette opération est requise pour les nuanceurs de pixels : sans les données de couleur du nuanceur de pixels, Direct3D n’aurait rien à afficher !

Un exemple de nuanceur de pixels plus complexe pour effectuer un ombrage Phong peut ressembler à ceci. Étant donné que les vecteurs et les normales ont été interpolés, nous n’avons pas besoin de les calculer sur une base par pixel. Toutefois, nous devons les rénormaliser en raison du fonctionnement de l’interpolation. d’un point de vue conceptuel, nous devons progressivement « faire tourner » le vecteur de la direction du sommet A à la direction du sommet B, en conservant sa longueur (l’interpolation wheras est déplacée sur une ligne droite entre les deux points de terminaison vectoriels).

``` syntax
cbuffer MaterialConstantBuffer : register(b2)
{
    float4 lightColor;
    float4 Ka;
    float4 Kd;
    float4 Ks;
    float4 shininess;
};

struct PixelShaderInput
{
    float4 position : SV_POSITION;
    float3 outVec : POSITION0;
    float3 normal : NORMAL0;
    float3 light : POSITION1;
};

float4 main(PixelShaderInput input) : SV_TARGET
{
    float3 L = normalize(input.light);
    float3 V = normalize(input.outVec);
    float3 R = normalize(reflect(L, input.normal));

    float4 diffuse = Ka + (lightColor * Kd * max(dot(input.normal, L), 0.0f));
    diffuse = saturate(diffuse);

    float4 specular = Ks * pow(max(dot(R, V), 0.0f), shininess.x - 50.0f);
    specular = saturate(specular);

    float4 finalColor = diffuse + specular;

    return finalColor;
}
```

Dans un autre exemple, le nuanceur de pixels utilise ses propres mémoires tampons constantes qui contiennent des informations de lumière et de matériau. La disposition d’entrée dans le nuanceur vertex est développée de façon à inclure des données normales, et la sortie de ce nuanceur de vertex est supposée inclure les vecteurs transformés pour le vertex, la lumière et le vertex normal dans le système de coordonnées de la vue.

Si vous avez des tampons de texture et des échantillonneurs avec des registres affectés (**t** et **s**, respectivement), vous pouvez également y accéder dans le nuanceur de pixels.

``` syntax
Texture2D simpleTexture : register(t0);
SamplerState simpleSampler : register(s0);

struct PixelShaderInput
{
    float4 pos : SV_POSITION;
    float3 norm : NORMAL;
    float2 tex : TEXCOORD0;
};

float4 SimplePixelShader(PixelShaderInput input) : SV_TARGET
{
    float3 lightDirection = normalize(float3(1, -1, 0));
    float4 texelColor = simpleTexture.Sample(simpleSampler, input.tex);
    float lightMagnitude = 0.8f * saturate(dot(input.norm, -lightDirection)) + 0.2f;
    return texelColor * lightMagnitude;
}
```

Les nuanceurs sont des outils très puissants qui peuvent être utilisés pour générer des ressources procédurales telles que des clichés instantanés ou des textures de bruit. En fait, les techniques avancées requièrent que vous considériez les textures de manière plus abstraite, et non comme des éléments visuels, mais comme des tampons. Elles contiennent des données telles que des informations de hauteur, ou d’autres données qui peuvent être échantillonnées dans le test de nuanceur de pixels final ou dans ce frame particulier dans le cadre d’un passage à plusieurs étages. L’échantillonnage multiple est un outil puissant et l’épine dorsale de nombreux effets visuels modernes.

## <a name="next-steps"></a>Étapes suivantes

Nous espérons que vous êtes familiarisé avec DirectX 11at ce point et que vous êtes prêt à commencer à travailler sur votre projet. Voici quelques liens pour vous aider à répondre à d’autres questions que vous pouvez vous poser concernant le développement avec DirectX et C++ :

-   [Développement de jeux](/previous-versions/windows/apps/hh452744(v=win.10))
-   [Utiliser Visual Studio Tools pour la programmation de jeux DirectX](/previous-versions/windows/apps/dn166877(v=win.10))
-   [Développement de jeux DirectX et exemples de procédures pas à pas](/previous-versions/windows/apps/hh465149(v=win.10))
-   [Ressources supplémentaires pour la programmation de jeux](/previous-versions/windows/apps/dn194515(v=win.10))

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utiliser les ressources de l’appareil DirectX](work-with-dxgi.md)
</dt> <dt>

[Comprendre le pipeline de rendu Direct3D 11](understand-the-directx-11-2-graphics-pipeline.md)
</dt> </dl>

 

 