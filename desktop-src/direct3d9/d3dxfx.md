---
description: Options d’enregistrement et de création d’effets.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6858f659b1561a526a284b3ea2dca0e1d9a11a31
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624085"
---
# <a name="d3dxfx"></a>D3DXFX

Options d’enregistrement et de création d’effets.

Les constantes dans le tableau suivant sont définies dans d3dx9effect. h.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>Indicateurs d’enregistrement et de restauration de l’état d’effet</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Aucun État n’est enregistré lors de l’appel de <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> ou de Restore lors de l’appel de <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Un stateblock enregistre l’état lors de l’appel de <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> et restaure l’état lors de l’appel de <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Un stateblock enregistre l’État (à l’exception des nuanceurs et des constantes de nuanceur) lors de l’appel de <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> et restaure l’état lors de l’appel de <a href="id3dxeffect--end.md"><strong>end</strong></a>.</td>
</tr>
<tr class="odd">
<td>Indicateurs de création d’effet</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>L’effet ne peut pas être cloné et ne contient pas de données binaires de nuanceur. <a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> ne retourne pas les pointeurs de fonction de nuanceur. La définition de cet indicateur réduit l’effet de l’utilisation de la mémoire d’environ 50%, car elle élimine la nécessité pour le système d’effet de conserver une copie des nuanceurs en mémoire. Cet indicateur est utilisé par <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>et <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Active l’allocation d’une ressource Effect dans l’espace d’adressage uppder d’un ordinateur. Une limitation importante est que vous ne pouvez pas utiliser des chaînes et les gère de façon interchangeable. Par exemple, le code suivant ne fonctionnera plus. <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Au lieu de cela, une méthode telle que [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) doit être utilisée pour stocker le handle du paramètre, qui est ensuite utilisé pour passer des variables à l’effet.</td>
</tr>
</tbody>
</table>



 

Les constantes dans le tableau suivant ne sont pas définies par défaut et doivent être définies par le développeur.



| Définition du préprocesseur \# d’effet | Description                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Handle D3DXFX LARGEADDRESS \_   | Définissez cette valeur avant d’inclure d3dx9. h afin que votre application ne soit pas compilée quand vous tentez de passer des chaînes dans des paramètres D3DXHANDLE. Cela permet de s’assurer que des informations valides sont passées au Runtime. |
| Indicateurs de l’éditeur de liens Effects            | Description                                                                                                                                                                                                                          |
| prise en \_ charge d’adresses volumineuses \_          | La définition de l’indicateur de l’éditeur de liens pour la grande prise \_ \_ en charge de l’adresse = 1 permettra à l’application d’allouer des ressources au-delà de la limite de 2 Go si nécessaire.                                                                                      |



 

Le système d’effet utilise des blocs d’État pour enregistrer et restaurer automatiquement l’État. Pour plus d’informations sur les blocs d’État, consultez State [Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes d’effet](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



