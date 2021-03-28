---
title: LD (SM4-ASM)
description: Extrait des données de la mémoire tampon ou de la texture spécifiée sans aucun filtrage (par exemple, échantillonnage par points) à l’aide de l’adresse entière fournie. Les données sources peuvent provenir de n’importe quel type de ressource, autre que TextureCube.
ms.assetid: DEE9A55F-EDFE-478E-8169-5BF9C43E98AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaacc3d76d49cc2b3043d39036f0ff652d7b8794
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313684"
---
# <a name="ld-sm4---asm"></a>LD (SM4-ASM)

Extrait des données de la mémoire tampon ou de la texture spécifiée sans aucun filtrage (par exemple, échantillonnage par points) à l’aide de l’adresse entière fournie. Les données sources peuvent provenir de n’importe quel type de ressource, autre que TextureCube.



| LD \[ \_ aoffimmi (u, v, w) \] dest \[ . Mask \] , srcAddress \[ . Swizzle \] , srcResource \[ . Swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Élément                                                                                                               | Description                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[dans \] l’adresse du résultat de l’opération.<br/>                                                               |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>     | \[dans \] les coordonnées de texture nécessaires à l’exécution de l’exemple.<br/>                                                     |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[dans \] un registre de texture (t \# ) qui doit avoir été déclaré, identifiant la texture ou la mémoire tampon à partir de laquelle effectuer l’extraction.<br/> |



 

## <a name="remarks"></a>Notes

Cette instruction est une alternative simplifiée à l' [exemple](sample--sm4---asm-.md) d’instruction. Contrairement à l' **exemple**, **LD** peut également extraire des données de tampons. **LD** peut également extraire des ressources à plusieurs exemples (sur le nuanceur de pixels uniquement).

*srcAddress* fournit l’ensemble des coordonnées de texture nécessaires pour exécuter l’exemple sous la forme d’entiers non signés. Si *srcAddress* est en dehors de la plage \[ 0... ( \# texels dans la dimension-1) \] , le comportement hors limites est appelé, où **LD** retourne 0 dans tous les composants non manquants du format de *srcResource*, et la valeur par défaut pour les composants manquants. Une application qui souhaite obtenir un contrôle plus flexible sur le comportement de l’adresse hors limites doit utiliser l' **exemple** d’instruction à la place, car elle honore l’état de l’échantillonneur/de la mise en miroir/de la bordure/de la bordure.

*srcAddress. a* (pos-Swizzle) fournit toujours un niveau de mipmap d’entier non signé. Si la valeur est en dehors de la plage \[ 0... ( num miplevels a dans la ressource-1) \] ), le comportement hors limites est appelé. Si la ressource est une mémoire tampon, qui ne peut pas avoir de des mipmaps, *srcAddress. a* est ignoré.

*srcAddress. Go* (pos-Swizzle) est ignoré pour les mémoires tampons et les texture1D (non-tableau). *srcAddress. b* (pos-Swizzle) est ignoré pour les tableaux Texture1D et texture2Ds.

Pour les tableaux texture1D, *srcAddress. g* (pos-Swizzle) fournit l’index de tableau sous la forme d’un entier non signé. Si la valeur est en dehors de la plage d’index de tableau disponibles \[ 0... ( Array size-1) \] , alors le comportement hors limites est appelé.

Pour les tableaux texture2D, *srcAddress. b* (pos-Swizzle) fournit l’index de tableau, sinon avec la même sémantique que pour texture1D.

L’extraction de *t \#* qui n’a rien lié à elle retourne 0 pour tous les composants.

### <a name="address-offset"></a>Décalage d’adresse

Le \[ \_ suffixe aoffimmi (u, v, w) facultatif \] (décalage d’adresse par entier immédiat) indique que les coordonnées de texture pour le **LD** doivent être décalées par un jeu d’espaces de texture d’entier d’espace de texture immédiate fournis. Les valeurs littérales sont un ensemble de numéros de compléments de 4 bits 2, dont la plage d’entiers est comprise entre \[ -8 et 7 \] . Ce modificateur est défini uniquement pour texture1D/2D/3D, y compris les tableaux, et non pour les mémoires tampons.

Les décalages sont ajoutés aux coordonnées de texture, dans l’espace de Texel, par rapport au miplevel auquel le **LD** accède.

Les décalages d’adresse ne sont pas appliqués le long de l’axe de tableau des tableaux texture1D/2D.

Les composants *\_ aoffimmi v, w* sont ignorés pour texture1Ds.

Le composant *\_ aoffimmi w* est ignoré pour texture2Ds.

Étant donné que les coordonnées de texture pour **LD** sont des entiers non signés, si le décalage entraîne la sortie de l’adresse sous zéro, elle est renvoyée à une adresse de grande taille et entraîne un accès hors limites.

### <a name="return-type-control"></a>Contrôle de type de retour

Le format de données renvoyé par **LD** au registre de destination est déterminé de la même façon que pour l' **exemple** d’instruction. elle est basée sur le format lié au paramètre *srcResource* (*t \#*).

Comme avec l' **exemple** d’instruction, les valeurs retournées pour **LD** sont 4-vectors avec des valeurs par défaut spécifiques au format pour les composants qui ne sont pas présents dans le format. Swizzle sur *srcResource* détermine comment Swizzle le résultat à 4 composants à partir de la charge de texture, après quoi. Mask sur *dest* détermine les composants de *dest* qui sont mis à jour.

Quand une valeur float 32 bits est lue par *LD* dans un registre 32 bits, les bits ne sont pas touchés ; autrement dit, les valeurs dénormales restent dénormalisées. Contrairement à l' **exemple** d’instruction.

### <a name="miscellaneous-details"></a>Détails divers

Comme aucun filtrage n’est associé à l’instruction **LD** , les concepts tels que LOD Bias ne s’appliquent pas à **LD**. En conséquence, il n’y *a \# aucun paramètre de* l’échantillonneur.

### <a name="restrictions"></a>Restrictions

-   *srcResource* doit être un \# Registre t et non un TextureCube. *srcResource* ne peut pas être un constantbuffer, qui ne peut pas être lié à des \# registres t.
-   L’adressage relatif sur *srcResource* n’est pas autorisé.
-   *srcAddress* doit être un registre Temp (r \# /x \# ), constant (CB \# ) ou Input (v \# ).
-   *dest* doit être un registre Temp (r \# /x \# ) ou Output (o \* \# ).

Cette instruction s’applique aux étapes suivantes du nuanceur :



| Nuanceur de sommets | Nuanceur de géométrie | Nuanceur de pixels |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cette fonction est prise en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                              | Prise en charge |
|-----------------------------------------------------------|-----------|
| [Shader, modèle 5](d3d11-graphics-reference-sm5.md)        | Oui       |
| [Modèle de nuanceur 4,1](dx-graphics-hlsl-sm4.md)              | Oui       |
| [Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)                | Oui       |
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | non        |
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | non        |
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | non        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Assembly modèle 4 du nuanceur (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





