---
description: Indicateur de fonctionnalité du pilote.
ms.assetid: 78ff4433-f0b5-4bbb-b2c0-bd389fbc31ce
title: D3DENUM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50cb3ed10a4a12602e8586bbd0e941641287346a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012827"
---
# <a name="d3denum"></a>D3DENUM

Indicateur de fonctionnalité du pilote.



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
<td>D3DENUM_WHQL_LEVEL</td>
<td>0x00000002L</td>
<td>test des pilotes WHQL (Microsoft Windows Hardware Quality Labs). Il s’agit d’un test qui prend beaucoup de temps, ce qui nécessite une pénalité d’une seconde ou de deux secondes. Cette constante est utilisée par le membre WHQLLevel de <a href="d3dadapter-identifier9.md"><strong>D3DADAPTER_IDENTIFIER9</strong></a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 9Ex :<br/> D3DENUM_WHQL_LEVEL est déconseillé pour les Direct3D9Ex s’exécutant sur Windows Vista, Windows server 2008, Windows 7 et Windows server 2008 R2 (ou plus le système d’exploitation actuel). L’un de ces systèmes d’exploitation retourne 1 pour le niveau WHQL sans vérifier l’état du pilote. <br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9. h     |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




