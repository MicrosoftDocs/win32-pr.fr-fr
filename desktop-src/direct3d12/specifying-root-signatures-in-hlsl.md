---
title: Spécification de signatures racine en langage HLSL
description: La spécification de signatures racines dans le modèle de nuanceur HLSL 5,1 est une alternative à leur spécification dans du code C++.
ms.assetid: 399F5E91-B017-4F5E-9037-DC055407D96F
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dad0da9f84d68fc1acbf53332d1cae4075f0faa
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/14/2021
ms.locfileid: "107492281"
---
# <a name="specifying-root-signatures-in-hlsl"></a>Spécification de signatures racine en langage HLSL

La spécification de signatures racines dans le modèle de nuanceur HLSL 5,1 est une alternative à leur spécification dans du code C++.

-   [Exemple de signature racine HLSL](#an-example-hlsl-root-signature)
    -   [Signature racine version 1,0](#root-signature-version-10)
    -   [Signature racine version 1.1](#root-signature-version-11)
-   [RootFlags](#rootflags)
-   [Constantes racine](#root-constants)
-   [Visibilité](#visibility)
-   [CBV au niveau de la racine](#root-level-cbv)
-   [SRV au niveau de la racine](#root-level-srv)
-   [UAV au niveau de la racine](#root-level-uav)
-   [Tableau du descripteur](#descriptor-table)
-   [Échantillonneur statique](#static-sampler)
-   [Compilation d’une signature racine HLSL](#compiling-an-hlsl-root-signature)
-   [Manipulation des signatures racines avec le compilateur FXC](#manipulating-root-signatures-with-the-fxc-compiler)
-   [Remarques](#notes)
-   [Rubriques connexes](#related-topics)

## <a name="an-example-hlsl-root-signature"></a>Exemple de signature racine HLSL

Une signature racine peut être spécifiée en langage HLSL en tant que chaîne. La chaîne contient une collection de clauses séparées par des virgules qui décrivent les composants constitutifs de la signature racine. La signature racine doit être identique sur les nuanceurs pour un objet d’état de pipeline (PSO). Voici un exemple :

### <a name="root-signature-version-10"></a>Signature racine version 1,0

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1), " \
              "SRV(t0), " \
              "UAV(u0, visibility = SHADER_VISIBILITY_GEOMETRY), " \
              "DescriptorTable( CBV(b0), " \
                               "UAV(u1, numDescriptors = 2), " \
                               "SRV(t1, numDescriptors = unbounded)), " \
              "DescriptorTable(Sampler(s0, numDescriptors = 2)), " \
              "RootConstants(num32BitConstants=1, b9), " \
              "DescriptorTable( UAV(u3), " \
                               "UAV(u4), " \
                               "UAV(u5, offset=1)), " \

              "StaticSampler(s2)," \
              "StaticSampler(s3, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Cette définition donne la signature racine suivante, en notant :

-   Utilisation des paramètres par défaut.
-   B0 et (B0, Space = 1) ne sont pas en conflit
-   U0 est visible uniquement pour le nuanceur Geometry
-   U4 et U5 ont pour alias le même descripteur dans un segment de mémoire

![signature racine spécifiée à l’aide du langage de nuanceur de haut niveau](images/hlsl-root-signature.png)

### <a name="root-signature-version-11"></a>Signature racine version 1.1

La [signature racine Version 1,1](root-signature-version-1-1.md) permet d’optimiser les pilotes sur les descripteurs de signature racine et les données.

``` syntax
#define MyRS1 "RootFlags( ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | " \
                         "DENY_VERTEX_SHADER_ROOT_ACCESS), " \
              "CBV(b0, space = 1, flags = DATA_STATIC), " \
              "SRV(t0), " \
              "UAV(u0), " \
              "DescriptorTable( CBV(b1), " \
                               "SRV(t1, numDescriptors = 8, " \
                               "        flags = DESCRIPTORS_VOLATILE), " \
                               "UAV(u1, numDescriptors = unbounded, " \
                               "        flags = DESCRIPTORS_VOLATILE)), " \
              "DescriptorTable(Sampler(s0, space=1, numDescriptors = 4)), " \
              "RootConstants(num32BitConstants=3, b10), " \
              "StaticSampler(s1)," \
              "StaticSampler(s2, " \
                             "addressU = TEXTURE_ADDRESS_CLAMP, " \
                             "filter = FILTER_MIN_MAG_MIP_LINEAR )"
```

Le langage de signature racine HLSL correspond étroitement aux API de signature racine C++ et a une puissance expressif équivalente. La signature racine est spécifiée en tant que séquence de clauses, séparées par des virgules. L’ordre des clauses est important, car l’ordre d’analyse détermine la position de l’emplacement dans la signature racine. Chaque clause accepte un ou plusieurs paramètres nommés. Toutefois, l’ordre des paramètres n’est pas important.

## <a name="rootflags"></a>RootFlags

La clause facultative *RootFlags* prend la valeur 0 (valeur par défaut pour indiquer qu’il n’y a pas d’indicateur), ou une ou plusieurs valeurs d’indicateurs racines prédéfinies, connectées via l’opérateur ou' \| '. Les valeurs d’indicateur racine autorisées sont définies par les [**\_ \_ \_ indicateurs de signature racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags).

Par exemple :

``` syntax
RootFlags(0) // default value – no flags
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT)
RootFlags(ALLOW_INPUT_ASSEMBLER_INPUT_LAYOUT | DENY_VERTEX_SHADER_ROOT_ACCESS)
```

## <a name="root-constants"></a>Constantes racine

La clause *RootConstants* spécifie des constantes racine dans la signature racine. Deux paramètres obligatoires sont : *num32BitConstants* et *bReg* (le registre correspondant à *BaseShaderRegister* dans les API C++) du *CBuffer*. Les paramètres espace (*RegisterSpace* dans les API c++) et visibilité (*ShaderVisibility* en c++) sont facultatifs, et les valeurs par défaut sont :

``` syntax
RootConstants(num32BitConstants=N, bReg [, space=0, 
              visibility=SHADER_VISIBILITY_ALL ])
```

Par exemple :

``` syntax
RootConstants(num32BitConstants=3, b3)
```

## <a name="visibility"></a>Visibilité

Visibility est un paramètre facultatif qui peut avoir l’une des valeurs de la [**\_ \_ visibilité du nuanceur D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

\_La visibilité \_ du nuanceur diffuse tous les arguments racine à tous les nuanceurs. Sur un matériel, cela n’a aucun coût, mais sur un autre matériel, il y a un coût pour la duplication des données à toutes les étapes du nuanceur. La définition de l’une des options, comme \_ le vertex de visibilité du nuanceur \_ , limite l’argument racine à une seule étape de nuanceur.

La définition des arguments racine sur des étapes de nuanceur uniques permet d’utiliser le même nom de liaison à différentes étapes. Par exemple, une liaison SRV de `t0,SHADER_VISIBILITY_VERTEX` et une liaison SRV de sont `t0,SHADER_VISIBILITY_PIXEL` valides. Toutefois, si le paramètre de visibilité était `t0,SHADER_VISIBILITY_ALL` pour l’une des liaisons, la signature racine n’est pas valide.

## <a name="root-level-cbv"></a>CBV au niveau de la racine

La `CBV` clause (vue de la mémoire tampon constante) spécifie une entrée de registre de la mémoire tampon de l’enregistrement b-Register au niveau de la racine. Notez qu’il s’agit d’une entrée scalaire ; Il n’est pas possible de spécifier une plage pour le niveau racine.

``` syntax
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
CBV(bReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-srv"></a>SRV au niveau de la racine

La `SRV` clause (vue de ressource Shader) spécifie une entrée de Registre SRV t-Register de niveau racine. Notez qu’il s’agit d’une entrée scalaire ; Il n’est pas possible de spécifier une plage pour le niveau racine.

``` syntax
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
SRV(tReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

## <a name="root-level-uav"></a>UAV au niveau de la racine

La `UAV` clause (vue d’accès non ordonnée) spécifie une entrée de Registre UAV u-Register au niveau de la racine. Notez qu’il s’agit d’une entrée scalaire ; Il n’est pas possible de spécifier une plage pour le niveau racine.

``` syntax
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL ])    //   Version 1.0
UAV(uReg [, space=0, visibility=SHADER_VISIBILITY_ALL,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Par exemple :

``` syntax
UAV(u3)
```

## <a name="descriptor-table"></a>Tableau du descripteur

La `DescriptorTable` clause est elle-même une liste de clauses de table de descripteur séparées par des virgules, ainsi qu’un paramètre de visibilité facultatif. Les clauses *DescriptorTable* incluent CBV, SRV, UAV et échantillonner. Notez que leurs paramètres diffèrent de ceux des clauses de niveau racine.

``` syntax
DescriptorTable( DTClause1, [ DTClause2, … DTClauseN,
                 visibility=SHADER_VISIBILITY_ALL ] )
```

La table du descripteur `CBV` a la syntaxe suivante :

``` syntax
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])   // Version 1.0
CBV(bReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND      // Version 1.1
          , flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Par exemple :

``` syntax
DescriptorTable(CBV(b0),SRV(t3, numDescriptors=unbounded))
```

Le paramètre obligatoire *bReg* spécifie le début de l’reg de la plage CBuffer. Le paramètre *numDescriptors* spécifie le nombre de descripteurs dans la plage de CBuffer contiguës ; la valeur par défaut est 1. L’entrée déclare une plage CBuffer ` [Reg, Reg + numDescriptors - 1]` , lorsque *numDescriptors* est un nombre. Si *numDescriptors* est égal à « Unlimited », la plage est `[Reg, UINT_MAX]` , ce qui signifie que l’application doit s’assurer qu’elle ne référence pas de zone hors limites. Le champ *offset* représente le paramètre *OffsetInDescriptorsFromTableStart* dans les API C++, autrement dit, l’offset (dans descripteurs) à partir du début de la table. Si le décalage est défini sur le descripteur de décalage de la plage de descripteurs \_ \_ \_ (valeur par défaut), cela signifie que la plage se trouve directement après la plage précédente. Toutefois, l’entrée de décalages spécifiques permet aux plages de se chevaucher l’une de l’autre, ce qui permet d’enregistrer les alias.

La table du descripteur `SRV` a la syntaxe suivante :

``` syntax
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
SRV(tReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_STATIC_WHILE_SET_AT_EXECUTE ])
```

Cela est similaire à l’entrée du tableau du descripteur `CBV` , à la différence que la plage spécifiée concerne les vues des ressources de nuanceur.

La table du descripteur `UAV` a la syntaxe suivante :

``` syntax
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])    // Version 1.0
UAV(uReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,      // Version 1.1
            flags=DATA_VOLATILE ])
```

Cela est similaire à l’entrée de table du descripteur `CBV` , à la différence que la plage spécifiée concerne les vues d’accès non ordonnées.

La table du descripteur `Sampler` a la syntaxe suivante :

``` syntax
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND ])  // Version 1.0
Sampler(sReg [, numDescriptors=1, space=0, offset=DESCRIPTOR_RANGE_OFFSET_APPEND,    // Version 1.1
                flags=0 ])
```

Cela est similaire à l’entrée de table du descripteur `CBV` , sauf que la plage spécifiée est pour les échantillonneurs de nuanceur. Notez que les échantillonneurs ne peuvent pas être mélangés avec d’autres types de descripteurs dans la même table de descripteurs (puisqu’ils se trouvent dans un tas de descripteur distinct).

## <a name="static-sampler"></a>Échantillonneur statique

L’échantillonneur statique représente la structure de l' [**\_ \_ échantillonneur \_ statique D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) . Le paramètre obligatoire pour *StaticSampler* est un fichier de Registre scalaire, d’échantillonneur. Les autres paramètres sont facultatifs avec les valeurs par défaut indiquées ci-dessous. La plupart des champs acceptent un ensemble d’énumérations prédéfinies.

``` syntax
StaticSampler( sReg,
              [ filter = FILTER_ANISOTROPIC, 
                addressU = TEXTURE_ADDRESS_WRAP,
                addressV = TEXTURE_ADDRESS_WRAP,
                addressW = TEXTURE_ADDRESS_WRAP,
                mipLODBias = 0.f,
                maxAnisotropy = 16,
                comparisonFunc = COMPARISON_LESS_EQUAL,
                borderColor = STATIC_BORDER_COLOR_OPAQUE_WHITE,
                minLOD = 0.f,         
                maxLOD = 3.402823466e+38f,
                space = 0, 
                visibility = SHADER_VISIBILITY_ALL ])
```

Par exemple :

``` syntax
StaticSampler(s4, filter=FILTER_MIN_MAG_MIP_LINEAR)
```

Les options des paramètres sont très similaires aux appels de l’API C++, à l’exception de *BorderColor*, qui est limité à une énumération en HLSL.

Le champ de filtre peut être l’un des [**\_ filtres D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter).

Les champs d’adresse peuvent tous être un [**\_ mode d' \_ adresse \_ de texture D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode).

La fonction de comparaison peut être l’une des fonctions de [**\_ comparaison \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func).

Le champ de couleur de la bordure peut être une [**\_ \_ \_ couleur de bordure statique D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color).

La visibilité peut être l’une des D3D12 de la [**\_ \_ visibilité du nuanceur**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility).

## <a name="compiling-an-hlsl-root-signature"></a>Compilation d’une signature racine HLSL

Il existe deux mécanismes pour compiler une signature racine HLSL. Tout d’abord, il est possible d’attacher une chaîne de signature racine à un nuanceur particulier par le biais de l’attribut *RootSignature* (dans l’exemple suivant, à l’aide du point d’entrée **MyRS1** ) :

``` syntax
[RootSignature(MyRS1)]
float4 main(float4 coord : COORD) : SV_Target
{
…
}
```

Le compilateur crée et vérifie l’objet blob de signature racine pour le nuanceur et l’incorpore en même temps que le code d’octet du nuanceur dans l’objet blob de nuanceur. Le compilateur prend en charge la syntaxe de signature racine pour le Shader Model 5,0 et versions ultérieures. Si une signature racine est incorporée dans un nuanceur de modèle de nuanceur 5,0 et que le nuanceur est envoyé au runtime D3D11, contrairement à D3D12, la partie de la signature racine est ignorée en mode silencieux par D3D11.

L’autre mécanisme consiste à créer un objet blob de signature racine autonome, peut-être à le réutiliser avec un grand ensemble de nuanceurs, ce qui économise de l’espace. L' [outil Effect-compiler Tool](/windows/desktop/direct3dtools/fxc) (fxc) prend en charge les modèles de nuanceur **rootsig \_ 1 \_ 0** et **rootsig \_ 1 \_ 1** . Le nom de la chaîne définie est spécifié à l’aide de l’argument/E habituel. Par exemple :

``` syntax
fxc.exe /T rootsig_1_1 MyRS1.hlsl /E MyRS1 /Fo MyRS1.fxo
```

Notez que la définition de la chaîne de signature racine peut également être passée sur la ligne de commande, par exemple/D MyRS1 = "...".

## <a name="manipulating-root-signatures-with-the-fxc-compiler"></a>Manipulation des signatures racines avec le compilateur FXC

Le compilateur FXC crée un code d’octet de nuanceur à partir de fichiers sources HLSL. Il existe un grand nombre de paramètres facultatifs pour ce compilateur, reportez-vous à l' [outil Effect-compiler](/windows/desktop/direct3dtools/fxc).

Pour la gestion des signatures racines créées par HLSL, le tableau suivant fournit des exemples d’utilisation de FXC.



| Courbes | Ligne de commande                                                                 | Description                                                                                                                                                                                                                              |
|------|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1    | `fxc /T ps_5_1 shaderWithRootSig.hlsl /Fo rs1.fxo`                           | Compile un nuanceur pour la cible de nuanceur de pixels 5,1, la source du nuanceur se trouve dans le fichier shaderWithRootSig. HLSL, qui comprend une signature racine. Le nuanceur et la signature racine sont compilés en tant qu’objets BLOB distincts dans le fichier binaire RS1. FXO.    |
| 2    | `fxc /dumpbin rs1.fxo /extractrootsignature /Fo rs1.rs.fxo`                  | Extrait la signature racine du fichier créé par la ligne 1, de sorte que le fichier RS1. RS. FXO contient simplement une signature racine.                                                                                                                      |
| 3    | `fxc /dumpbin rs1.fxo /Qstrip_rootsignature /Fo rs1.stripped.fxo`            | Supprime la signature racine du fichier créé par la ligne 1, de sorte que le fichier RS1. decapad. FXO contient un shader sans signature racine.                                                                                                       |
| 4    | `fxc /dumpbin rs1.stripped.fxo /setrootsignature rs1.rs.fxo /Fo rs1.new.fxo` | Combine un nuanceur et une signature racine qui se trouvent dans des fichiers distincts en un fichier binaire contenant les deux objets BLOB. Dans cet exemple, RS1. New. FX0 est identique à RS1. FX0 à la ligne 1.                                                           |
| 5    | `fxc /T rootsig_1_0 rootSigAndMaybeShaderInHereToo.hlsl /E RS1 /Fo rs2.fxo`  | Crée un fichier binaire de signature racine autonome à partir d’une source qui peut contenir plus qu’une seule signature racine. Notez la \_ cible rootsig 1 \_ 0 et RS1 est le nom de la chaîne de macro de signature racine ( \# define) dans le fichier HLSL. |



 

Les fonctionnalités disponibles via FXC sont également disponibles par programme à l’aide de la fonction [**D3DCompile**](/windows/desktop/direct3dhlsl/d3dcompile) . Cet appel compile un nuanceur avec une signature racine ou une signature racine autonome (en définissant la cible rootsig \_ 1 \_ 0). [**D3DGetBlobPart**](/windows/desktop/direct3dhlsl/d3dgetblobpart) et [**D3DSetBlobPart**](/windows/desktop/direct3dhlsl/d3dsetblobpart) peuvent extraire et attacher des signatures racines à un objet BLOB existant.  \_ \_ La signature racine d’objet BLOB D3D \_ est utilisée pour spécifier le type de composant blob de signature racine. [**D3DStripShader**](/windows/desktop/direct3dhlsl/d3dstripshader) supprime la signature racine (à l’aide de l' \_ \_ \_ indicateur de signature racine D3DCOMPILER Strip) de l’objet BLOB.

## <a name="notes"></a>Notes

> [!Note]  
> Alors que la compilation hors connexion des nuanceurs est fortement recommandée, si les nuanceurs doivent être compilés au moment de l’exécution, reportez-vous aux remarques relatives à [**D3DCompile2**](/windows/desktop/direct3dhlsl/d3dcompile2).

 

> [!Note]  
> Les ressources HLSL existantes n’ont pas besoin d’être modifiées pour gérer les signatures racines à utiliser avec elles.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Indexation dynamique à l’aide de HLSL 5.1](dynamic-indexing-using-hlsl-5-1.md)
</dt> <dt>

[Caractéristiques du modèle de nuanceur HLSL 5,1 pour Direct3D 12](/windows/desktop/direct3dhlsl/hlsl-shader-model-5-1-features-for-direct3d-12)
</dt> <dt>

[Liaison de ressource](resource-binding.md)
</dt> <dt>

[Liaison de ressource dans HSL](resource-binding-in-hlsl.md)
</dt> <dt>

[Signatures racine](root-signatures.md)
</dt> <dt>

[Modèle de nuanceur 5,1](/windows/desktop/direct3dhlsl/shader-model-5-1)
</dt> <dt>

[Valeur de référence du stencil spécifié par le nuanceur](shader-specified-stencil-reference-value.md)
</dt> <dt>

[Chargements de vues d’accès non ordonnées typées](typed-unordered-access-view-loads.md)
</dt> </dl>

 

 
