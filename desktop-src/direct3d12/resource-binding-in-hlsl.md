---
title: Liaison de ressources en HLSL
description: Cette rubrique décrit certaines fonctionnalités spécifiques à l’utilisation du modèle de nuanceur HLSL (High Level Shader Language) 5,1 avec Direct3D 12.
ms.assetid: 3CD4BDAD-8AE3-4DE0-B3F8-9C9F9E83BBE9
ms.localizationpriority: high
ms.topic: article
ms.date: 08/27/2019
ms.openlocfilehash: 749fed319f9ffe840f2b06512e337efa28081e24
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548566"
---
# <a name="resource-binding-in-hlsl"></a>Liaison de ressources en HLSL

Cette rubrique décrit certaines fonctionnalités spécifiques à l’utilisation du [modèle de nuanceur](/windows/desktop/direct3dhlsl/shader-model-5-1) HLSL (High Level Shader Language) 5,1 avec Direct3D 12. Tout le matériel Direct3D 12 prend en charge le modèle de nuanceur 5,1. par conséquent, la prise en charge de ce modèle ne dépend pas du niveau de fonctionnalité matérielle.

-   [Types de ressources et tableaux](#resource-types-and-arrays)
-   [Tableaux de descripteurs et tableaux de texture](#descriptor-arrays-and-texture-arrays)
-   [Alias des ressources](#resource-aliasing)
-   [Divergence et dérivées](#divergence-and-derivatives)
-   [UAVs dans les nuanceurs de pixels](#uavs-in-pixel-shaders)
-   [Mémoires tampons constantes](#constant-buffers)
-   [Changements de bytecode dans SM 5.1](#bytecode-changes-in-sm51)
-   [Exemples de déclarations HLSL](#example-hlsl-declarations)
-   [Rubriques connexes](#related-topics)

## <a name="resource-types-and-arrays"></a>Types de ressources et tableaux

La syntaxe de ressource Shader Model 5 (SM 5.0) utilise le `register` mot clé pour transmettre les informations importantes sur la ressource au compilateur HLSL. Par exemple, l’instruction suivante déclare un tableau de quatre textures liées aux emplacements T3, T4, T5 et T6. T3 est le seul emplacement de Registre qui s’affiche dans l’instruction, qui est simplement le premier dans le tableau de quatre.

``` syntax
Texture2D<float4> tex1[4] : register(t3)
```

La syntaxe de ressource du Shader Model 5,1 (SM 5.1) en langage HLSL est basée sur la syntaxe de ressource de Registre existante, pour faciliter le portage. Les ressources Direct3D 12 en HLSL sont liées à des registres virtuels au sein d’espaces de registres logiques :

-   t – pour les vues des ressources de nuanceur (SRV)
-   s : pour les échantillonneurs
-   u : pour les vues d’accès non ordonnées (UAV)
-   b – pour les vues de mémoire tampon constantes (CBV)

La signature racine faisant référence au nuanceur doit être compatible avec les emplacements de Registre déclarés. Par exemple, la partie suivante d’une signature racine est compatible avec l’utilisation d’emplacements de texture T3 à T6, car elle décrit une table de descripteur avec les emplacements T0 à T98.

``` syntax
DescriptorTable( CBV(b1), SRV(t0,numDescriptors=99), CBV(b2) )
```

Une déclaration de ressource peut être un scalaire, un tableau 1D ou un tableau multidimensionnel :

``` syntax
Texture2D<float4> tex1 : register(t3,  space0)
Texture2D<float4> tex2[4] : register(t10)
Texture2D<float4> tex3[7][5][3] : register(t20, space1)
```

SM 5.1 utilise les mêmes types de ressource et types d’éléments que le SM 5.0. Les limites de déclaration de SM 5.1 sont plus flexibles et limitées uniquement par les limites de Runtime/matériel. Le `space` mot clé spécifie l’espace de Registre logique auquel la variable déclarée est liée. Si le `space` mot clé est omis, l’index d’espace par défaut 0 est implicitement affecté à la plage (la `tex2` plage ci-dessus réside dans `space0` ). `register(t3,  space0)` n’est jamais en conflit avec `register(t3,  space1)` , ni avec un tableau dans un autre espace qui peut inclure T3.

Une ressource de tableau peut avoir une taille illimitée, qui est déclarée en spécifiant que la toute première dimension doit être vide, ou 0 :

``` syntax
Texture2D<float4> tex1[] : register(t0)
```

La table de descripteurs correspondante peut être :

``` syntax
DescriptorTable( CBV(b1), UAV(u0, numDescriptors = 4), SRV(t0, numDescriptors=unbounded)
```

Un tableau non lié en HLSL ne correspond pas à un nombre fixe défini avec `numDescriptors` dans la table du descripteur, et une taille fixe dans le langage HLSL correspond à une déclaration non liée dans la table du descripteur.

Les tableaux multidimensionnels sont autorisés, y compris une taille illimitée. Ces tableaux multidimensionnels sont aplatis dans l’espace de registre.

``` syntax
Texture2D<float4> tex2[3000][10] : register(t0, space0); // t0-t29999 in space0
Texture2D<float4> tex3[0][5][3] : register(t5, space1)
```

L’alias des plages de ressources n’est pas autorisé. En d’autres termes, pour chaque type de ressource (t, s, u, b), les plages de registres déclarées ne doit pas se chevauchent. Cela comprend également les plages non liées. Les plages déclarées dans des espaces de registres différents ne se chevauchent jamais. Notez que le non lié `tex2` (ci-dessus) réside dans `space0` , tandis que le non lié `tex3` réside dans `space1` , de sorte qu’ils ne se chevauchent pas.

L’accès aux ressources qui ont été déclarées en tant que tableaux est aussi simple que l’indexation.

``` syntax
Texture2D<float4> tex1[400] : register(t3);
sampler samp[7] : register(s0);
tex1[myMaterialID].Sample(samp[samplerID], texCoords);
```

Il existe une restriction par défaut importante sur l’utilisation des index ( `myMaterialID` et `samplerID` dans le code ci-dessus) en ce sens qu’ils ne sont pas autorisés à varier au sein d’une [vague](../direct3dhlsl/hlsl-shader-model-6-0-features-for-direct3d-12.md#terminology). Même la modification de l’index en fonction du nombre d’instanciations est variable.

Si vous devez faire varier l’index, spécifiez le `NonUniformResourceIndex` qualificateur sur l’index, par exemple :

``` syntax
tex1[NonUniformResourceIndex(myMaterialID)].Sample(samp[NonUniformResourceIndex(samplerID)], texCoords);
```

Sur un matériel, l’utilisation de ce qualificateur génère du code supplémentaire pour assurer l’exactitude (y compris entre les threads), mais à un coût de performances mineur. Si un index est modifié sans ce qualificateur et dans un dessin/Dispatch, les résultats ne sont pas définis.

## <a name="descriptor-arrays-and-texture-arrays"></a>Tableaux de descripteurs et tableaux de texture

Les tableaux de textures sont disponibles depuis DirectX 10. Les tableaux de textures requièrent un descripteur, mais tous les secteurs de tableau doivent partager les mêmes format, largeur, hauteur et compte MIP. En outre, le tableau doit occuper une plage contiguë dans l’espace d’adressage virtuel. Le code suivant montre un exemple d’accès à un tableau de texture à partir d’un nuanceur.

``` syntax
float3 myCoord(1.0f,1.4f,2.2f); // 2.2f is array index (rounded to int)
color = myTex2DArray.Sample(mySampler, myCoord);
```

Dans un tableau de textures, l’index peut être librement modifié, sans nécessiter de qualificateurs tels que `NonUniformResourceIndex` .

Le tableau de descripteurs équivalent serait :

``` syntax
Texture2D<float4> myTex2DArray[] : register(t0); // t0+
float2 myCoord(1.0f, 1.4f);
color = myTex2D[2].Sample(mySampler,myCoord); // 2 is index
```

Remarque l’utilisation maladroite d’un float pour l’index de tableau est remplacée par `myTex2D[2]` . En outre, les tableaux de descripteurs offrent davantage de flexibilité avec les dimensions. Le type `Texture2D` est cet exemple, ne peut pas varier, mais le format, la largeur, la hauteur et le nombre MIP peuvent varier avec chaque descripteur.

Il est légitime d’avoir un tableau de descripteurs de tableaux de textures :

``` syntax
Texture2DArray<float4> myTex2DArrayOfArrays[2] : register(t0);
```

Il n’est pas possible de déclarer un tableau de structures, chaque structure contenant des descripteurs, par exemple le code suivant n’est pas pris en charge.

``` syntax
struct myStruct {
    Texture2D                    a; 
    Texture2D                    b;
    ConstantBuffer<myConstants>  c;
};
myStruct foo[10000] : register(....);
```

Cela aurait permis d’autoriser la disposition de la mémoire **abcabcabc.**..., mais il s’agit d’une limitation de langage et n’est pas prise en charge. L’une des méthodes prises en charge est la suivante, bien que la disposition de la mémoire dans ce cas soit **AAA... BBB... CCC...**.

``` syntax
Texture2D                     a[10000] : register(t0);
Texture2D                     b[10000] : register(t10000);
ConstantBuffer<myConstants>   c[10000] : register(b0);
```

Pour obtenir la disposition **abcabcabc....** Memory, utilisez une table de descripteur sans utiliser la `myStruct` structure.

## <a name="resource-aliasing"></a>Alias des ressources

Les plages de ressources spécifiées dans les nuanceurs HLSL sont des plages logiques. Elles sont liées à des plages de tas concrètes au moment de l’exécution via le mécanisme de signature racine. Normalement, une plage logique est mappée à une plage de tas qui ne se chevauche pas avec d’autres plages de tas. Toutefois, le mécanisme de signature racine permet d’effectuer un alias (chevauchement) des plages de tas de types compatibles. Par exemple, `tex2` les `tex3` plages de l’exemple ci-dessus peuvent être mappées à la même plage de tas (ou chevauchement), ce qui a pour effet d’affecter des textures à des textures dans le programme HLSL. Si de tels alias sont souhaités, le nuanceur doit être compilé avec les \_ ressources de nuanceur D3D10 peuvent être définies à l' \_ \_ \_ aide de l’option d' *\_ \_ alias/res peut* être définie pour l' [outil Effect-compiler Tool](/windows/desktop/direct3dtools/fxc) (fxc). L’option permet au compilateur de générer un code correct en empêchant certaines optimisations de charge/stockage en supposant que les ressources peuvent créer un alias.

## <a name="divergence-and-derivatives"></a>Divergence et dérivées

Le SM 5.1 n’impose pas de limitations sur l’index de ressource ; c’est-à-dire ` tex2[idx].Sample(…)` : l’index idx peut être une constante littérale, une constante CBuffer ou une valeur interpolée. Bien que le modèle de programmation offre une telle flexibilité exceptionnelle, il existe des problèmes à connaître :

-   Si l’index est divergent sur un quadruple, les dérivés calculés sur le matériel et les quantités dérivées telles que LOD peuvent ne pas être définies. Le compilateur HLSL fait le meilleur effort pour émettre un avertissement dans ce cas, mais n’empêchera pas la compilation d’un nuanceur. Ce comportement est similaire à celui des dérivés de calcul dans un workflow de contrôle divergent.
-   Si l’index de ressource est divergent, les performances sont réduites par rapport à la casse d’un index uniforme, car le matériel doit effectuer des opérations sur plusieurs ressources. Les index de ressources qui peuvent être divergents doivent être marqués avec la `NonUniformResourceIndex` fonction en code HLSL. Sinon, les résultats ne sont pas définis.

## <a name="uavs-in-pixel-shaders"></a>UAVs dans les nuanceurs de pixels

Le SM 5.1 n’impose pas de contraintes sur les plages de UAV dans les nuanceurs de pixels comme c’était le cas pour le SM 5.0.

## <a name="constant-buffers"></a>Mémoires tampons constantes

La syntaxe des tampons constantes du SM 5.1 (CBuffer) est passée de SM 5.0 pour permettre aux développeurs d’indexer des mémoires tampons constantes. Pour activer les mémoires tampons constantes indexables, le SM 5.1 introduit la `ConstantBuffer` construction « modèle » :

``` syntax
struct Foo
{
    float4 a;
    int2 b;
};
ConstantBuffer<Foo> myCB1[2][3] : register(b2, space1);
ConstantBuffer<Foo> myCB2 : register(b0, space1);
```

Le code précédent déclare une variable de mémoire tampon constante `myCB1` de type `Foo` et de taille 6, ainsi qu’une variable de mémoire tampon constante scalaire `myCB2` . Une variable de mémoire tampon constante peut maintenant être indexée dans le nuanceur en tant que :

``` syntax
myCB1[i][j].a.xyzw
myCB2.b.yy
```

Les champs « a » et « b » ne deviennent pas des variables globales, mais doivent plutôt être traités comme des champs. Pour la compatibilité descendante, SM 5.1 prend en charge l’ancien concept CBuffer pour Scala cbuffers. L’instruction suivante fait des variables globales « a » et « b », en lecture seule, comme dans SM 5.0. Toutefois, un CBuffer de style ancien ne peut pas être indexé.

``` syntax
cbuffer : register(b1)
{
    float4 a;
    int2 b;
};
```

Actuellement, le compilateur du nuanceur prend en charge le `ConstantBuffer` modèle uniquement pour les structures définies par l’utilisateur.

Pour des raisons de compatibilité, le compilateur HLSL peut affecter automatiquement des registres de ressources pour les plages déclarées dans `space0` . Si « Space » est omis dans la clause Register, la valeur par défaut `space0` est utilisée. Le compilateur utilise l’heuristique « First-Hole » pour assigner les registres. L’attribution peut être récupérée par le biais de l’API de réflexion, qui a été étendue pour ajouter le champ *espace* pour l’espace, tandis que le champ *BindPoint* indique la limite inférieure de la plage du registre des ressources.

## <a name="bytecode-changes-in-sm51"></a>Changements de bytecode dans SM 5.1

SM 5.1 change la façon dont les registres de ressources sont déclarés et référencés dans les instructions. La syntaxe implique la déclaration d’un registre « variable », de la même façon que pour les registres de mémoire partagée de groupe :

``` syntax
Texture2D<float4> tex0          : register(t5,  space0);
Texture2D<float4> tex1[][5][3]  : register(t10, space0);
Texture2D<float4> tex2[8]       : register(t0,  space1);
SamplerState samp0              : register(s5, space0);

float4 main(float4 coord : COORD) : SV_TARGET
{
    float4 r = coord;
    r += tex0.Sample(samp0, r.xy);
    r += tex2[r.x].Sample(samp0, r.xy);
    r += tex1[r.x][r.y][r.z].Sample(samp0, r.xy);
    return r;
}
```

Cela va désassembler :

``` syntax
// Resource Bindings:
//
// Name                                 Type  Format         Dim    ID   HLSL Bind     Count
// ------------------------------ ---------- ------- ----------- -----   --------- ---------
// samp0                             sampler      NA          NA     S0    a5            1
// tex0                              texture  float4          2d     T0    t5            1
// tex1[0][5][3]                     texture  float4          2d     T1   t10        unbounded
// tex2[8]                           texture  float4          2d     T2    t0.space1     8
//
//
//
// Input signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// COORD                    0   xyzw        0     NONE   float   xyzw
//
//
// Output signature:
//
// Name                 Index   Mask Register SysValue  Format   Used
// -------------------- ----- ------ -------- -------- ------- ------
// SV_TARGET                0   xyzw        0   TARGET   float   xyzw
//
ps_5_1
dcl_globalFlags refactoringAllowed
dcl_sampler s0[5:5], mode_default, space=0
dcl_resource_texture2d (float,float,float,float) t0[5:5], space=0
dcl_resource_texture2d (float,float,float,float) t1[10:*], space=0
dcl_resource_texture2d (float,float,float,float) t2[0:7], space=1
dcl_input_ps linear v0.xyzw
dcl_output o0.xyzw
dcl_temps 2
sample r0.xyzw, v0.xyxx, t0[0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, v0.xyzw
ftou r1.x, r0.x
sample r1.xyzw, r0.xyxx, t2[r1.x + 0].xyzw, s0[5]
add r0.xyzw, r0.xyzw, r1.xyzw
ftou r1.xyz, r0.zyxz
imul null, r1.yz, r1.zzyz, l(0, 15, 3, 0)
iadd r1.y, r1.z, r1.y
iadd r1.x, r1.x, r1.y
sample r1.xyzw, r0.xyxx, t1[r1.x + 10].xyzw, s0[5]
add o0.xyzw, r0.xyzw, r1.xyzw
ret
// Approximately 12 instruction slots are used.
```

Chaque plage de ressources de nuanceur a maintenant un ID (un nom) qui est unique pour le bytecode du nuanceur. Par exemple, le tableau de texture Tex1 (T10) devient « t 1 » dans le bytecode du nuanceur. L’attribution d’ID uniques à chaque plage de ressources permet d’effectuer deux opérations :

-   Identifiez clairement la plage de ressources (voir la \_ ressource DCL \_ Texture2D) qui est indexée dans une instruction (voir exemple d’instruction).
-   Attachement d’un ensemble d’attributs à la déclaration, par exemple, type d’élément, taille de numérisation, mode de fonctionnement raster, etc.

Notez que l’ID de la plage n’est pas associé à la déclaration de la limite inférieure HLSL.

L’ordre des liaisons de ressources de réflexion (répertoriées en haut) et les instructions de déclaration de nuanceur (DCL \_ \* ) sont les mêmes pour faciliter l’identification de la correspondance entre les variables HLSL et les ID de bytecode.

Chaque instruction de déclaration dans le SM 5.1 utilise un opérande 3D pour définir : ID de plage, limites inférieure et supérieure. Un jeton supplémentaire est émis pour spécifier l’espace de registre. D’autres jetons peuvent être émis pour transmettre des propriétés supplémentaires de la plage, par exemple, CBuffer ou une instruction de déclaration de mémoire tampon structurée émet la taille de la structure ou du CBuffer. Les détails exacts de l’encodage se trouvent dans d3d12TokenizedProgramFormat. h et **D3D10ShaderBinary :: CShaderCodeParser**.

Les instructions du SM 5.1 n’émettent pas d’informations d’opérande de ressource supplémentaires dans le cadre de l’instruction (comme dans le SM 5.0). Ces informations se trouvent maintenant dans les instructions de déclaration. Dans SM 5.0, les instructions d’indexation des ressources nécessitant des attributs de ressource sont décrites dans les jetons d’opcode étendus, car l’indexation a obscurci l’Association à la déclaration. Dans le SM 5.1, chaque ID (par exemple, « t 1 ») est associé de manière non équivoque à une déclaration unique qui décrit les informations sur les ressources requises. Par conséquent, les jetons d’opcode étendus utilisés sur les instructions pour décrire les informations sur les ressources ne sont plus émis.

Dans les instructions de non-déclaration, un opérande de ressource pour les échantillonneurs, SRVs et UAVs est un opérande 2D. Le premier index est une constante littérale qui spécifie l’ID de la plage. Le deuxième index représente la valeur linéarisée de l’index. La valeur est calculée par rapport au début de l’espace de Registre correspondant (et non par rapport au début de la plage logique) afin d’améliorer la corrélation avec la signature racine et réduire la charge de compilateur du pilote pour l’ajustement de l’index.

Un opérande de ressource pour CBVs est un opérande 3D, contenant : ID littéral de la plage, index de la mémoire tampon constante, décalage dans l’instance particulière de la mémoire tampon constante.

## <a name="example-hlsl-declarations"></a>Exemples de déclarations HLSL

Les programmes HLSL n’ont pas besoin de savoir quoi que ce soit sur les signatures racines. Ils peuvent assigner des liaisons à l’espace de liaison « Register » virtuel, t \# pour SRVs, u \# pour UAVs, b \# pour CBVS, s \# pour les échantillonneurs, ou s’appuyer sur le compilateur pour sélectionner des assignations (et interroger les mappages résultants à l’aide de la réflexion du nuanceur par la suite). La signature racine mappe les tables de descripteurs, les descripteurs racines et les constantes racine à cet espace de Registre virtuel.

Voici quelques exemples de déclarations qu’un nuanceur HLSL peut avoir. Notez qu’il n’existe aucune référence aux signatures racines ou aux tables de descripteurs.

``` syntax
Texture2D foo[5] : register(t2);
Buffer bar : register(t7);
RWBuffer dataLog : register(u1);

Sampler samp : register(s0);

struct Data
{
    UINT index;
    float4 color;
};
ConstantBuffer<Data> myData : register(b0);

Texture2D terrain[] : register(t8); // Unbounded array
Texture2D misc[] : register(t0,space1); // Another unbounded array 
                                        // space1 avoids overlap with above t#

struct MoreData
{
    float4x4 xform;
};
ConstantBuffer<MoreData> myMoreData : register(b1);

struct Stuff
{
    float2 factor;
    UINT drawID;
};
ConstantBuffer<Stuff> myStuff[][3][8]  : register(b2, space3)
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexation dynamique à l’aide de HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Effect-Tool du compilateur](/windows/desktop/direct3dtools/fxc)
</dt> <dt>

[Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Affichages ordonnés du rastériseur](rasterizer-order-views.md)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> <dt>

[Signatures racines](root-signatures.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Spécification de signatures racines en langage HLSL](specifying-root-signatures-in-hlsl.md)
</dt> </dl>

 

 