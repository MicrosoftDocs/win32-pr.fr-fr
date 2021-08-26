---
description: Indicateurs des fonctionnalités primitives du pilote divers.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee88ba03b3c0a6d51c0100b20768df4cbf632d46
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624535"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Indicateurs des fonctionnalités primitives du pilote divers.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Valeur</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>L’appareil peut activer et désactiver la modification de la mémoire tampon de profondeur sur les opérations de pixels.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>Le pilote n’effectue pas l’élimination des triangles. Cela correspond au membre D3DCULL_NONE du type énuméré <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>Le pilote prend en charge le sens des aiguilles d’une montre à travers l’État D3DRS_CULLMODE. (Cela s’applique uniquement aux primitives de triangle.) Cet indicateur correspond au D3DCULL_CW membre du type énuméré <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>Le pilote prend en charge l’élimination dans le sens inverse dans l’État D3DRS_CULLMODE. (Cela s’applique uniquement aux primitives de triangle.) Cet indicateur correspond au D3DCULL_CCW membre du type énuméré <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>L’appareil prend en charge les écritures par canal pour la mémoire tampon de couleur de rendu-cible par le biais de l’État D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>L’appareil découpe correctement les points de la taille mis à l’échelle de plus de 1,0 en plans de découpage définis par l’utilisateur.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Éléments d’appareil primitives de vertex transformés. Spécifiez D3DUSAGE_DONOTCLIP lorsque le pipeline ne doit pas effectuer de découpage. Dans ce cas, il peut être nécessaire d’effectuer des découpages logiciels supplémentaires au moment du dessin, ce qui nécessite que la mémoire tampon du vertex soit dans la mémoire système.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>L’appareil prend en charge <a href="d3dta.md">D3DTA</a> pour le registre temporaire.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>L’appareil prend en charge les opérations de fusion alpha autres que D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Appareil de référence qui n’est pas rendu.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>L’appareil prend en charge des masques d’écriture indépendants pour plusieurs textures d’élément ou plusieurs cibles de rendu.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>L’appareil prend en charge les constantes par étape. Consultez D3DTSS_CONSTANT dans <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>L’appareil prend en charge la conversion en sRVB après la fusion. 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Cet indicateur est disponible uniquement dans Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>L’appareil prend en charge le brouillard distinct et l’alpha spéculaire. De nombreux appareils utilisent le canal alpha spéculaire pour stocker le facteur de brouillard.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>L’appareil prend en charge des paramètres de fusion distincts pour le canal alpha.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>L’appareil prend en charge des profondeurs différentes pour plusieurs cibles de rendu.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>L’appareil prend en charge les opérations de nuanceur de pixel après plusieurs cibles de rendu.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Pinces de l’appareil : facteur de mélange de brouillard par vertex.</td>
</tr>
</tbody>
</table>



 

Ces constantes sont utilisées par le membre PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



| Condition requise                         |  Valeur          |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
