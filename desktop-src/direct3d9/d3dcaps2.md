---
description: Consultez la liste des indicateurs de capacité du pilote. Comprend les définitions, les valeurs et les descriptions avec des liens vers des API.
ms.assetid: 0c0c65fc-f953-4379-a6d0-6ce447a0c183
title: D3DCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f209e840450b834c3a69593d1297f2cba9ee43c0
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343374"
---
# <a name="d3dcaps2"></a>D3DCAPS2

Indicateurs de capacité du pilote.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#définition</td>
<td>Valeur</td>
<td>Description</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANAUTOGENMIPMAP</td>
<td>0x40000000L</td>
<td>Le pilote est en capacité de générer automatiquement des des mipmaps. Pour plus d’informations, consultez <a href="automatic-generation-of-mipmaps.md">génération automatique de des mipmaps (Direct3D 9)</a>.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_CANCALIBRATEGAMMA</td>
<td>0x00100000L</td>
<td>Un étalonnage est installé sur le système et peut ajuster automatiquement la rampe gamma afin que le résultat soit identique sur tous les systèmes ayant un étalonnage. Pour appeler le étalonnage lors de la définition de nouveaux niveaux gamma, utilisez l’indicateur D3DSGR_CALIBRATE lors de l’appel de <a href="/windows/desktop/api"><strong>SetGammaRamp</strong></a>. L’étalonnage des rampes gamma entraîne une surcharge de traitement et ne doit pas être utilisé fréquemment.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_CANSHARERESOURCE</td>
<td>0x80000000L</td>
<td>L’appareil peut créer des ressources partageables. Les méthodes qui créent des ressources peuvent définir des valeurs non NULL pour leurs paramètres <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getsharedhandle"><strong>pSharedHandle</strong></a> . 
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
<td>D3DCAPS2_CANMANAGERESOURCE</td>
<td>0x10000000L</td>
<td>Le pilote est en charge de la gestion des ressources. Sur ces pilotes, les ressources de D3DPOOL_MANAGED seront gérées par le pilote. Pour que Direct3D remplace le pilote afin que Direct3D gère les ressources, utilisez l’indicateur D3DCREATE_DISABLE_DRIVER_MANAGEMENT lors de l’appel de <a href="/windows/desktop/api"><strong>CreateDevice</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_DYNAMICTEXTURES</td>
<td>0x20000000L</td>
<td>Le pilote prend en charge les textures dynamiques.</td>
</tr>
<tr class="odd">
<td>D3DCAPS2_FULLSCREENGAMMA</td>
<td>0x00020000L</td>
<td>Le pilote prend en charge l’ajustement dynamique de la rampe gamma en mode plein écran.</td>
</tr>
<tr class="even">
<td>D3DCAPS2_RESERVED</td>
<td>0x02000000L</td>
<td>Réservé non utilisé.</td>
</tr>
</tbody>
</table>



 

Ces constantes sont utilisées par le membre D3CAPS2 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



|  Condition requise                        | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
