---
title: Syntaxe des variables
description: Utilisez les règles de syntaxe suivantes pour déclarer des variables HLSL.
ms.assetid: 684c42d1-2dd4-42e1-9cff-580edb5c6bcd
keywords:
- extern, syntaxe de variable (DirectX HLSL)
- nointerpolation, syntaxe de variable (DirectX HLSL)
- Syntaxe Shared, variable (DirectX HLSL)
- groupshared, syntaxe de variable (DirectX HLSL)
- Syntaxe des variables statiques (DirectX HLSL)
- Syntaxe uniforme et variable (DirectX HLSL)
- volatile, syntaxe de variable (DirectX HLSL)
- Syntaxe précise et variable (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0ce89287d969683b72eb6db6d352300ce5295852
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481165"
---
# <a name="variable-syntax"></a>Syntaxe des variables

Utilisez les règles de syntaxe suivantes pour déclarer des variables HLSL.

\[*Stockage \_* Nom du type de \] \[ *\_ modificateur* de type de classe \]  \[ *index* \] \[ *: sémantique* \] \[ *: Packoffset* \] \[ *: Register* \] ;    \[ *Annotations* \] \[ *= Initial \_ Valeur*                    \]



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="Storage_Class_"></span><span id="storage_class_"></span><span id="STORAGE_CLASS_"></span>*Stockage \_ Type* 
</dt> <dd>

Modificateurs de classe de stockage facultatifs qui fournissent les indications du compilateur sur la portée de la variable et la durée de vie ; les modificateurs peuvent être spécifiés dans n’importe quel ordre.




| Valeur | Description | 
|-------|-------------|
| <strong>extern</strong> | Marquez une variable globale comme entrée externe pour le nuanceur. Il s’agit du marquage par défaut pour toutes les variables globales. Ne peut pas être combiné avec <strong>static</strong>. | 
| <strong>nointerpolation</strong> | N’interpolez pas les sorties d’un nuanceur de sommets avant de les passer à un nuanceur de pixels. | 
| <strong>établir</strong> | Le mot clé <strong>precis</strong> lorsqu’il est appliqué à une variable limite les calculs utilisés pour produire la valeur assignée à cette variable des manières suivantes : * les opérations distinctes sont conservées séparément. Par exemple, lorsqu’une opération mul et Add peut avoir été fusionnée dans une opération Mad, <strong>precise</strong> force les opérations à rester séparées. Au lieu de cela, vous devez utiliser explicitement la fonction intrinsèque Mad. * l’ordre des opérations est conservé. Lorsque l’ordre des instructions peut avoir été aléatoire pour améliorer les performances, la <strong>précision</strong> garantit que le compilateur conserve la commande comme écrit. * les opérations non sécurisées IEEE sont restreintes. Là où le compilateur peut avoir utilisé des opérations mathématiques rapides qui ne concernent pas les valeurs NaN (not a Number) et INF (infini), force <strong>précisément</strong> les exigences IEEE relatives aux valeurs NaN et INF à respecter. Sans <strong>précision</strong>, ces optimisations et opérations mathématiques ne sont pas compatibles IEEE. * la qualification d’une variable <strong>précise</strong> ne rend pas les opérations qui utilisent la variable avec <strong>précision</strong>. Étant donné que <strong>precise</strong> se propage uniquement aux opérations qui contribuent aux valeurs affectées à la variable qualifiée <strong>précise</strong>, <strong>il peut être</strong> difficile de déterminer correctement les calculs souhaités. nous vous recommandons donc de marquer les sorties du nuanceur avec <strong>précision</strong> directement là où vous les déclarez, si celles-ci se trouvent sur un champ de structure, ou sur un paramètre de sortie ou le type de retour de La possibilité de contrôler les optimisations de cette façon maintient l’invariance de résultat pour la variable de sortie modifiée en désactivant les optimisations qui peuvent affecter les résultats finaux en raison de différences de différences de précision accumulée. Il est utile lorsque vous souhaitez que les nuanceurs de facettes maintiennent des jointures de patch hermétiques ou des valeurs de profondeur de correspondance sur plusieurs passes. [Exemple de code](https://github.com/microsoft/DirectXShaderCompiler/blob/master/tools/clang/test/HLSLFileCheck/hlsl/types/modifiers/precise/precise4.hlsl): ```HLSLmatrix g_mWorldViewProjection;void main(in float3 InPos : Position, out precise float4 OutPos : SV_Position){  // operation is precise because it contributes to the precise parameter OutPos  OutPos = mul( float4( InPos, 1.0 ), g_mWorldViewProjection );}``` | 
| <strong>partagé</strong> | Marquer une variable pour le partage entre les effets ; Il s’agit d’un indicateur pour le compilateur. | 
| <strong>groupshared</strong> | Marquez une variable pour la mémoire partagée de groupe de threads pour les nuanceurs de calcul. Dans D3D10, la taille totale maximale de toutes les variables avec la classe de stockage groupshared est de 16 Ko, dans D3D11 la taille maximale est de 32 Ko. Consultez les exemples. | 
| <strong>static</strong> | Marquez une variable locale pour qu’elle soit initialisée une fois et persiste entre les appels de fonction. Si la déclaration n’inclut pas d’initialiseur, la valeur est égale à zéro. Une variable globale marquée comme <strong>static</strong> n’est pas visible pour une application. | 
| <strong>uniforme</strong> | Marquer une variable dont les données sont constantes tout au long de l’exécution d’un nuanceur (par exemple, une couleur de matériau dans un nuanceur de sommets); les variables globales sont considérées comme <strong>uniformes</strong> par défaut. | 
| <strong>volatile</strong> | Marquer une variable qui change fréquemment ; Il s’agit d’un indicateur pour le compilateur. Ce modificateur de classe de stockage s’applique uniquement à une variable locale.<br /><blockquote>[!Note]<br />Le compilateur HLSL ignore actuellement ce modificateur de classe de stockage.</blockquote><br /> | 




 

</dd> <dt>

<span id="Type_Modifier"></span><span id="type_modifier"></span><span id="TYPE_MODIFIER"></span>*\_Modificateur de type*
</dt> <dd>

Modificateur de type variable facultatif.



| Valeur             | Description                                                                                                                                                                                                                                  |
|-------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **const**         | Marquer une variable qui ne peut pas être modifiée par un nuanceur, par conséquent, elle doit être initialisée dans la déclaration de la variable. Les variables globales sont considérées comme **const** par défaut (supprimez ce comportement en fournissant l’indicateur/GEC au compilateur). |
| **ligne \_ principale**    | Marquer une variable qui stocke quatre composants sur une seule ligne afin qu’ils puissent être stockés dans un seul registre de constantes.                                                                                                                             |
| **colonne \_ principale** | Marquez une variable qui stocke 4 composants dans une seule colonne pour optimiser les mathématiques de matrice.                                                                                                                                                         |



 

> [!Note]  
> Si vous ne spécifiez pas de valeur de modificateur de type, le compilateur utilise la **colonne \_ principale** comme valeur par défaut.

 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>*Entrer*
</dt> <dd>

Tout type HLSL listé dans [types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md).

</dd> <dt>

<span id="Name_Index_"></span><span id="name_index_"></span><span id="NAME_INDEX_"></span>*Nom* \[ *Index*\]
</dt> <dd>

Chaîne ASCII qui identifie de façon unique une variable de nuanceur. Pour définir un tableau facultatif, utilisez **index** pour la taille du tableau, qui est un entier positif = 1.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Équivalent*
</dt> <dd>

Informations d’utilisation de paramètre facultatives, utilisées par le compilateur pour lier les entrées et sorties du nuanceur. Il existe plusieurs [sémantiques](dx-graphics-hlsl-semantics.md) prédéfinies pour les nuanceurs de sommets et de pixels. Le compilateur ignore la sémantique, sauf si elles sont déclarées sur une variable globale, ou un paramètre passé dans un nuanceur.

</dd> <dt>

<span id="Packoffset"></span><span id="packoffset"></span><span id="PACKOFFSET"></span>*Packoffset*
</dt> <dd>

Mot clé facultatif pour la compression manuelle des constantes de nuanceur. Consultez [packoffset (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md).

</dd> <dt>

<span id="Register"></span><span id="register"></span><span id="REGISTER"></span>*Annuler*
</dt> <dd>

Mot clé facultatif permettant d’assigner manuellement une variable de nuanceur à un registre particulier. Consultez [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md).

</dd> <dt>

<span id="Annotation_s_"></span><span id="annotation_s_"></span><span id="ANNOTATION_S_"></span>*Annotation (s)*
</dt> <dd>

Métadonnées facultatives, sous la forme d’une chaîne, attachées à une variable globale. Une annotation est utilisée par l’infrastructure Effect et est ignorée par le langage HLSL. Pour plus d’informations sur la syntaxe, consultez [syntaxe d’annotation](/windows/desktop/direct3d10/d3d10-effect-annotation-syntax).

</dd> <dt>

<span id="Initial_Value"></span><span id="initial_value"></span><span id="INITIAL_VALUE"></span>*\_Valeur initiale*
</dt> <dd>

Valeur (s) initiale facultative (s); le nombre de valeurs doit correspondre au nombre de composants dans le *type*. Chaque variable globale marquée **extern** doit être initialisée avec une valeur littérale ; chaque variable marquée comme **static** doit être initialisée avec une constante.

Les variables globales qui ne sont pas marquées comme **static** ou **extern** ne sont pas compilées dans le nuanceur. Le compilateur ne définit pas automatiquement les valeurs par défaut pour les variables globales et ne peut pas les utiliser dans les optimisations. Pour initialiser ce type de variable globale, utilisez la réflexion pour obtenir sa valeur, puis copiez la valeur dans une mémoire tampon constante. Par exemple, vous pouvez utiliser la méthode [**ID3D11ShaderReflection :: GetVariableByName**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getvariablebyname) pour obtenir la variable, utiliser la méthode [**ID3D11ShaderReflectionVariable :: GetDesc**](/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflectionvariable-getdesc) pour obtenir la description de la variable de nuanceur et obtenir la valeur initiale du membre **DefaultValue** de la structure DESC de la [**\_ \_ variable \_ de nuanceur d3d11**](/windows/desktop/api/d3d11shader/ns-d3d11shader-d3d11_shader_variable_desc) . Pour copier la valeur dans la mémoire tampon constante, vous devez vous assurer que la mémoire tampon a été créée avec l’accès en écriture de l’UC ([**d3d11 \_ \_ l’accès \_**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_cpu_access_flag)en écriture de l’UC). Pour plus d’informations sur la création d’une mémoire tampon constante, consultez [How to : Create a constant buffer](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Vous pouvez également utiliser l' [infrastructure Effects](../direct3d11/d3d11-graphics-programming-guide-effects.md) pour traiter automatiquement la réflexion et définir la valeur initiale. Par exemple, vous pouvez utiliser la méthode [**ID3DX11EffectPass :: apply**](/windows/desktop/direct3d11/id3dx11effectpass-apply) .

</dd> </dl>

## <a name="examples"></a>Exemples

Voici plusieurs exemples de déclarations de variable de nuanceur.


```
float fVar;
```




```
float4 color;
float fVar = 3.1f;

int iVar[3];

int iVar[3] = {1,2,3};

uniform float4 position : SV_POSITION; 
const float4 lightDirection = {0,0,1};
      
```



### <a name="group-shared"></a>Groupe partagé

Le langage HLSL permet aux threads d’un nuanceur de calcul d’échanger des valeurs via la mémoire partagée. Le langage HLSL fournit des primitives de cloisonnement telles que [**GroupMemoryBarrierWithGroupSync**](groupmemorybarrierwithgroupsync.md), et ainsi de suite pour garantir l’ordre correct des lectures et des écritures dans la mémoire partagée dans le nuanceur et pour éviter les concurrences de données.

> [!Note]  
> Le matériel exécute des threads dans des groupes (distorsions ou frontaux Wave), et la synchronisation de cloisonnement peut parfois être omise pour améliorer les performances lorsque seuls les threads qui appartiennent au même groupe sont corrects. Toutefois, nous déconseillons vivement cette omission pour les raisons suivantes :
>
> -   Cette omission entraîne un code non portable, qui peut ne pas fonctionner sur du matériel et ne fonctionne pas sur les rastériseurs logiciels qui exécutent généralement des threads dans des groupes plus petits.
> -   Les améliorations de performances que vous pourriez atteindre avec cette omission seront mineures par rapport à l’utilisation de la barrière All-threads.

 

Dans Direct3D 10, il n’existe pas de synchronisation des threads lors de l’écriture dans **groupshared**, ce qui signifie que chaque thread est limité à un emplacement unique dans un tableau pour l’écriture. Utilisez la valeur système [SV \_ GroupIndex](dx-graphics-hlsl-semantics.md) pour indexer dans ce tableau lors de l’écriture afin de garantir que deux threads ne peuvent pas entrer en conflit. En termes de lecture, tous les threads ont accès à l’ensemble du tableau pour la lecture.


```
struct GSData
{
    float4 Color;
    float Factor;
}

groupshared GSData data[5*5*1];

[numthreads(5,5,1)]
void main( uint index : SV_GroupIndex )
{
    data[index].Color = (float4)0;
    data[index].Factor = 2.0f;
    GroupMemoryBarrierWithGroupSync();
    ...
}
```



### <a name="packing"></a>Colis

Compresser les sous-composants des vecteurs et des scalaires dont la taille est suffisamment grande pour empêcher le franchissement des limites du Registre. Par exemple, ils sont tous valides :


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
        
```



Impossible de mélanger les types de compression.

À l’instar du mot clé Register, un packoffset peut être spécifique à Target. La compression des sous-composants est uniquement disponible avec le mot clé packoffset, pas le mot clé Register. Dans une déclaration CBuffer, le mot clé Register est ignoré pour les cibles Direct3D 10, car il est supposé être pour la compatibilité multiplateforme.

Les éléments empaquetés peuvent se chevaucher et le compilateur n’émet aucune erreur ni aucun avertissement. Dans cet exemple, élément2 et Element3 se chevauchent avec Element1. x et Element1. y.


```
cbuffer MyBuffer
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c0);
    float1 Element3 : packoffset(c0.y);
}
        
```



Un exemple qui utilise packoffset est : [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Variables (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

