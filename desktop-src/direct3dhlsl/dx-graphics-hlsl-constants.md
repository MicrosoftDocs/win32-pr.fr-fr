---
title: Constantes de nuanceur (HLSL)
description: Dans le nuancier modèle 4, les constantes de nuanceur sont stockées dans une ou plusieurs ressources de mémoire tampon en mémoire.
ms.assetid: 89fe874a-8009-4901-bebe-2d9e45f894bb
keywords:
- cbuffer
- tbuffer
- mémoire tampon constante
- mémoire tampon de texture
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b2a6b2ffa9168e870aeb405badb6ff71b0a4a59b23d76947e56a9c085ed0107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726549"
---
# <a name="shader-constants-hlsl"></a>Constantes de nuanceur (HLSL)

Dans le nuancier modèle 4, les constantes de nuanceur sont stockées dans une ou plusieurs ressources de mémoire tampon en mémoire. Ils peuvent être organisés en deux types de mémoires tampons : des mémoires tampons constantes (cbuffers) et des mémoires tampons de texture (tbuffers). Les mémoires tampons constantes sont optimisées pour l’utilisation de variables constantes, ce qui est caractérisé par un accès à latence faible et des mises à jour plus fréquentes de l’UC. Pour cette raison, des restrictions supplémentaires sur la taille, la disposition et l’accès s’appliquent à ces ressources. Les mémoires tampons de texture sont accessibles comme les textures et s’exécutent mieux pour les données indexées arbitrairement. Quel que soit le type de ressource que vous utilisez, il n’existe aucune limite quant au nombre de mémoires tampons constantes ou de mémoires tampons de texture qu’une application peut créer.

La déclaration d’une mémoire tampon constante ou d’une mémoire tampon de texture ressemble beaucoup à celle d’une déclaration de structure en C, avec l’ajout des mots clés **Register** et **packoffset** pour l’affectation manuelle des registres ou l’empaquetage des données.



|                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------|
| *BufferType* \[ *Nom* \] \[: **Register**(b \# ) \] { *VariableDeclaration* \[ : **packoffset**(c \# . XYZW) \] ;      ... }; |



 

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="BufferType"></span><span id="buffertype"></span><span id="BUFFERTYPE"></span>*BufferType*
</dt> <dd>

\[dans \] le type de mémoire tampon.



| BufferType | Description     |
|------------|-----------------|
| cbuffer    | mémoire tampon constante |
| tbuffer    | mémoire tampon de texture  |



 

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomme*
</dt> <dd>

\[dans \] une chaîne ASCII facultative, contenant un nom de mémoire tampon unique.

</dd> <dt>

<span id="register_b__"></span><span id="REGISTER_B__"></span>**inscrire**(b \# )
</dt> <dd>

\[dans le \] mot clé facultatif, utilisé pour empaqueter manuellement des données constantes. Les constantes peuvent être empaquetées dans un registre uniquement dans une mémoire tampon constante, où le registre de départ est donné par le numéro de Registre ( *\#* ).

</dd> <dt>

<span id="VariableDeclaration"></span><span id="variabledeclaration"></span><span id="VARIABLEDECLARATION"></span>*VariableDeclaration*
</dt> <dd>

\[dans \] une déclaration de variable, semblable à une déclaration de membre de structure. Il peut s’agir d’un objet de type ou d’effet HLSL (à l’exception d’une texture ou d’un objet échantillonneur).

</dd> <dt>

<span id="packoffset_c_.xyzw_"></span><span id="PACKOFFSET_C_.XYZW_"></span>**packoffset**(c \# . XYZW)
</dt> <dd>

\[dans le \] mot clé facultatif, utilisé pour empaqueter manuellement des données constantes. Les constantes peuvent être compressées dans n’importe quelle mémoire tampon constante, où le numéro de Registre est donné par ( *\#* ). La compression de sous-composant (à l’aide de XYZW swizzling) est disponible pour les constantes dont la taille s’ajuste à un seul registre (ne pas traverser une limite de registre). Par exemple, un float4 ne peut pas être empaqueté dans un seul registre à partir du composant y car il ne tient pas dans un registre à quatre composants.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les mémoires tampons constantes réduisent la bande passante requise pour mettre à jour les constantes de nuanceur en permettant aux constantes de nuanceur d’être regroupées et validées en même temps plutôt que d’effectuer des appels individuels pour valider chaque constante séparément.

Une mémoire tampon constante est une ressource tampon spécialisée accessible comme une mémoire tampon. Chaque mémoire tampon constante peut contenir jusqu’à 4096 [vecteurs](dx-graphics-hlsl-vector.md); chaque vecteur contient jusqu’à 4 32 bits. Vous pouvez lier jusqu’à 14 mémoires tampons constantes par étape de pipeline (2 emplacements supplémentaires sont réservés à un usage interne).

Une mémoire tampon de texture est une ressource tampon spécialisée accessible comme une texture. L’accès aux textures (par rapport à l’accès aux tampons) peut avoir de meilleures performances pour les données indexées arbitrairement. Vous pouvez lier jusqu’à 128 tampons de texture par étape de pipeline.

Une ressource de mémoire tampon est conçue pour réduire la surcharge liée à la définition de constantes de nuanceur. L’infrastructure Effect (voir [**interface ID3D10Effect**](/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effect)) gère la mise à jour des mémoires tampons de constante et de texture, ou vous pouvez utiliser l’API Direct3D pour mettre à jour les mémoires tampons (pour plus d’informations, consultez [copie et accès aux données des ressources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-mapping) ). Une application peut également copier des données à partir d’une autre mémoire tampon (telle qu’une cible de rendu ou une cible de sortie de flux) dans une mémoire tampon constante.

Pour plus d’informations sur l’utilisation de mémoires tampons constantes dans une application D3D10, consultez [types de ressources (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) et [création de ressources de mémoire tampon (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).

Pour Morel d’informations sur l’utilisation de mémoires tampons constantes dans une application D3D11, consultez [Introduction aux mémoires tampons dans Direct3D 11](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-intro) et [Comment : créer une mémoire tampon constante](/windows/desktop/direct3d11/overviews-direct3d-11-resources-buffers-constant-how-to).

Une mémoire tampon constante ne nécessite pas la liaison d’une [vue](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views) au pipeline. Toutefois, une mémoire tampon de texture requiert une vue et doit être liée à un emplacement de texture (ou doit être liée à [**SetTextureBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-settexturebuffer) lors de l’utilisation d’un effet).

Il existe deux façons de compresser des données de constantes : à l’aide des mots clés [Register (DirectX HLSL)](dx-graphics-hlsl-variable-register.md) et [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .

Différences entre Direct3D 9 et Direct3D 10 et 11 :

- Contrairement à l’allocation automatique de constantes dans Direct3D 9, qui n’effectuait pas de compression et attribuaient à la place chaque variable à un ensemble de registres float4, les variables de constantes HLSL suivent les règles de compression dans Direct3D 10 et 11.



 

### <a name="organizing-constant-buffers"></a>Organisation de mémoires tampons constantes

Les mémoires tampons constantes réduisent la bande passante requise pour mettre à jour les constantes de nuanceur en permettant aux constantes de nuanceur d’être regroupées et validées en même temps plutôt que d’effectuer des appels individuels pour valider chaque constante séparément.

Pour optimiser l’utilisation des mémoires tampons constantes, classez les variables de nuanceur dans ces mémoires en fonction de la fréquence de leur mise à jour. Cela permet à une application de réduire la bande passante requise pour la mise à jour des constantes de nuanceur. Par exemple, un nuanceur peut déclarer deux mémoires tampons constantes et organiser les données en fonction de leur fréquence de mise à jour : les données qui doivent être mises à jour au niveau de chaque objet (par exemple, une matrice universelle) sont regroupées dans une mémoire tampon constante qui peut être mise à jour pour chaque objet. Cela est indépendant des données qui caractérisent une scène et est donc susceptible d’être mis à jour bien moins souvent (lorsque la scène change).


```
cbuffer myObject
{       
    float4x4 matWorld;
    float3   vObjectPosition;
    int      arrayIndex;
}
 
cbuffer myScene
{
    float3   vSunPosition;
    float4x4 matView;
}
        
```



### <a name="default-constant-buffers"></a>Mémoires tampons constantes par défaut

Deux mémoires tampons constantes par défaut sont disponibles, $Global et $Param. Les variables placées dans la portée globale sont ajoutées implicitement au $Global CBuffer, à l’aide de la même méthode de compression que celle utilisée pour cbuffers. Les paramètres uniformes de la liste de paramètres d’une fonction s’affichent dans le $Param mémoire tampon constante lorsqu’un nuanceur est compilé en dehors de l’infrastructure d’effets. En cas de compilation dans l’infrastructure Effects, toutes les uniformes doivent être résolues en variables définies dans la portée globale.

## <a name="examples"></a>Exemples

Voici un exemple de l' [exemple Skinning10](https://msdn.microsoft.com/library/Ee416429(v=VS.85).aspx) qui est une mémoire tampon de texture constituée d’un tableau de matrices.


```
tbuffer tbAnimMatrices
{
    matrix g_mTexBoneWorld[MAX_BONE_MATRICES];
};
      
```



Cet exemple de déclaration assigne manuellement une mémoire tampon constante pour commencer à un registre particulier et compresse également des éléments particuliers par sous-composants.


```
cbuffer MyBuffer : register(b3)
{
    float4 Element1 : packoffset(c0);
    float1 Element2 : packoffset(c1);
    float1 Element3 : packoffset(c1.y);
}
      
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

