---
description: La page suivante fournit un plan de base des principales différences entre Direct3D 9 et Direct3D 10. Le plan ci-dessous fournit des informations pour aider les développeurs avec l’expérience Direct3D 9 à explorer et à associer Direct3D 10.
ms.assetid: 283b54e0-94cb-47a8-8cfc-5798e0538b9f
title: Considérations relatives à Direct3D 9 vers Direct3D 10 (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467ceefe7784a9b408bb36c8bed13217cb6de7c4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748021"
---
# <a name="direct3d-9-to-direct3d-10-considerations-direct3d-10"></a>Considérations relatives à Direct3D 9 vers Direct3D 10 (Direct3D 10)

La page suivante fournit un plan de base des principales différences entre Direct3D 9 et Direct3D 10. Le plan ci-dessous fournit des informations pour aider les développeurs avec l’expérience Direct3D 9 à explorer et à associer Direct3D 10.

Bien que les informations de cette rubrique comparent Direct3D 9 avec Direct3D 10, puisque Direct3D 11 s’appuie sur les améliorations apportées à Direct3D 10 et 10,1, vous avez également besoin de ces informations pour effectuer la migration de Direct3D 9 vers Direct3D 11. Pour plus d’informations sur le passage au-delà de Direct3D 10 vers Direct3D 11, consultez [migration vers Direct3D 11](../direct3d11/d3d11-programming-guide-migrating.md).

-   [Vue d’ensemble des principales modifications structurelles dans Direct3D 10](#overview-of-the-major-structural-changes-in-direct3d-10)
    -   [Suppression de la fonction Fixed](#removal-of-fixed-function)
    -   [Validation de l’heure de création de l’objet périphérique](#device-object-creation-time-validation)
-   [Abstractions/séparation du moteur](/windows)
    -   [Suppression directe des dépendances Direct3D 9](#direct-removal-of-direct3d-9-dependencies)
-   [Astuces pour résoudre rapidement les problèmes de génération d’applications](#tricks-for-quickly-resolving-application-build-issues)
    -   [Substitution de types Direct3D 9](#overriding-direct3d-9-types)
    -   [Résolution des problèmes liés aux liens](#resolving-link-issues)
    -   [Simulation des Cap des appareils](#simulating-device-caps)
-   [Conduite de l’API Direct3D 10](#driving-the-direct3d-10-api)
    -   [Création de ressources](#resource-creation)
    -   [Views](#views)
    -   [Accès aux ressources statiques et dynamiques](#static-versus-dynamic-resource-access)
    -   [Effets Direct3D 10](#direct3d-10-effects)
    -   [HLSL sans effets](#hlsl-without-effects)
    -   [Compilation du nuanceur](#shader-compilation)
    -   [Création de ressources de nuanceur](#creation-of-shader-resources)
    -   [Interface de couche de réflexion du nuanceur](#shader-reflection-layer-interface)
    -   [Dispositions de l’assembleur d’entrée-liaison de nuanceur de sommets/flux d’entrée](/windows)
    -   [Impact de la suppression du code mort du nuanceur](#impact-of-shader-dead-code-removal)
    -   [Exemple de structure d’entrée de nuanceur de sommets](#vertex-shader-input-structure-example)
    -   [Création d’un objet d’État](#state-object-creation)
-   [Portage des textures](#porting-textures)
    -   [Formats de fichier pris en charge](#file-formats-supported)
    -   [Mappage des formats de texture](#mapping-texture-formats)
-   [Portage des nuanceurs](#porting-shaders)
    -   [Les nuanceurs Direct3D 10 sont créés en HLSL](#direct3d-10-shaders-are-authored-in-hlsl)
    -   [Signatures et liaison de nuanceur](#shader-signatures-and-linkage)
    -   [Liaisons d’étape de nuanceur HLSL](#hlsl-shader-stage-linkages)
    -   [Mémoires tampons constantes](#constant-buffers)
    -   [Plans d’utilisateur en HLSL sur le niveau de fonctionnalité 9 et versions ultérieures](#user-clip-planes-in-hlsl-on-feature-level-9-and-higher)
-   [Autres différences Direct3D 10 à surveiller](#additional-direct3d-10-differences-to-watch-for)
    -   [Entiers comme entrée](#integers-as-input)
    -   [Curseurs de la souris](#mouse-cursors)
    -   [Mappage de texels à des pixels dans Direct3D 10](#mapping-texels-to-pixels-in-direct3d-10)
    -   [Modifications du comportement du décompte de références](#reference-counting-behavior-changes)
    -   [Niveau de coopératif de test](#test-cooperative-level)
    -   [StretchRect](#stretchrect)
-   [Différences Direct3D 10,1 supplémentaires](#additional-direct3d-101-differences)
-   [Rubriques connexes](#related-topics)

## <a name="overview-of-the-major-structural-changes-in-direct3d-10"></a>Vue d’ensemble des principales modifications structurelles dans Direct3D 10

-   [Suppression de la fonction Fixed](#removal-of-fixed-function)
-   [Validation de l’heure de création de l’objet périphérique](#device-object-creation-time-validation)

Le processus de rendu à l’aide de l’appareil Direct3D 10 est structurellement similaire à Direct3D 9.

-   Définir une source de flux de vertex
-   Définir la disposition d’entrée dans Direct3D 10 (définir la déclaration de flux de vertex dans Direct3D 9)
-   Déclarer la topologie primitive
-   Définir des textures
-   Définir les objets d’État
-   Définir des nuanceurs
-   Dessin

L’appel de [**dessin**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) lie les opérations ensemble ; l’ordre des appels avant l’appel de dessin est arbitraire. Les principales différences dans la conception de l’API Direct3D 10 sont les suivantes :

-   Suppression de la fonction Fixed
-   Suppression des bits en MAJUSCULEs-l’ensemble des fonctionnalités de base de Direct3D 10 est garanti
-   Gestion plus stricte : accès aux ressources, état de l’appareil, constantes de nuanceur, liaison de nuanceur (entrées et sorties aux nuanceurs) entre les phases
-   Les modifications du nom du point d’entrée de l’API reflètent l’utilisation de la mémoire du GPU virtuel (Map () au lieu de lock ()).
-   Une couche de débogage peut être ajoutée à l’appareil au moment de la création
-   La topologie primitive est désormais un État explicite (séparé de l’appel de [**dessin**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-draw) )
-   Les constantes de nuanceur explicites sont maintenant stockées dans des mémoires tampons constantes
-   La création de nuanceur est entièrement effectuée en HLSL. Le compilateur HLSL se trouve désormais dans la DLL principale de Direct3D 10.
-   Nouvelle étape programmable-nuanceur de géométrie
-   Suppression de BeginScene ()/EndScene ()
-   Fonctionnalités courantes de gestion des adaptateurs, de focus et de mise en œuvre dans un nouveau composant : DXGI

### <a name="removal-of-fixed-function"></a>Suppression de la fonction Fixed

Il est parfois surprenant que même dans un moteur Direct3D 9 qui exploite pleinement le pipeline programmable, il reste un certain nombre de zones qui dépendent du pipeline de fonction fixe (FF). Les zones les plus courantes sont généralement liées au rendu aligné sur l’espace de l’écran pour l’interface utilisateur. C’est pour cette raison que vous devrez probablement créer un nuanceur d’émulation FF ou un ensemble de nuanceurs qui fournissent les comportements de remplacement nécessaires.

Cette documentation contient un livre blanc contenant des sources de nuanceur de remplacement pour les comportements FF les plus courants (Voir l' [exemple Fixed Function UME](https://msdn.microsoft.com/library/Ee416406(v=VS.85).aspx)). Certains comportements de pixel de fonction fixe, y compris le test alpha, ont été déplacés dans les nuanceurs.

### <a name="device-object-creation-time-validation"></a>Validation de l’heure de création de l’objet périphérique

Le pipeline Direct3D 10 a été remanié du point de vue du matériel et des logiciels, avec un objectif principal de réduire la surcharge du processeur (au moment du tracé). Pour réduire les coûts, tous les types de données de l’appareil ont été affectés à un objet avec des méthodes de création explicites fournies par l’appareil lui-même. Cela permet une validation stricte des données au moment de la création de l’objet plutôt que pendant l’appel de dessin, comme c’est souvent le cas avec Direct3D 9.

## <a name="engine-abstractions--separation"></a>Abstractions/séparation du moteur

Les applications, y compris les jeux, qui souhaitent prendre en charge Direct3D 9 et Direct3D 10 doivent avoir les couches de rendu abstraites du reste de la base de code. Il existe de nombreuses façons d’y parvenir, mais la clé de chacun d’entre eux est la conception de la couche d’abstraction pour le périphérique Direct3D de niveau inférieur. Tous les systèmes doivent communiquer avec le matériel via la couche commune, conçue pour fournir la ressource GPU et la gestion des types de bas niveau.

### <a name="direct-removal-of-direct3d-9-dependencies"></a>Suppression directe des dépendances Direct3D 9

Lors du Portage de bases de code volumineuses et précédemment testées, il est important de réduire la quantité de modifications de code à celles qui sont absolument nécessaires pour conserver les comportements testés précédemment dans le code. Les meilleures pratiques incluent clairement la façon dont les éléments sont modifiés à l’aide de commentaires. Il est souvent utile d’avoir une norme de commentaires pour ce travail, ce qui permet une navigation rapide dans la base de code.

Vous trouverez ci-dessous un exemple de liste de commentaires de bloc de début/ligne standard qui pourraient être utilisés pour ce travail.



| Élément                                                                                                                                                                             | Description                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="___Direct3D_10_REMOVED"></span><span id="___direct3d_10_removed"></span><span id="___DIRECT3D_10_REMOVED"></span>Direct3D 10 supprimé<br/>                     | Utilisez cette ligne où les lignes/blocs de code sont supprimés<br/>                                                                                                                                                                                                                                                                   |
| <span id="___Direct3D_10_NEEDS_UPDATE"></span><span id="___direct3d_10_needs_update"></span><span id="___DIRECT3D_10_NEEDS_UPDATE"></span>MISE à jour des besoins Direct3D 10<br/> | Elle permet d’ajouter des remarques supplémentaires au commentaire de mise à jour nécessaire, qui suggère l’utilisation de l’API travail/nouvelle pour les visites ultérieures au code pour la conversion de comportement. Une utilisation intensive de la méthode Assert (**false**) doit également être utilisée lorsque \\ \\ Direct3D 10 a besoin d’une mise à jour pour s’assurer que vous n’exécutez pas de code errant sans le savoir.<br/> |
| <span id="___Direct3D_10_CHANGED"></span><span id="___direct3d_10_changed"></span><span id="___DIRECT3D_10_CHANGED"></span>Direct3D 10 modifié<br/>                     | Les zones où des modifications majeures ont été apportées doivent être conservées pour référence ultérieure, mais commentées<br/>                                                                                                                                                                                                                       |
| <span id="___Direct3D_10_END"></span><span id="___direct3d_10_end"></span><span id="___DIRECT3D_10_END"></span>FIN de Direct3D 10<br/>                                     | Qualificateur de bloc de code de fin<br/>                                                                                                                                                                                                                                                                                            |



 

Pour plusieurs lignes de source, vous devez également utiliser les commentaires//de style C \* \* , mais ajouter les commentaires de début/fin appropriés autour de ces zones.

## <a name="tricks-for-quickly-resolving-application-build-issues"></a>Astuces pour résoudre rapidement les problèmes de génération d’applications

-   [Substitution de types Direct3D 9](#overriding-direct3d-9-types)
-   [Résolution des problèmes liés aux liens](#resolving-link-issues)
-   [Simulation des Cap des appareils](#simulating-device-caps)

### <a name="overriding-direct3d-9-types"></a>Substitution de types Direct3D 9

Il peut être utile d’insérer un fichier d’en-tête de haut niveau contenant des définitions/remplacements de type pour les types de base Direct3D 9 qui ne sont plus pris en charge par les en-têtes Direct3D 10. Cela vous permet de réduire le nombre de modifications dans le code et les interfaces où il existe un mappage direct d’un type Direct3D 9 vers le type Direct3D 10 nouvellement défini. Cette approche est également utile pour conserver les comportements de code dans un fichier source. Dans ce cas, il est judicieux de définir des types de noms neutres/généralement nommés qui décrivent les constructions courantes utilisées pour le rendu, mais qui s’étendent encore sur les API Direct3D 9 et Direct3D 10. Par exemple :


```
#if defined(D3D9)
typedef IDirect3DIndexBuffer9   IDirect3DIndexBuffer;
typedef IDirect3DVertexBuffer9  IDirect3DVertexBuffer;
#else //D3D10
typedef ID3D10Buffer            IDirect3DIndexBuffer;
typedef ID3D10Buffer            IDirect3DVertexBuffer
#endif
```



Voici d’autres exemples spécifiques à Direct3D 10 :


```
typedef ID3D10TextureCube   IDirect3DCubeTexture;
typedef ID3D10Texture3D     IDirect3DVolumeTexture;
typedef D3D10_VIEWPORT      D3DVIEWPORT;
typedef ID3D10VertexShader  IDirect3DVertexShader;
typedef ID3D10PixelShader   IDirect3DPixelShader;
```



### <a name="resolving-link-issues"></a>Résolution des problèmes liés aux liens

Il est recommandé de développer des applications Direct3D 10 et Windows Vista à l’aide de la dernière version de Microsoft Visual Studio. Toutefois, il est possible de créer une application Windows Vista qui dépend de Direct3D 10 à l’aide de la version 2003 antérieure de Visual Studio. Direct3D 10 est un composant de plateforme Windows Vista qui a des dépendances (comme le kit de développement logiciel (SDK) de plate-forme serveur 2003 SP1) sur la bibliothèque suivante : BufferOverflowU. lib est nécessaire pour résoudre les problèmes de l’éditeur de liens de vérification de sécurité de mémoire tampon \_ .

### <a name="simulating-device-caps"></a>Simulation des Cap des appareils

De nombreuses applications contiennent des zones de code qui dépendent des données de la capitalisation des appareils disponibles. Contourner cela en remplaçant l’énumération des appareils et en forçant les limites des appareils à des valeurs sensibles. Envisagez de revisiter les zones où il y a des dépendances sur les Cap ultérieurement pour la suppression complète des Cap dans la mesure du possible.

## <a name="driving-the-direct3d-10-api"></a>Conduite de l’API Direct3D 10

Cette section se concentre sur les modifications de comportement provoquées par l’API Direct3D 10.

-   [Création de ressources](#resource-creation)
-   [Views](#views)
-   [Accès aux ressources statiques et dynamiques](#static-versus-dynamic-resource-access)
-   [Effets Direct3D 10](#direct3d-10-effects)
-   [HLSL sans effets](#hlsl-without-effects)
-   [Compilation du nuanceur](#shader-compilation)
-   [Création de ressources de nuanceur](#creation-of-shader-resources)
-   [Interface de couche de réflexion du nuanceur](#shader-reflection-layer-interface)
-   [Dispositions de l’assembleur d’entrée-liaison de nuanceur de sommets/flux d’entrée](/windows)
-   [Impact de la suppression du code mort du nuanceur](#impact-of-shader-dead-code-removal)
-   [Exemple de structure d’entrée de nuanceur de sommets](#vertex-shader-input-structure-example)
-   [Création d’un objet d’État](#state-object-creation)

### <a name="resource-creation"></a>Création de ressources

L’API Direct3D 10 a conçu des ressources en tant que types de tampons génériques qui ont des indicateurs de liaison spécifiques en fonction de l’utilisation planifiée. Ce point de conception a été choisi pour faciliter l’accès presque omniprésent des ressources dans le pipeline pour des scénarios tels que le rendu dans une mémoire tampon de vertex, puis le dessin instantané des résultats sans interrompre l’UC. L’exemple suivant illustre l’allocation de mémoires tampons de vertex et de tampon d’index, où vous pouvez voir que la description de la ressource diffère uniquement par les indicateurs de liaison de la ressource GPU.

L’API Direct3D 10 a fourni des méthodes d’assistance de texture pour créer explicitement des ressources de type texture, mais comme vous pouvez l’imaginer, il s’agit d’une fonction d’assistance.

-   CreateTexture2D()
-   CreateTextureCube()
-   CreateTexture3D()

Quand vous ciblez Direct3D 10, vous souhaiterez probablement allouer plus d’éléments pendant la durée de création des ressources que vous ne l’utilisez avec Direct3D 9. Cela deviendra le plus évident avec la création de mémoires tampons cibles de rendu et de textures où vous devez également créer une vue pour accéder à la mémoire tampon et définir la ressource sur l’appareil.

[Didacticiel 1 : principes de base de Direct3D 10](https://msdn.microsoft.com/library/Ee416436(v=VS.85).aspx)

> [!Note]  
> Direct3D 10 et les versions ultérieures de Direct3D étendent le format de fichier DDS pour prendre en charge de nouveaux formats DXGI, des tableaux de texture et des tableaux de mappage de cube. Pour plus d’informations sur l’extension de format de fichier DDS, consultez le [Guide de programmation pour DDS](../direct3ddds/dx-graphics-dds-pguide.md).

 

### <a name="views"></a>Les vues

Une vue est une interface spécifiquement typée aux données stockées dans une mémoire tampon de pixels. Plusieurs vues peuvent être allouées à une ressource à la fois et cette fonctionnalité est mise en surbrillance dans l’exemple de carte cubique de passe unique contenu dans ce kit de développement logiciel (SDK).

[Page Guide des programmeurs sur l’accès aux ressources](d3d10-graphics-programming-guide-resources-access-views.md)

[Exemple carte cubique](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

### <a name="static-versus-dynamic-resource-access"></a>Accès aux ressources statiques et dynamiques

Pour des performances optimales, les applications doivent partitionner l’utilisation des données en fonction de la nature statique et dynamique des données. Direct3D 10 a été conçu pour tirer parti de cette approche et, par conséquent, les règles d’accès aux ressources ont été considérablement renforcées par Direct3D 9. Pour les ressources statiques, vous devez idéalement remplir la ressource avec ses données au moment de la création. Si votre moteur a été conçu autour du point de conception créer, verrouiller, remplir et déverrouiller de Direct3D 9, vous pouvez différer le remplissage de l’heure de création à l’aide d’une ressource de mise en lots et de la méthode UpdateSubResource sur l’interface de ressource.

### <a name="direct3d-10-effects"></a>Effets Direct3D 10

L’utilisation du système d’effets Direct3D 10 sort du cadre de cet article. Le système a été écrit pour tirer pleinement parti des avantages architecturaux fournis par Direct3D 10. Pour plus d’informations sur son utilisation, consultez la section [effets (Direct3D 10)](d3d10-graphics-programming-guide-effects.md) .

### <a name="hlsl-without-effects"></a>HLSL sans effets

Le pipeline de nuanceur Direct3D 10 peut être piloté sans l’utilisation du système d’effets Direct3D 10. Notez que dans ce cas, toutes les liaisons de tampon, de nuanceur, d’échantillonneur et de texture de constante doivent être gérées par l’application elle-même. Pour plus d’informations, consultez l’exemple de lien et les sections suivantes de ce document :

[Exemple HLSL sans effets](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)

### <a name="shader-compilation"></a>Compilation du nuanceur

Le compilateur HLSL Direct3D 10 apporte des améliorations à la définition du langage HLSL et peut donc fonctionner en 2 modes. Pour une prise en charge complète de la sémantique et des fonctions intrinsèques de style Direct3D 9, la compilation doit être appelée à l’aide de l’indicateur de MODE de compatibilité qui peut être spécifié pour chaque compilation.

Le modèle de nuanceur 4,0 une sémantique spécifique du langage HLSL et des fonctions intrinsèques pour Direct3D 10 est disponible en [HLSL](../direct3dhlsl/dx-graphics-hlsl.md). Les modifications majeures apportées à la syntaxe de Direct3D 9 HLSL pour prendre le plus de note de se trouvent dans le domaine de l’accès aux textures. La nouvelle syntaxe est la seule forme prise en charge par le compilateur en dehors du mode de compatibilité.

> [!Note]  
> Les API de type compilateur Direct3D 10 ([**D3D10CompileShader**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-d3d10compileshader) et [**D3D10CompileEffectFromMemory**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-d3d10compileeffectfrommemory)) sont fournies par les runtimes Direct3D 10, 10,1 et 11 qui s’exécutent dans Windows Vista et versions ultérieures. Les API de type compilateur Direct3D 10 ont les mêmes fonctionnalités que le compilateur HLSL fourni dans le kit de développement logiciel (SDK) DirectX (décembre 2006). Ce compilateur HLSL ne prend pas en charge les profils Direct3D 10,1 (vs \_ 4 \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1, FX \_ 4 \_ 1) et il manque un certain nombre d’optimisations et d’améliorations. Vous pouvez vous procurer un compilateur HLSL qui prend en charge les profils Direct3D 10,1 de la dernière version héritée de [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)). Pour plus d’informations sur le SDK DirectX hérité, consultez [où est le kit de développement logiciel (SDK) DirectX ?](../directx-sdk--august-2009-.md). Vous pouvez vous procurer la dernière version du compilateur de ligne de commande Fxc.exe HLSL et des API [D3DCompiler](../direct3dhlsl/dx-graphics-d3dcompiler-reference.md) à partir du SDK Windows.

 

### <a name="creation-of-shader-resources"></a>Création de ressources de nuanceur

La création d’instances de nuanceur compilées en dehors du système d’effets Direct3D 10 s’effectue de façon très similaire à Direct3D 9. Toutefois, dans Direct3D 10, il est important de conserver la signature d’entrée du nuanceur pour une utilisation ultérieure. La signature est retournée par défaut dans le cadre de l’objet blob de nuanceur, mais peut être extraite pour réduire les besoins en mémoire si nécessaire. Pour plus d’informations, consultez [utilisation de nuanceurs dans Direct3D 10](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).

### <a name="shader-reflection-layer-interface"></a>Interface de couche de réflexion du nuanceur

La couche de réflexion du nuanceur est l’interface par laquelle les informations sur les spécifications du nuanceur peuvent être obtenues. Cela s’avère particulièrement utile lors de la création de liens d’assembly d’entrée (voir ci-dessous) où vous devrez peut-être traverser les spécifications d’entrée du nuanceur pour vous assurer que vous fournissez la structure d’entrée correcte au nuanceur. Vous pouvez créer une instance de l’interface de la couche réflexion en même temps que la création d’une instance d’un nuanceur compilé.

La couche de réflexion du nuanceur remplace les méthodes D3DX9 qui offrent des fonctionnalités similaires. Par exemple, [**IsParameterUsed**](../direct3d9/id3dxeffect--isparameterused.md) est remplacé par la méthode [**GetDesc**](/windows/desktop/api/D3D10Shader/nf-d3d10shader-id3d10shaderreflectionvariable-getdesc) .

### <a name="input-assembler-layouts---vertex-shader--input-stream-linkage"></a>Dispositions de l’assembleur d’entrée-liaison de nuanceur de sommets/flux d’entrée

L’assembleur d’entrée (IA) remplace la déclaration de flux de vertex de style Direct3D 9 et sa structure de description est très similaire dans la forme. La principale différence réside dans le fait que l’objet de disposition IA créé doit être directement mappé à un format spécifique de signature d’entrée de nuanceur. L’objet de mappage créé pour lier le flux d’entrée au nuanceur peut être utilisé sur un nombre quelconque de nuanceurs où la signature d’entrée du nuanceur correspond à celle du nuanceur utilisé pour créer la disposition d’entrée.

Pour optimiser le pipeline avec des données statiques, vous devez considérer les permutations du format de flux d’entrée par rapport aux signatures d’entrée de nuanceur possibles et créer les instances d’objet de disposition IA aussi tôt que possible et les réutiliser dans la mesure du possible.

### <a name="impact-of-shader-dead-code-removal"></a>Impact de la suppression du code mort du nuanceur

La section suivante décrit en détail une différence significative entre Direct3D 9 et Direct3D 10, qui est susceptible de nécessiter une gestion soigneuse dans le code de votre moteur. Les nuanceurs qui contiennent des expressions conditionnelles ont souvent certains chemins de code supprimés dans le cadre du processus de compilation. Dans Direct3D 9, deux types d’entrées peuvent être supprimés (marquées pour suppression) en cas d’inutilisation : entrées de signature (comme l’exemple ci-dessous) et entrées constantes. Si la fin de la mémoire tampon constante contient des entrées inutilisées, la déclaration de taille dans le nuanceur reflète la taille de la mémoire tampon constante sans les entrées inutilisées à la fin. Ces deux types d’entrées restent dans les signatures ou les mémoires tampons constantes Direct3D 10 avec une exception spéciale dans le cas d’entrées constantes inutilisées à la fin d’une mémoire tampon constante. Cela peut avoir un impact sur le moteur lors de la gestion de grands nuanceurs et de la création de dispositions d’entrée. Les éléments supprimés par les optimisations du code mort dans le compilateur doivent toujours être déclarés dans la structure d’entrée. Cela est illustré par l'exemple suivant :

### <a name="vertex-shader-input-structure-example"></a>Exemple de structure d’entrée de nuanceur de sommets


```
struct VS_INPUT
{
float4 pos: SV_Position;
float2 uv1 : Texcoord1;
float2 uv2 : Texcoord2; *
};
```



\* La suppression du code mort de Direct3D 9 supprime la déclaration dans le nuanceur en raison de la suppression du code mort conditionnel


```
float4x4  g_WorldViewProjMtx;
static const bool g_bLightMapped = false; // define a compile time constant

VS_INPUT main(VS_INPUT i) 
{
    VS_INPUT o;
    o.pos = mul( i.pos, g_WorldViewProjMtx);
    o.uv1 = i.uv1;
    if ( g_bLightMapped )
    {
        o.uv2 = i.uv2;
    }
    return o;
}
```



Ou bien, il peut être plus évident que la constante est une constante au moment de la compilation avec la déclaration suivante :


```
#define LIGHT_MAPPED false
```



Dans l’exemple ci-dessus, sous Direct3D 9, l’élément UV2 serait supprimé en raison des optimisations du code mort dans le compilateur. Sous Direct3D 10, le code mort sera toujours supprimé, mais la disposition de l’assembleur d’entrée du nuanceur requiert la définition des données d’entrée. La couche de réflexion du nuanceur fournit les moyens de gérer cette situation de façon générique, ce qui vous permet de traverser les spécifications d’entrée du nuanceur et de vous assurer que vous fournissez une description complète du flux d’entrée au mappage de signature du nuanceur.

Voici un exemple de fonction pour détecter l’existence d’un nom ou d’un index sémantique dans une signature de fonction :


```
// Returns true if the SemanticName / SemanticIndex is used in the input signature.
// pReflector is a previously acquired shader reflection interface.
bool IsSignatureElementExpected(ID3D10ShaderReflection *pReflector, const LPCSTR SemanticName, UINT SemanticIndex)
{
    D3D10_SHADER_DESC               shaderDesc;
    D3D10_SIGNATURE_PARAMETER_DESC  paramDesc;

    Assert(pReflector);
    Assert(SemanticName);

    pReflector->GetDesc(&shaderDesc);

    for (UINT k=0; k<shaderDesc.InputParameters; k++)
    {
        pReflector->GetInputParameterDesc( k, &paramDesc);
        if (wcscmp( SemanticName, paramDesc.SemanticName)==0 && paramDesc.SemanticIndex == SemanticIndex) 
            return true;
    }

    return false;
}
```



### <a name="state-object-creation"></a>Création d’un objet d’État

Lors du Portage du code du moteur, il peut être utile d’utiliser initialement un ensemble d’objets d’État par défaut et de désactiver tous les paramètres d’état de texture/état de rendu de l’appareil Direct3D 9. Cela entraînera des artefacts de rendu, mais est le moyen le plus rapide d’exécuter et d’exécuter des tâches. Vous pouvez par la suite construire un système de gestion d’objets d’État qui peut utiliser une clé composée pour permettre la réutilisation maximale du nombre d’objets d’état utilisés.

## <a name="porting-textures"></a>Portage des textures

### <a name="file-formats-supported"></a>Formats de fichier pris en charge

Les fonctions **D3DXxxCreateXXX** et **D3DXxxSaveXXX** qui créent ou enregistrent une texture depuis ou vers un fichier graphique (par exemple, [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)) prennent en charge un autre ensemble de formats de fichier dans Direct3D 10 que dans Direct3D 9 :



| Format de fichier | Direct3D 9 | Direct3D 10 |
|-------------|------------|-------------|
| .bmp        | x          | x           |
| .jpg        | x          | x           |
| .tga        | x          |             |
| .png        | x          | x           |
| .dds        | x          | x           |
| . ppm        | x          |             |
| .dib        | x          |             |
| . HDR        | x          |             |
| . PFM        | x          |             |
| .tiff       |            | x           |
| .gif        |            | x           |
| .tif        |            | x           |



 

Pour plus d’informations, comparez les énumérations de [**D3DXIMAGE \_ FILEFORMAT**](../direct3d9/d3dximage-fileformat.md) de Direct3D 9 avec les énumérations de [**\_ \_ \_ format de fichier image d3dx10**](d3dx10-image-file-format.md) pour Direct3D 10.

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8. Pour le traitement des fichiers de texture, nous vous recommandons d’utiliser [DirectXTex](https://github.com/Microsoft/DirectXTex).

 

### <a name="mapping-texture-formats"></a>Mappage des formats de texture

Le tableau suivant montre le mappage des formats de texture de Direct3D 9 vers Direct3D 10. Tout contenu dans les formats non disponibles dans DXGI doit être converti par les routines de l’utilitaire.



| Format Direct3D 9                   | Format Direct3D 10                                                                                                                                                                                                                                   |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFMT \_ inconnu                     | \_format dxgi \_ inconnu                                                                                                                                                                                                                                |
| D3DFMT \_ R8G8B8                      | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A8R8G8B8                    | DXGI \_ format \_ B8G8R8A8 \_ UNORM & dxgi \_ format \_ B8G8R8A8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ X8R8G8B8                    | DXGI \_ format \_ B8G8R8X8 \_ UNORM & dxgi \_ format \_ B8G8R8X8 \_ UNORM \_ sRGB ¹                                                                                                                                                                                 |
| D3DFMT \_ R5G6B5                      | \_Format dxgi \_ B5G6R5 \_ UNORM ²                                                                                                                                                                                                                         |
| D3DFMT \_ X1R5G5B5                    | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A1R5G5B5                    | \_Format dxgi \_ B5G5R5A1 \_ UNORM ²                                                                                                                                                                                                                       |
| D3DFMT \_ A4R4G4B4                    | DXGI \_ format \_ B4G4R4A4 \_ UNORM ³                                                                                                                                                                                                                       |
| D3DFMT \_ R3G3B2                      | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ a8                          | \_Format dxgi \_ a8 \_ UNORM                                                                                                                                                                                                                              |
| D3DFMT \_ A8R3G3B2                    | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X4R4G4B4                    | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A2B10G10R10                 | DXGI \_ format \_ R10G10B10A2                                                                                                                                                                                                                            |
| D3DFMT \_ A8B8G8R8                    | DXGI \_ format \_ R8G8B8A8 \_ UNORM & dxgi \_ R8G8B8A8 \_ \_ UNORM \_ sRGB                                                                                                                                                                                  |
| D3DFMT \_ X8B8G8R8                    | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ G16R16                      | DXGI \_ format \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DFMT \_ A2R10G10B10                 | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A16B16G16R16                | DXGI \_ format \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DFMT \_ A8P8                        | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ P8                          | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ N8                          | \_Format dxgi \_ R8 \_ UNORM Remarque : utilisez. r Swizzle dans le nuanceur pour dupliquer le rouge sur d’autres composants afin d’atteindre le comportement de d3d9.                                                                                                                                    |
| D3DFMT \_ A8L8                        | DXGI \_ format \_ R8G8 \_ UNORM Remarque : utilisez Swizzle. rrrg dans le nuanceur pour dupliquer la couleur rouge et déplacer le vert vers les composants alpha pour atteindre le comportement d3d9.                                                                                                            |
| D3DFMT \_ A4L4                        | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ V8U8                        | \_Format dxgi \_ R8G8 \_ ronfler                                                                                                                                                                                                                            |
| D3DFMT \_ L6V5U5                      | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X8L8V8U8                    | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ Q8W8V8U8                    | \_Format dxgi \_ R8G8B8A8 \_ ronfler                                                                                                                                                                                                                        |
| D3DFMT \_ V16U16                      | \_Format dxgi \_ R16G16 \_ ronfler                                                                                                                                                                                                                          |
| D3DFMT \_ W11V11U10                   | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ A2W10V10U10                 | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ UYVY                        | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ R8G8 \_ B8G8                  | DXGI \_ format \_ G8R8 \_ G8B8 \_ UNORM (dans virtuel DX9, les données ont été mises à l’échelle par 255.0 f, mais cela peut être géré dans le code du nuanceur).                                                                                                                                   |
| D3DFMT \_ YUY2                        | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ G8R8 \_ G8B8                  | DXGI \_ format \_ R8G8 \_ B8G8 \_ UNORM (dans virtuel DX9, les données ont été mises à l’échelle par 255.0 f, mais cela peut être géré dans le code du nuanceur).                                                                                                                                   |
| D3DFMT \_ DXT1                        | DXGI \_ format \_ BC1 \_ UNORM & dxgi \_ BC1 \_ \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT2                        | DXGI \_ format \_ BC1 \_ UNORM & dxgi \_ format \_ BC1 \_ UNORM \_ sRVB Remarque : DXT1 et DXT2 sont les mêmes d’une perspective API/matérielle... seule la différence était « prémultipliée alpha », qui peut être suivie par une application et n’a pas besoin d’un format distinct. |
| D3DFMT \_ DXT3                        | DXGI \_ format \_ BC2 \_ UNORM & dxgi \_ BC2 \_ \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ DXT4                        | DXGI \_ format \_ BC2 \_ UNORM & dxgi \_ format \_ BC2 \_ UNORM \_ sRVB Remarque : DXT3 et DXT4 sont les mêmes d’une perspective API/matérielle... seule la différence était « prémultipliée alpha », qui peut être suivie par une application et n’a pas besoin d’un format distinct. |
| D3DFMT \_ DXT5                        | DXGI \_ format \_ BC3 \_ UNORM & dxgi \_ BC3 \_ \_ UNORM \_ sRGB                                                                                                                                                                                            |
| D3DFMT \_ D16 & D3DFMT \_ D16 \_ verrouillable | DXGI \_ format \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ d32                         | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D15S1                       | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24S8                       | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X8                       | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D24X4S4                     | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ D16                         | DXGI \_ format \_ D16 \_ UNORM                                                                                                                                                                                                                             |
| D3DFMT \_ D32F \_ verrouillable              | DXGI \_ format \_ d32 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ D24FS8                      | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ S1D15                       | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ S8D24                       | DXGI \_ format \_ D24 \_ UNORM \_ S8 \_ uint                                                                                                                                                                                                                   |
| D3DFMT \_ X8D24                       | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ X4S4D24                     | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ L16                         | DXGI \_ format \_ R16 \_ UNORM Remarque : utilisez le Swizzle. r dans le nuanceur pour dupliquer le rouge sur d’autres composants afin d’atteindre le comportement d3d9.                                                                                                                                   |
| D3DFMT \_ INDEX16                     | DXGI \_ format \_ R16 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ INDEX32                     | DXGI \_ format \_ R32 \_ uint                                                                                                                                                                                                                              |
| D3DFMT \_ Q16W16V16U16                | \_Format dxgi \_ R16G16B16A16 \_ ronfler                                                                                                                                                                                                                    |
| D3DFMT \_ MULTI2 \_ ARGB8               | Non disponible                                                                                                                                                                                                                                        |
| D3DFMT \_ R16F                        | DXGI \_ format \_ R16 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ G16R16F                     | DXGI \_ format \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DFMT \_ A16B16G16R16F               | DXGI \_ format \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| D3DFMT \_ R32F                        | DXGI \_ format \_ R32 \_ float                                                                                                                                                                                                                             |
| D3DFMT \_ G32R32F                     | DXGI \_ format \_ R32G32 \_ float                                                                                                                                                                                                                          |
| D3DFMT \_ A32B32G32R32F               | DXGI \_ format \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DFMT \_ CxV8U8                      | Non disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT1                 | DXGI \_ format \_ R32 \_ float                                                                                                                                                                                                                             |
| D3DDECLTYPE \_ FLOAT2                 | DXGI \_ format \_ R32G32 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT3                 | DXGI \_ format \_ R32G32B32 \_ float                                                                                                                                                                                                                       |
| D3DDECLTYPE \_ float4                 | DXGI \_ format \_ R32G32B32A32 \_ float                                                                                                                                                                                                                    |
| D3DDECLTYPED3DCOLOR                 | Non disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ UBYTE4                 | DXGI \_ format \_ R8G8B8A8 \_ uint Remarque : Shader obtient des valeurs uint, mais si les valeurs float intégral de style Direct3D 9 sont nécessaires (0.0 f, 1.0 f... 255. f), UINT peut simplement être converti en float32 dans le nuanceur.                                                               |
| D3DDECLTYPE \_ SHORT2                 | \_Format dxgi \_ R16G16 \_ Saint Note : le nuanceur obtient des valeurs de Saint-est, mais si les valeurs float de style intégral Direct3D 9 sont nécessaires, Saint-est tout simplement converti en float32 dans le nuanceur.                                                                                       |
| D3DDECLTYPE \_ SHORT4                 | \_Format dxgi \_ R16G16B16A16 \_ Saint Note : le nuanceur obtient des valeurs de Saint-est, mais si les valeurs float de style intégral Direct3D 9 sont nécessaires, Saint-est tout simplement converti en float32 dans le nuanceur.                                                                                 |
| D3DDECLTYPE \_ UBYTE4N                | DXGI \_ format \_ R8G8B8A8 \_ UNORM                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ SHORT2N                | \_Format dxgi \_ R16G16 \_ ronfler                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ SHORT4N                | \_Format dxgi \_ R16G16B16A16 \_ ronfler                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ USHORT2N               | DXGI \_ format \_ R16G16 \_ UNORM                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ USHORT4N               | DXGI \_ format \_ R16G16B16A16 \_ UNORM                                                                                                                                                                                                                    |
| D3DDECLTYPE \_ UDEC3                  | Non disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ DEC3N                  | Non disponible                                                                                                                                                                                                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2             | DXGI \_ format \_ R16G16 \_ float                                                                                                                                                                                                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4             | DXGI \_ format \_ R16G16B16A16 \_ float                                                                                                                                                                                                                    |
| FourCC 'ATI1'                       | DXGI \_ format \_ textures BC4 \_ UNORM                                                                                                                                                                                                                             |
| FourCC 'ATI2'                       | DXGI \_ format \_ BC5 \_ UNORM                                                                                                                                                                                                                             |



 

¹ DXGI 1,1, inclus dans le runtime Direct3D 11, inclut les formats BGRA. Toutefois, la prise en charge de ces formats est facultative pour les appareils Direct3D 10 et 10,1 avec des pilotes qui sont implémentés sur le modèle WDDM (Windows Display Driver Model) pour Windows Vista (WDDM 1,0). Envisagez d’utiliser DXGI au \_ format \_ R8G8B8A8 UNORM à la \_ place. Vous pouvez également créer votre appareil avec la [**\_ \_ \_ \_ prise en charge D3D10 créer un appareil BGRA**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) pour vous assurer que vous ne prenez en charge que les ordinateurs avec le runtime Direct3D 11,0 et un pilote WDDM 1,1 ou une version ultérieure.

² DXGI 1,0 définis 5:6:5 et 5:5:5:1 formats, mais ils n’étaient pas pris en charge par le runtime Direct3D 10. x ou Direct3D 11,0. Ces formats sont éventuellement pris en charge avec DXGI 1,2 dans le runtime DirectX 11,1, qui est requis pour les cartes vidéo de niveau de fonctionnalité 11,1 et le WDDM 1,2 (afficher le modèle de pilote à partir de Windows 8) et déjà pris en charge sur les niveaux de fonctionnalité 10level9.

³ DXGI 1,2 a introduit le format 4:4:4:4. Ce format est éventuellement pris en charge dans le runtime DirectX 11,1, qui est requis pour les cartes vidéo de niveau de fonctionnalité 11,1 et les pilotes WDDM 1,2, et déjà pris en charge sur les niveaux de fonctionnalité 10level9.

Pour les formats non compressés, DXGI a limité la prise en charge des modèles de format de pixel arbitraires. tous les formats non compressés doivent être de type RVBA. Cela peut nécessiter la swizzling des formats de pixel actifs existants, que nous vous recommandons de calculer comme un test de prétraitement hors connexion lorsque cela est possible.

## <a name="porting-shaders"></a>Portage des nuanceurs

### <a name="direct3d-10-shaders-are-authored-in-hlsl"></a>Les nuanceurs Direct3D 10 sont créés en HLSL

Direct3D 10 limite l’utilisation du langage assembleur uniquement à des fins de débogage. par conséquent, tous les nuanceurs d’assembly écrits à la main utilisés dans Direct3D 9 devront être convertis en langage HLSL.

### <a name="shader-signatures-and-linkage"></a>Signatures et liaison de nuanceur

Nous avons abordé les conditions requises pour la liaison d’assembly d’entrée aux signatures d’entrée de nuanceur vertex plus haut dans ce document (voir ci-dessus). Notez que le runtime Direct3D 10 a également renforcé la configuration requise pour la liaison intermédiaire entre les nuanceurs. Cette modification affecte les sources de nuanceur dans lesquelles la liaison entre les étapes peut ne pas avoir été entièrement décrite sous Direct3D 9. Par exemple :


```
VS_OUTPUT                       PS_INPUT
float4   pos : SV_POSITION;     float4 pos : SV_POSITION;
float4   uv1 : TEXCOORD1;       float4 uv1 : TEXCOORD1;
float4x3 tangentSp : TEXCOORD2; float4 tangent : TEXCOORD2; *
float4   Color : TEXCOORD6;     float4 color : TEXCOORD6;
```



\* Liaison VS-PS rompue-même si le nuanceur de pixels peut ne pas être intéressé par la matrice complète, la liaison doit spécifier la float4x3 complète.

Notez que la sémantique de liaison entre les étapes doit correspondre exactement, mais les entrées de étapes cibles peuvent être un préfixe des valeurs en cours de sortie. Dans l’exemple ci-dessus, le nuanceur de pixels peut avoir la position et texcoord1 comme les seules entrées, mais il n’a pas pu avoir la position et texcoord2 comme seules entrées en raison des contraintes de classement.

### <a name="hlsl-shader-stage-linkages"></a>Liaisons d’étape de nuanceur HLSL

La liaison entre les nuanceurs peut se produire à n’importe quel point suivant dans le pipeline :

-   Assembleur d’entrée au nuanceur de sommets
-   Nuanceur de sommets vers nuanceur de pixels
-   Nuanceur de sommets au nuanceur Geometry
-   Nuanceur vertex pour la sortie de flux
-   Nuanceur de géométrie à nuanceur de pixels
-   Nuanceur Geometry à diffuser en continu

### <a name="constant-buffers"></a>Mémoires tampons constantes

Pour faciliter le portage de contenu à partir de Direct3D 9, une approche initiale de la gestion constante en dehors du système d’effets peut impliquer la création d’une seule mémoire tampon constante contenant toutes les constantes requises. Il est important pour les performances de classer les constantes dans les tampons selon la fréquence attendue de la mise à jour. Cette organisation réduira la quantité de jeux de constantes redondants au minimum.

### <a name="user-clip-planes-in-hlsl-on-feature-level-9-and-higher"></a>Plans d’utilisateur en HLSL sur le niveau de fonctionnalité 9 et versions ultérieures

À compter de Windows 8, vous pouvez utiliser l’attribut de fonction **clipplanes** dans une [déclaration de fonction](../direct3dhlsl/dx-graphics-hlsl-function-syntax.md) HLSL plutôt que [SV \_ ClipDistance](../direct3dhlsl/dx-graphics-hlsl-semantics.md) pour que votre nuanceur fonctionne sur le [niveau de fonctionnalité](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 x, ainsi que sur le niveau de \_ fonctionnalité 10 et ultérieur. Pour plus d’informations, consultez l' [image des plans d’utilisateur sur le matériel de niveau de fonctionnalité 9](../direct3dhlsl/user-clip-planes-on-10level9.md).

## <a name="additional-direct3d-10-differences-to-watch-for"></a>Autres différences Direct3D 10 à surveiller

### <a name="integers-as-input"></a>Entiers comme entrée

Dans Direct3D 9, il n’existait pas de prise en charge matérielle réelle pour les types de données Integer, mais le matériel Direct3D 10 prend en charge les types d’entiers explicites. Si vous avez des données à virgule flottante dans votre mémoire tampon de vertex, vous devez avoir une entrée float. Dans le cas contraire, un type entier sera la représentation du modèle de bits de la valeur à virgule flottante. Un type entier n’est pas autorisé pour une entrée de nuanceur de pixels, sauf si la valeur est marquée pour aucune interpolation (consultez [modificateurs d’interpolation](../direct3dhlsl/dx-graphics-hlsl-struct.md)).

### <a name="mouse-cursors"></a>Curseurs de la souris

Dans les versions précédentes de Windows, les routines de curseur de souris GDI standard ne fonctionnaient pas correctement sur tous les périphériques exclusifs en plein écran. Les API [**SetCursorProperties**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorproperties), [**ShowCursor**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-showcursor)et [**SetCursorPosition**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setcursorposition) ont été ajoutées pour gérer ces cas. Étant donné que la version de GDI de Windows Vista comprend entièrement les surfaces [dxgi](../direct3ddxgi/d3d10-graphics-programming-guide-dxgi.md) , il n’est pas nécessaire d’utiliser cette API de curseur de souris spécialisée pour qu’il n’y ait pas d’équivalent Direct3D 10. Les applications Direct3D 10 doivent à la place utiliser les [routines de curseur de souris GDI](../menurc/cursors.md) standard pour les curseurs de souris.

### <a name="mapping-texels-to-pixels-in-direct3d-10"></a>Mappage de texels à des pixels dans Direct3D 10

Dans Direct3D 9, les centres de texture et les centres de pixels étaient séparés par une demi-unité (consultez [mappage direct des texels à des pixels (Direct3D 9)](../direct3d9/directly-mapping-texels-to-pixels.md)). Dans Direct3D 10, les centres de texels sont déjà aux demi-unités, donc il n’est pas nécessaire de déplacer du tout des coordonnées de vertex.

Le rendu des quatre cœurs en plein écran est plus simple avec Direct3D 10. Les Quad-plein écran doivent être définis dans clipspace (-1, 1) et simplement transmis au nuanceur de sommets sans aucune modification. De cette façon, il n’est pas nécessaire de recharger votre mémoire tampon de vertex chaque fois que la résolution de l’écran change, et il n’y a pas de travail supplémentaire dans le nuanceur de pixels pour manipuler les coordonnées de la texture.

### <a name="reference-counting-behavior-changes"></a>Modifications du comportement du décompte de références

Contrairement aux versions Direct3D précédentes, les différentes fonctions set ne contiendront pas de référence aux objets périphériques. Cela signifie que l’application doit s’assurer qu’elle contient une référence sur l’objet aussi longtemps qu’il veut que cet objet soit lié au pipeline. Lorsque le nombre de références de l’objet est inférieur à zéro, l’objet est indépendant du pipeline lors de sa destruction. Ce style d’exploitation de référence est également connu sous le nom de maintien de référence faible. par conséquent, chaque emplacement de liaison sur l’objet appareil contient une référence faible à l’interface/l’objet. À moins d’être explicitement mentionné dans le cas contraire, ce comportement doit être utilisé pour toutes les méthodes Set. Chaque fois que la destruction d’un objet entraîne la définition d’un point de liaison sur la **valeur null** , la couche de débogage émet un avertissement. Notez que les appels aux méthodes d’extraction de périphérique, telles que [**OMGetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omgetrendertargets) , augmentent le nombre de références des objets retournés.

### <a name="test-cooperative-level"></a>Niveau de coopératif de test

La fonctionnalité de l’API Direct3D 9 [**TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) est analogue à la définition [du \_ \_ test de présentation dxgi](../direct3ddxgi/dxgi-present.md) lors de l’appel de [**présent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present).

### <a name="stretchrect"></a>StretchRect

Une fonction semblable à la méthode Direct3D 9 [**IDirect3DDevice9 :: StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) n’est pas disponible dans Direct3D 10 et 10,1. Pour copier des surfaces de ressource, utilisez [**ID3D10Device :: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion). Pour les opérations de redimensionnement, restituez sur une texture à l’aide du filtrage de texture. Pour convertir des surfaces MSAA en surfaces non MSAA, utilisez [**ID3D10Device :: ResolveSubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource).

## <a name="additional-direct3d-101-differences"></a>Différences Direct3D 10,1 supplémentaires

Windows Vista avec Service Pack 1 (SP1) comprenait une mise à jour mineure de Direct3D 10 et Direct3D 10,1, qui exposait les fonctionnalités matérielles supplémentaires suivantes :

-   Nuanceurs par exemple MSAA
-   Lecture de profondeur MSAA
-   Modes de fusion indépendants par cible de rendu
-   Tableaux de mappage de cube
-   Rendu aux formats compressés par bloc (BC)

La mise à jour Direct3D 10,1 a ajouté la prise en charge des nouvelles interfaces suivantes, qui sont dérivées des interfaces existantes :

-   [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)
-   [**ID3D10BlendState1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10blendstate1)
-   [**ID3D10ShaderResourceView1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1)

La mise à jour de Direct3D 10,1 incluait également les structures supplémentaires suivantes :

-   [**D3D10 \_ Render \_ cible \_ Blend \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_render_target_blend_desc1)
-   [**D3D10 \_ Blend \_ DESC1**](/windows/desktop/api/D3D10_1/ns-d3d10_1-d3d10_blend_desc1)
-   [**\_Affichage des ressources du nuanceur D3D10 \_ \_ \_ DESC1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1)

L’API Direct3D 10,1 comprend un nouveau concept nommé niveau de fonctionnalité. Ce concept signifie que vous pouvez utiliser l’API Direct3D 10,1 pour piloter le matériel Direct3D 10,0 ([**D3D10 \_ Feature \_ Level \_ 10 \_ 0**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)) ou Direct3D 10,1 ([**D3D10 \_ Feature \_ Level \_ 10 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)). Étant donné que l’API Direct3D 10,1 est dérivée des interfaces Direct3D 10, les applications peuvent créer un appareil Direct3D 10,1, puis l’utiliser en tant qu’appareil Direct3D 10,0, sauf si de nouvelles fonctionnalités spécifiques à 10,1 sont nécessaires (à condition que le niveau de fonctionnalité **D3D10 de \_ \_ niveau \_ 10 \_ 1** soit présent et prenne en charge ces fonctionnalités).

> [!Note]  
> Les périphériques Direct3D 10,1 peuvent utiliser les profils de nuanceur HLSL 10,0 existants (vs 4 \_ \_ 0, PS \_ 4 \_ 0, GS \_ 4 \_ 0) et les nouveaux profils 10,1 (vs 4 \_ \_ 1, PS \_ 4 \_ 1, GS \_ 4 \_ 1) avec des instructions et des fonctionnalités HLSL supplémentaires.

 

Windows 7 contenait une mise à jour mineure de l’API Direct3D 10,1 qui est incluse dans le runtime Direct3D 11. Cette mise à jour ajoute la prise en charge des niveaux de fonctionnalités suivants :

-   [**\_Niveau de fonctionnalité D3D10 \_ \_ 9 \_ 1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**\_Niveau de fonctionnalité D3D10 \_ \_ 9 \_ 2**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)
-   [**\_Niveau de fonctionnalité D3D10 \_ \_ 9 \_ 3**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1)

Windows 7 a également ajouté la prise en charge de Direct3D 10,1 pour la [plateforme de rastérisation avancée Windows (Warp)](../direct3darticles/directx-warp.md). Vous pouvez spécifier un pilote WARP à l’aide de la distorsion du [**\_ type de pilote \_ \_ D3D10**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

Pour plus d’informations sur Direct3D 10,1, consultez [fonctionnalités direct3d 10,1](d3d10-graphics-programming-guide-10-1.md) et l’énumération [**D3D10 \_ Feature \_ niveau1**](/windows/desktop/api/D3D10_1/ne-d3d10_1-d3d10_feature_level1) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation pour Direct3D 10](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
