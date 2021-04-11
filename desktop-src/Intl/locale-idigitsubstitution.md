---
description: paramètres régionaux \_ IDIGITSUBSTITUTION
ms.assetid: f3f7d7ac-8f1e-4bfa-84f0-dfe8cff568c3
title: LOCALE_IDIGITSUBSTITUTION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c063ed5b937c3e4c4ae06e40631b9795f6a73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112002"
---
# <a name="locale_idigitsubstitution"></a>paramètres régionaux \_ IDIGITSUBSTITUTION

**Windows 2000 :** Forme des chiffres. Par exemple, les chiffres arabe, thaï et Indo-aryen ont des formes classiques différentes des chiffres européens. Pour les paramètres régionaux avec les [paramètres régionaux \_ SNATIVEDIGITS](locale-snative-constants.md) spécifiés en tant que valeurs autres que ASCII 0-9, cette valeur spécifie si la préférence doit être donnée à ces autres chiffres à des fins d’affichage. Par exemple, si vous choisissez la valeur 2, les chiffres spécifiés par les paramètres régionaux \_ SNATIVEDIGITS sont toujours utilisés. Si 1 est choisi, les chiffres ASCII 0-9 sont toujours utilisés. Si un 0 est choisi, ASCII est utilisé dans certaines circonstances et les chiffres spécifiés par les paramètres régionaux \_ SNATIVEDIGITS sont utilisés dans d’autres, selon le contexte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0</td>
<td>Substitution basée sur le contexte. Les chiffres s’affichent en fonction du texte précédent dans la même sortie. Les chiffres européens suivent les scripts latins, Arabic-Indic chiffres suivent le texte arabe et d’autres chiffres nationaux suivent le texte écrit dans d’autres scripts. En l’absence de texte précédent, les paramètres régionaux et l’ordre de lecture affiché déterminent la substitution des chiffres, comme indiqué dans le tableau suivant.
<table>
<thead>
<tr class="header">
<th>Paramètres régionaux</th>
<th>Ordre de lecture</th>
<th>Chiffres utilisés</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Arabe</td>
<td>De droite à gauche</td>
<td>Arabic-Indic</td>
</tr>
<tr class="even">
<td>Thaï</td>
<td>De gauche à droite</td>
<td>Chiffres thaï</td>
</tr>
<tr class="odd">
<td>Tous les autres</td>
<td>Quelconque</td>
<td>Aucune substitution utilisée</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>1</td>
<td>Aucune substitution utilisée. Compatibilité Unicode complète.</td>
</tr>
<tr class="odd">
<td>2</td>
<td>Substitution de chiffres natifs. Les formes nationales sont affichées en fonction de LOCALE_SNATIVEDIGITS.</td>
</tr>
</tbody>
</table>



 

 

 



