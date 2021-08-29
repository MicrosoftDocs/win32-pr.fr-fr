---
description: Cette rubrique décrit les informations de type de calendrier (type de données CALTYPE) utilisées dans les fonctions EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo et GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Informations sur le type de calendrier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 719591e3c912b68dca08ab600b9fa479377b9ef0
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473725"
---
# <a name="calendar-type-information"></a>Informations sur le type de calendrier

Cette rubrique décrit les informations de type de calendrier (type de données CALTYPE) utilisées dans les fonctions [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)et [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) . Certaines de ces valeurs sont également utilisées par la fonction [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .

Les constantes CALTYPE suivantes peuvent être utilisées en association avec d’autres constantes CALTYPE.



| Constante                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_NOUSEROVERRIDE Cal          | **Windows Me/98, Windows 2000 :** Utilisez la valeur par défaut du système au lieu du choix de l’utilisateur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ noms génitif de retour de licence d’accès client \_ | **Windows 7 et versions ultérieures :** Récupérez le résultat de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) sous la forme de noms génitif de mois, qui sont les noms utilisés lorsque les noms de mois sont combinés à d’autres éléments. Par exemple, en ukrainien, l’équivalent de janvier est écrit « Січень » lorsque le mois est nommé seul. Toutefois, lorsque le nom du mois est utilisé en combinaison, par exemple, dans une date telle que le 5 janvier 2003, la forme génitif du nom est utilisée. Pour l’exemple ukrainien, le nom du mois génitif est affiché sous la forme « 5 січня 2003 ». Pour plus d’informations, consultez [ \_ \_ \_ noms de paramètres régionaux](locale-return-constants.md). |
| \_numéro de retour Cal \_          | **Windows Me/98, Windows 2000 :** Récupère le résultat de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) sous la forme d’un nombre au lieu d’une chaîne. Cela n’est valide que pour les valeurs commençant par la licence d’accès client \_ I.                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| CAL- \_ utiliser \_ CP \_ ACP            | **Windows Me/98, Windows 2000 :** Utilisez la page de codes ANSI du système au lieu de la page de codes des paramètres régionaux pour la conversion de chaînes. Cela s’applique uniquement aux versions ANSI des fonctions, par exemple **EnumCalendarInfoA**.                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Les constantes CALTYPE suivantes s’excluent mutuellement et ne peuvent pas être utilisées en combinaison les unes avec les autres dans un appel de fonction.




| Constante | Description | 
|----------|-------------|
| CAL_ICALINTVALUE | Valeur entière indiquant le type de calendrier de l’autre calendrier. | 
| CAL_ITWODIGITYEARMAX | <strong>Windows Me/98, Windows 2000 :</strong> Valeur entière indiquant la limite supérieure de la plage d’années à deux chiffres. | 
| CAL_IYEAROFFSETRANGE | Une ou plusieurs chaînes se terminant par un caractère null qui spécifient les décalages d’année pour chaque plage d’ère. La dernière chaîne comporte un caractère null de fin supplémentaire. Cette valeur varie en fonction du type de calendrier facultatif. | 
| CAL_SABBREVDAYNAME1 | Nom natif abrégé du premier jour de la semaine. | 
| CAL_SABBREVDAYNAME2 | Nom natif abrégé du deuxième jour de la semaine. | 
| CAL_SABBREVDAYNAME3 | Nom natif abrégé du troisième jour de la semaine. | 
| CAL_SABBREVDAYNAME4 | Nom natif abrégé du quatrième jour de la semaine. | 
| CAL_SABBREVDAYNAME5 | Nom natif abrégé du cinquième jour de la semaine. | 
| CAL_SABBREVDAYNAME6 | Nom natif abrégé du sixième jour de la semaine. | 
| CAL_SABBREVDAYNAME7 | Nom natif abrégé du septième jour de la semaine. | 
| CAL_SABBREVERASTRING | <strong>Windows 7 et versions ultérieures :</strong> Nom natif abrégé d’une ère. L’ère complète est représentée par la constante CAL_SERASTRING. | 
| CAL_SABBREVMONTHNAME1 | Nom natif abrégé du premier mois de l’année. | 
| CAL_SABBREVMONTHNAME2 | Nom natif abrégé du deuxième mois de l’année. | 
| CAL_SABBREVMONTHNAME3 | Nom natif abrégé du troisième mois de l’année. | 
| CAL_SABBREVMONTHNAME4 | Nom natif abrégé du quatrième mois de l’année. | 
| CAL_SABBREVMONTHNAME5 | Nom natif abrégé du cinquième mois de l’année. | 
| CAL_SABBREVMONTHNAME6 | Nom natif abrégé du sixième mois de l’année. | 
| CAL_SABBREVMONTHNAME7 | Nom natif abrégé du septième mois de l’année. | 
| CAL_SABBREVMONTHNAME8 | Nom natif abrégé du huitième mois de l’année. | 
| CAL_SABBREVMONTHNAME9 | Nom natif abrégé du neuvième mois de l’année. | 
| CAL_SABBREVMONTHNAME10 | Nom natif abrégé du dixième mois de l’année. | 
| CAL_SABBREVMONTHNAME11 | Nom natif abrégé du onzième mois de l’année. | 
| CAL_SABBREVMONTHNAME12 | Nom natif abrégé du douzième mois de l’année. | 
| CAL_SABBREVMONTHNAME13 | Nom natif abrégé du treizième mois de l’année, le cas échéant. | 
| CAL_SCALNAME | Nom natif de l’autre calendrier. | 
| CAL_SDAYNAME1 | Nom natif du premier jour de la semaine. | 
| CAL_SDAYNAME2 | Nom natif du deuxième jour de la semaine. | 
| CAL_SDAYNAME3 | Nom natif du troisième jour de la semaine. | 
| CAL_SDAYNAME4 | Nom natif du quatrième jour de la semaine. | 
| CAL_SDAYNAME5 | Nom natif du cinquième jour de la semaine. | 
| CAL_SDAYNAME6 | Nom natif du sixième jour de la semaine. | 
| CAL_SDAYNAME7 | Nom natif du septième jour de la semaine. | 
| CAL_SERASTRING | Une ou plusieurs chaînes se terminant par un caractère null qui spécifient chacun des points de code Unicode spécifiant l’ère associée à CAL_IYEAROFFSETRANGE. La dernière chaîne comporte un caractère null de fin supplémentaire. Cette valeur varie en fonction du type de calendrier facultatif. | 
| CAL_SLONGDATE | Formats de date longue pour le type de calendrier. | 
| CAL_SMONTHDAY | <strong>Windows 7 et versions ultérieures :</strong> Format du mois et du jour pour le type de calendrier. La mise en forme est similaire à celle de CAL_SLONGDATE. Par exemple, si le modèle de mois/jour est le nom complet du mois suivi du nombre de jours avec des zéros non significatifs, par exemple, « 03 septembre », le format est « MMMM JJ ». Des guillemets simples peuvent être utilisés pour insérer des caractères qui ne sont pas de format, par exemple « de » en espagnol.<blockquote>[!Note]<br />Ce type de calendrier ne prend en charge qu’un seul format.</blockquote><br /> | 
| CAL_SMONTHNAME1 | Nom natif du premier mois de l’année. | 
| CAL_SMONTHNAME2 | Nom natif du deuxième mois de l’année. | 
| CAL_SMONTHNAME3 | Nom natif du troisième mois de l’année. | 
| CAL_SMONTHNAME4 | Nom natif du quatrième mois de l’année. | 
| CAL_SMONTHNAME5 | Nom natif du cinquième mois de l’année. | 
| CAL_SMONTHNAME6 | Nom natif du sixième mois de l’année. | 
| CAL_SMONTHNAME7 | Nom natif du septième mois de l’année. | 
| CAL_SMONTHNAME8 | Nom natif du huitième mois de l’année. | 
| CAL_SMONTHNAME9 | Nom natif du neuvième mois de l’année. | 
| CAL_SMONTHNAME10 | Nom natif du dixième mois de l’année. | 
| CAL_SMONTHNAME11 | Nom natif du onzième mois de l’année. | 
| CAL_SMONTHNAME12 | Nom natif du douzième mois de l’année. | 
| CAL_SMONTHNAME13 | Nom natif du treizième mois de l’année, le cas échéant. | 
| CAL_SSHORTDATE | Formats de date courts pour le type de calendrier. | 
| CAL_SSHORTESTDAYNAME1 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du premier jour de la semaine. | 
| CAL_SSHORTESTDAYNAME2 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du deuxième jour de la semaine. | 
| CAL_SSHORTESTDAYNAME3 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du troisième jour de la semaine. | 
| CAL_SSHORTESTDAYNAME4 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du quatrième jour de la semaine. | 
| CAL_SSHORTESTDAYNAME5 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du cinquième jour de la semaine. | 
| CAL_SSHORTESTDAYNAME6 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du sixième jour de la semaine. | 
| CAL_SSHORTESTDAYNAME7 | <strong>Windows Vista et versions ultérieures :</strong> Nom natif abrégé du septième jour de la semaine. | 
| CAL_SYEARMONTH | <strong>Windows Me/98, Windows 2000 :</strong> Formats année/mois pour les calendriers spécifiés. | 




 

> [!Note]  
> Si le nom natif du jour de la semaine ou pour un mois est une chaîne vide, ce nom est identique au nom spécifié dans les informations de paramètres régionaux correspondants et n’est donc pas dupliqué ici.

 

 

 




