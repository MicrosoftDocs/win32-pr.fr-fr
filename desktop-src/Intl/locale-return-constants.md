---
description: '\_Constantes de retour de paramètres régionaux \*'
ms.assetid: c6aadf84-c597-4cbd-a715-b68325ce5117
title: Constantes LOCALE_RETURN *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cedfb8c4434a817f334a0e2ae5ab0dd7a307ced0ddc6276351ffe4fd899eb70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106379"
---
# <a name="locale_return-constants"></a>\_Constantes de retour de paramètres régionaux \*

Cette rubrique définit les \_ constantes de retour de paramètres régionaux \* utilisées par nls.



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
<td>LOCALE_RETURN_GENITIVE_NAMES</td>
<td><strong>Windows 7 et versions ultérieures :</strong> Récupérez les noms génitif des mois, qui sont les noms utilisés lorsque les noms de mois sont combinés à d’autres éléments. Par exemple, en ukrainien, l’équivalent de janvier est écrit &quot; Січень &quot; lorsque le mois est nommé seul. Toutefois, lorsque le nom du mois est utilisé en combinaison, par exemple, dans une date telle que le 5 janvier 2003, la forme génitif du nom est utilisée. Pour l’exemple ukrainien, le nom du mois génitif s’affiche sous la forme &quot; 5 січня 2003 &quot; . La liste des noms de mois génitif commence par janvier et est délimitée par des points-virgules. S’il n’y a pas de 13e mois, utilisez un point-virgule à la fin de la liste.
<blockquote>
[!Note]<br />
Les noms de mois génitif n’existent pas dans toutes les langues.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>LOCALE_RETURN_NUMBER</td>
<td><strong>Windows Me/98, Windows NT 4,0 et versions ultérieures :</strong> Récupérez un nombre. Cette constante fait en sorte que <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> ou <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> récupère une valeur sous la forme d’un nombre et non sous forme de chaîne. La mémoire tampon qui reçoit la valeur doit être au moins égale à la longueur d’une valeur DWORD. Cette constante peut être combinée à toute autre constante dont le nom commence par &quot; LOCALE_I &quot; .</td>
</tr>
</tbody>
</table>



 

 

 




