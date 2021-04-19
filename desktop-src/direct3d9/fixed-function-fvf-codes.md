---
description: Un code d’erreur de la Commission décrit le contenu des vertex stockés entrelacés dans un flux de données unique.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Correction des codes de fonction de la Commission (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514298"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a>Correction des codes de fonction de la Commission (Direct3D 9)

Un code d’erreur de la Commission décrit le contenu des vertex stockés entrelacés dans un flux de données unique. Elle spécifie généralement les données à traiter par le pipeline de traitement de vertex de fonction fixe. Il s’agit d’une déclaration de vertex de style plus ancienne ; pour afficher le style de déclaration de vertex actuel, consultez [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

Les applications Direct3D peuvent définir des vertex de modèle de différentes façons. La prise en charge des définitions de vertex flexibles, également appelées formats de vertex flexibles ou codes de format de vertex flexibles, permet à votre application d’utiliser uniquement les composants de vertex dont elle a besoin, en éliminant les composants qui ne sont pas utilisés. En utilisant uniquement les composants de vertex nécessaires, votre application peut économiser de la mémoire et réduire la bande passante de traitement nécessaire pour restituer les modèles. Vous décrivez comment vos vertex sont mis en forme à l’aide d’une combinaison de codes [D3DFVF](d3dfvf.md) .

La spécification de la Commission des prix finals comprend des formats de taille de point, spécifiés par D3DFVF \_ psize. Cette taille est exprimée en unités d’espace de caméra pour les vertex non transformés et allumés (TL) et dans les unités d’espace de l’appareil pour les vertex TL.

Les méthodes de rendu de l’interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) fournissent aux applications C++ des méthodes qui acceptent une combinaison de ces indicateurs et les utilisent pour déterminer comment restituer les primitives. Fondamentalement, ces indicateurs indiquent au système quels sont les points de position, les poids de fusion de vertex, les couleurs normales, les couleurs et le nombre et le format des coordonnées de texture. votre application utilise et, indirectement, les parties du pipeline de rendu que vous souhaitez que Direct3D applique à celles-ci. En outre, la présence ou l’absence d’un indicateur de format de vertex particulier communique au système les champs de composant de vertex qui sont présents dans la mémoire et que vous avez omis.

Pour déterminer les limitations de l’appareil, vous pouvez interroger un appareil pour connaître les valeurs de D3DFVFCAPS \_ DONOTSTRIPELEMENTS et D3DFVFCAPS \_ TEXCOORDCOUNTMASK dans le membre FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

Les coordonnées de texture peuvent être déclarées dans différents formats, ce qui permet de résoudre les textures à l’aide d’une seule coordonnée ou jusqu’à quatre coordonnées de texture (pour les coordonnées de texture 2D projetées). Pour plus d’informations, consultez [formats de coordonnée de texture (Direct3D 9)](texture-coordinate-formats.md). Utilisez l’ensemble de macros [**\_ TEXCOORDSIZEN D3DFVF**](d3dfvf-texcoordsizen.md) pour créer des modèles de bits qui identifient les formats de coordonnée de texture utilisés par votre format de vertex.

Aucune application n’utilise chaque composant. Les champs mutuels homogènes W (RHW) et vertex normal s’excluent mutuellement. De plus, la plupart des applications essaient d’utiliser les huit jeux de coordonnées de texture, mais Direct3D dispose de cette capacité. Il existe plusieurs restrictions sur les indicateurs que vous pouvez utiliser avec d’autres indicateurs. Par exemple, vous ne pouvez pas utiliser les \_ indicateurs D3DFVF XYZ et D3DFVF \_ XYZRHW ensemble, car cela indiquerait que votre application décrit la position d’un sommet avec les vertex non transformés et transformés.

Pour utiliser la fusion de vertex indexée, l' \_ indicateur D3DFVF LASTBETA \_ UBYTE4 doit apparaître à la fin de la déclaration de la Commission des prix finaux. La présence de cet indicateur indique que la cinquième pondération de fusion sera traitée comme une valeur DWORD au lieu de float. Pour plus d’informations, consultez la rubrique relative à la [fusion des vertex indexés (Direct3D 9)](indexed-vertex-blending.md).

Les exemples de code suivants illustrent la différence entre un code d’erreur de la Commission qui utilise l' \_ indicateur D3DFVF LASTBETA \_ UBYTE4 et l’autre qui ne l’est pas. L’indicateur D3DFVF \_ XYZB3 est présent lorsque quatre index de fusion sont utilisés, car vous pouvez toujours soustraire la somme des trois premiers du numéro 1 pour obtenir le quatrième (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



La Commission de la Commission définie ci-dessous utilise l' \_ indicateur D3DFVF Last \_ UBYTE4.


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration de vertex](vertex-declaration.md)
</dt> </dl>

 

 
