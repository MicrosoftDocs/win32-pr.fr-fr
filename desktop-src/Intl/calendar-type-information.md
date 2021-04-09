---
description: Cette rubrique décrit les informations de type de calendrier (type de données CALTYPE) utilisées dans les fonctions EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo et GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informations sur le type de calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867946"
---
# <a name="calendar-type-information"></a>Informations sur le type de calendrier

Cette rubrique décrit les informations de type de calendrier (type de données CALTYPE) utilisées dans les fonctions [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)et [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) . Certaines de ces valeurs sont également utilisées par la fonction [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .

Les constantes CALTYPE suivantes peuvent être utilisées en association avec d’autres constantes CALTYPE.



| Constante                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_NOUSEROVERRIDE Cal          | **Windows Me/98, windows 2000 :** Utilisez la valeur par défaut du système au lieu du choix de l’utilisateur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ noms génitif de retour de licence d’accès client \_ | **Windows 7 et versions ultérieures :** Récupérez le résultat de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) sous la forme de noms génitif de mois, qui sont les noms utilisés lorsque les noms de mois sont combinés à d’autres éléments. Par exemple, en ukrainien, l’équivalent de janvier est écrit « Січень » lorsque le mois est nommé seul. Toutefois, lorsque le nom du mois est utilisé en combinaison, par exemple, dans une date telle que le 5 janvier 2003, la forme génitif du nom est utilisée. Pour l’exemple ukrainien, le nom du mois génitif est affiché sous la forme « 5 січня 2003 ». Pour plus d’informations, consultez [ \_ \_ \_ noms de paramètres régionaux](locale-return-constants.md). |
| \_numéro de retour Cal \_          | **Windows Me/98, windows 2000 :** Récupère le résultat de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) sous la forme d’un nombre au lieu d’une chaîne. Cela n’est valide que pour les valeurs commençant par la licence d’accès client \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL- \_ utiliser \_ CP \_ ACP            | **Windows Me/98, windows 2000 :** Utilisez la page de codes ANSI du système au lieu de la page de codes des paramètres régionaux pour la conversion de chaînes. Cela s’applique uniquement aux versions ANSI des fonctions, par exemple **EnumCalendarInfoA**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Les constantes CALTYPE suivantes s’excluent mutuellement et ne peuvent pas être utilisées en combinaison les unes avec les autres dans un appel de fonction.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Constante</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>CAL_ICALINTVALUE</td>
<td>Valeur entière indiquant le type de calendrier de l’autre calendrier.</td>
</tr>
<tr class="even">
<td>CAL_ITWODIGITYEARMAX</td>
<td><strong>Windows Me/98, windows 2000 :</strong> Valeur entière indiquant la limite supérieure de la plage d’années à deux chiffres.</td>
</tr>
<tr class="odd">
<td>CAL_IYEAROFFSETRANGE</td>
<td>Une ou plusieurs chaînes se terminant par un caractère null qui spécifient les décalages d’année pour chaque plage d’ère. La dernière chaîne comporte un caractère null de fin supplémentaire. Cette valeur varie en fonction du type de calendrier facultatif.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME1</td>
<td>Nom natif abrégé du premier jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME2</td>
<td>Nom natif abrégé du deuxième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME3</td>
<td>Nom natif abrégé du troisième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME4</td>
<td>Nom natif abrégé du quatrième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME5</td>
<td>Nom natif abrégé du cinquième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVDAYNAME6</td>
<td>Nom natif abrégé du sixième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVDAYNAME7</td>
<td>Nom natif abrégé du septième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVERASTRING</td>
<td><strong>Windows 7 et versions ultérieures :</strong> Nom natif abrégé d’une ère. L’ère complète est représentée par la constante CAL_SERASTRING.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME1</td>
<td>Nom natif abrégé du premier mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME2</td>
<td>Nom natif abrégé du deuxième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME3</td>
<td>Nom natif abrégé du troisième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME4</td>
<td>Nom natif abrégé du quatrième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME5</td>
<td>Nom natif abrégé du cinquième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME6</td>
<td>Nom natif abrégé du sixième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME7</td>
<td>Nom natif abrégé du septième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME8</td>
<td>Nom natif abrégé du huitième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME9</td>
<td>Nom natif abrégé du neuvième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME10</td>
<td>Nom natif abrégé du dixième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME11</td>
<td>Nom natif abrégé du onzième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SABBREVMONTHNAME12</td>
<td>Nom natif abrégé du douzième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SABBREVMONTHNAME13</td>
<td>Nom natif abrégé du treizième mois de l’année, le cas échéant.</td>
</tr>
<tr class="odd">
<td>CAL_SCALNAME</td>
<td>Nom natif de l’autre calendrier.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME1</td>
<td>Nom natif du premier jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME2</td>
<td>Nom natif du deuxième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME3</td>
<td>Nom natif du troisième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME4</td>
<td>Nom natif du quatrième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME5</td>
<td>Nom natif du cinquième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SDAYNAME6</td>
<td>Nom natif du sixième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SDAYNAME7</td>
<td>Nom natif du septième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SERASTRING</td>
<td>Une ou plusieurs chaînes se terminant par un caractère null qui spécifient chacun des points de code Unicode spécifiant l’ère associée à CAL_IYEAROFFSETRANGE. La dernière chaîne comporte un caractère null de fin supplémentaire. Cette valeur varie en fonction du type de calendrier facultatif.</td>
</tr>
<tr class="even">
<td>CAL_SLONGDATE</td>
<td>Formats de date longue pour le type de calendrier.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHDAY</td>
<td><strong>Windows 7 et versions ultérieures :</strong> Format du mois et du jour pour le type de calendrier. La mise en forme est similaire à celle de CAL_SLONGDATE. Par exemple, si le modèle de mois/jour est le nom complet du mois suivi du nombre de jours avec des zéros non significatifs, par exemple, &quot; &quot; le format est &quot; Mmmm jj &quot; . Des guillemets simples peuvent être utilisés pour insérer des caractères qui ne sont pas de format, par exemple « de » en espagnol.
<blockquote>
[!Note]<br />
Ce type de calendrier ne prend en charge qu’un seul format.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME1</td>
<td>Nom natif du premier mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME2</td>
<td>Nom natif du deuxième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME3</td>
<td>Nom natif du troisième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME4</td>
<td>Nom natif du quatrième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME5</td>
<td>Nom natif du cinquième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME6</td>
<td>Nom natif du sixième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME7</td>
<td>Nom natif du septième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME8</td>
<td>Nom natif du huitième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME9</td>
<td>Nom natif du neuvième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME10</td>
<td>Nom natif du dixième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME11</td>
<td>Nom natif du onzième mois de l’année.</td>
</tr>
<tr class="odd">
<td>CAL_SMONTHNAME12</td>
<td>Nom natif du douzième mois de l’année.</td>
</tr>
<tr class="even">
<td>CAL_SMONTHNAME13</td>
<td>Nom natif du treizième mois de l’année, le cas échéant.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTDATE</td>
<td>Formats de date courts pour le type de calendrier.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME1</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du premier jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME2</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du deuxième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME3</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du troisième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME4</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du quatrième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME5</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du cinquième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SSHORTESTDAYNAME6</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du sixième jour de la semaine.</td>
</tr>
<tr class="even">
<td>CAL_SSHORTESTDAYNAME7</td>
<td><strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du septième jour de la semaine.</td>
</tr>
<tr class="odd">
<td>CAL_SYEARMONTH</td>
<td><strong>Windows Me/98, windows 2000 :</strong> Formats année/mois pour les calendriers spécifiés.</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Si le nom natif du jour de la semaine ou pour un mois est une chaîne vide, ce nom est identique au nom spécifié dans les informations de paramètres régionaux correspondants et n’est donc pas dupliqué ici.

 

 

 




